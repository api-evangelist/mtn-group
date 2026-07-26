---
name: Subscribe a customer to a value-added service
description: List, create, inspect and cancel MTN value-added service subscriptions for a customer, including provisioning-status
  polling and the delete-all callback.
api: openapi/mtn-group-mtn-subscription-api-v2.yml
operations:
- List all Subscriptions
- Subscribe the customer to a new service
- Get Subscription Details
- Get Subscription Provisioning Status
- Delete a specific subscription
- Delete All subscriptions
- Retrieve subscription providers
provider: MTN Group
generated: '2026-07-25'
method: generated
---

# Subscribe a customer to a value-added service

List, create, inspect and cancel MTN value-added service subscriptions for a customer, including provisioning-status polling and the delete-all callback.

## Authentication (every MTN Developer Platform call)

1. `POST https://api.mtn.com/v1/oauth/access_token?grant_type=client_credentials` with
   `Content-Type: application/x-www-form-urlencoded` and body
   `client_id={consumer-key}&client_secret={consumer-secret}`.
2. Read `access_token` from the response (`token_type` is `BearerToken`, `expires_in` is `3599`).
3. Send `Authorization: Bearer {access_token}` on every call, plus the `x-api-key` header carrying the
   app consumer key. Cache the token for its lifetime; do not mint one per request.

## Steps

1. Mint a token (see Authentication). Base URL `https://api.mtn.com/v2`.
2. `GET /customers/{customerId}/subscriptions-providers` — operationId `Retrieve subscription providers` —
   to discover what the customer can subscribe to.
3. `GET /customers/{customerId}/subscriptions` — operationId `List all Subscriptions` — for current state.
   Guard against MTN error `1002` (already subscribed) before creating.
4. `POST /customers/{customerId}/subscriptions` — operationId
   `Subscribe the customer to a new service`.
5. Provisioning is asynchronous: poll
   `GET /customers/{customerId}/subscriptions/{subscriptionId}/status/{statusId}` — operationId
   `Get Subscription Provisioning Status` — until it settles.
6. `GET /customers/{customerId}/subscriptions/{subscriptionId}` — operationId `Get Subscription Details`.
7. Cancel one with operationId `Delete a specific subscription`, or all with `Delete All subscriptions`.
   The bulk delete reports back asynchronously to `POST /callback/delete-all-subscriptions`.

## Cautions

- `1003` means already unsubscribed — treat both `1002` and `1003` as idempotent no-ops, not failures.
- This product declares named business statuses (`463` subscription channel not found, `464` subscription
  not found, `467` active subscription exists, `485` pending subscription exists, `515` subscription not
  active). Map them explicitly; see `errors/mtn-group-problem-types.yml`.

## Rules the agent must follow

- Versioning is URI-path (`/v1`, `/v2`). Only the current version and n-1 are supported.
- Dates are RFC 3339, MSISDNs E.123 (country code included), countries ISO 3166, currencies ISO 4217.
- Responses are JSON, camelCase, wrapped with `data` and `_links` (HATEOAS) — follow `_links` rather than
  building URLs by hand.
- Send the `transactionID` header for traceability; some products require it.
- On failure read the MTN error code from the body, not just the HTTP status:
  `1013`/`3006` = rate exceeded (back off), `4000` = unauthorized (re-mint the token), `5000` = invalid
  parameters, `6001` = insufficient funds. Full registry: `errors/mtn-group-error-codes.yml`.
- HTTP `102` means the request is still processing and `207` means partial success — inspect the body per
  component before declaring success.
- No platform rate limits are published; treat `429` as authoritative and back off exponentially.
