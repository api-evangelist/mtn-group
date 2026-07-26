---
name: Place a TM Forum product order
description: Create, retrieve and cancel a TMF622 ProductOrder against the MTN catalogue, after resolving the offering
  from the TMF620 product catalog.
api: openapi/mtn-group-tmf-product-ordering-tmf622.yml
operations:
- createProductOrder
- retrieveProductOrder
- deleteProductOrder
provider: MTN Group
generated: '2026-07-25'
method: generated
---

# Place a TM Forum product order

Create, retrieve and cancel a TMF622 ProductOrder against the MTN catalogue, after resolving the offering from the TMF620 product catalog.

## Authentication (every MTN Developer Platform call)

1. `POST https://api.mtn.com/v1/oauth/access_token?grant_type=client_credentials` with
   `Content-Type: application/x-www-form-urlencoded` and body
   `client_id={consumer-key}&client_secret={consumer-secret}`.
2. Read `access_token` from the response (`token_type` is `BearerToken`, `expires_in` is `3599`).
3. Send `Authorization: Bearer {access_token}` on every call, plus the `x-api-key` header carrying the
   app consumer key. Cache the token for its lifetime; do not mint one per request.

## Steps

1. Mint a token (see Authentication).
2. Resolve what can be ordered from the TMF620 catalog
   (`openapi/mtn-group-tmf-product-catalog-tmf620.yml`, base `https://api.mtn.com/tmf-api/productcatalog/v1`).
3. `POST /productOrder` — operationId `createProductOrder` — against
   `https://api.mtn.com/tmf-api/productordering/v1` with the TMF622 ProductOrder payload.
4. `GET /productOrder/{id}` — operationId `retrieveProductOrder` — to track fulfilment state.
5. `DELETE /productOrder/{id}` — operationId `deleteProductOrder` — to cancel.

## Events

Register for order and service lifecycle events with the TMF hub pattern rather than polling in a loop:
`POST /hub` (`registerListener`) and `DELETE /hub/{id}` (`unregisterListener`) on the service activation and
resource inventory products. See `asyncapi/mtn-group-webhooks.yml`.

## Cautions

- The COE variant (`openapi/mtn-group-product-ordering-coe.yml`) exposes the same three operationIds against
  a different deployment. Pick the one that matches the market you are provisioned in.
- Order creation is asynchronous; a `201` is an acknowledgement, not fulfilment.

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
