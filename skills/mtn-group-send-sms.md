---
name: Send an SMS and track delivery
description: Send an SMS through the MTN SMS API, poll its delivery status, and register a callback listener for
  inbound messages and delivery receipts.
api: openapi/mtn-group-mtn-sms-api-v1.yml
operations:
- sendSMS
- Get SMS Status
- Retrieve SMS Responses
- registerCallback
- deregister Callback
provider: MTN Group
generated: '2026-07-25'
method: generated
---

# Send an SMS and track delivery

Send an SMS through the MTN SMS API, poll its delivery status, and register a callback listener for inbound messages and delivery receipts.

## Authentication (every MTN Developer Platform call)

1. `POST https://api.mtn.com/v1/oauth/access_token?grant_type=client_credentials` with
   `Content-Type: application/x-www-form-urlencoded` and body
   `client_id={consumer-key}&client_secret={consumer-secret}`.
2. Read `access_token` from the response (`token_type` is `BearerToken`, `expires_in` is `3599`).
3. Send `Authorization: Bearer {access_token}` on every call, plus the `x-api-key` header carrying the
   app consumer key. Cache the token for its lifetime; do not mint one per request.

## Steps

1. Mint a token (see Authentication).
2. `POST /sms` — operationId `sendSMS` — with the message payload. The base URL is
   `https://api.mtn.com/v1/messages/`.
3. Capture the returned `messageId`.
4. `GET /sms/{messageId}/status` — operationId `Get SMS Status` — to read delivery status. Poll rather
   than assuming success; SMS delivery is asynchronous.
5. To receive inbound messages and delivery receipts instead of polling, `POST /sms-listeners`
   — operationId `registerCallback` — with your HTTPS listener. Remove it with
   `DELETE /sms-listeners/{accessCode}` — operationId `deregister Callback`.
6. `GET /sms` — operationId `Retrieve SMS Responses` — pulls responses when no listener is registered.

## Cautions

- Message bodies are capped; MoMo documentation notes 160 characters for note/message fields on the
  payment products, and long SMS content should be split by the caller.
- Do not re-send on a timeout without checking status first — the message may already be in flight.

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
