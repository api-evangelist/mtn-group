---
name: Request a MoMo payment and handle the callback
description: 'Run the MoMo Collection request-to-pay flow end to end in sandbox: provision an API user, mint a token,
  submit the request with a unique X-Reference-Id, then reconcile via callback or status polling.'
api: https://momodeveloper.mtn.com/api-documentation
operations: []
provider: MTN Group
generated: '2026-07-25'
method: generated
---

# Request a MoMo payment and handle the callback

Run the MoMo Collection request-to-pay flow end to end in sandbox: provision an API user, mint a token, submit the request with a unique X-Reference-Id, then reconcile via callback or status polling.

## Authentication (every MTN Developer Platform call)

1. `POST https://api.mtn.com/v1/oauth/access_token?grant_type=client_credentials` with
   `Content-Type: application/x-www-form-urlencoded` and body
   `client_id={consumer-key}&client_secret={consumer-secret}`.
2. Read `access_token` from the response (`token_type` is `BearerToken`, `expires_in` is `3599`).
3. Send `Authorization: Bearer {access_token}` on every call, plus the `x-api-key` header carrying the
   app consumer key. Cache the token for its lifetime; do not mint one per request.

## Steps

1. Subscribe to the Collection product on https://momodeveloper.mtn.com/ and take the
   `Ocp-Apim-Subscription-Key` (primary or secondary) from https://momodeveloper.mtn.com/profile.
2. Provision a sandbox API user and key with the Sandbox Provisioning API, passing `providerCallbackHost`
   in the body. Existing Partner GUI accounts cannot be used for sandbox use cases.
3. Exchange the API user and key for an OAuth token.
4. Submit the collection with headers:
   `Ocp-Apim-Subscription-Key`, `Authorization: Bearer {token}`,
   `X-Target-Environment: sandbox` (or the market value, e.g. `mtnnigeria`),
   `X-Reference-Id: {fresh UUID v4}`, and optionally `X-Callback-Url`.
   A valid submission answers `202 Accepted`.
5. Reconcile. The Wallet Platform sends the callback **exactly once with no retry**, so always implement
   status polling on the same `X-Reference-Id` as the fallback.

## Idempotency

`X-Reference-Id` is the idempotency and correlation key. It must be UUID v4 and unique per request; reusing
one returns `409 RESOURCE_ALREADY_EXIST`. Persist it before sending so a crashed retry can resume by polling
rather than re-charging.

## Sandbox

Currency is `EUR`. Predefined payer MSISDNs drive deterministic outcomes — `46733123451` rejects,
`46733123452` expires, `46733123455` is payer-not-found, and any other number succeeds. The full matrix is in
`sandbox/mtn-group-sandbox.yml`; failure reasons are in `errors/mtn-group-decline-codes.yml`.

## Cautions

- The callback host must match the registered `providerCallbackHost`, HTTPS only, and the listener must
  accept both POST and PUT. A mismatch fails with `INVALID_CALLBACK_URL_HOST`.
- `X-Callback-Url` should not be sent in sandbox.

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
