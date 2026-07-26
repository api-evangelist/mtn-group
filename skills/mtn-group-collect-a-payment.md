---
name: Collect and reconcile a payment
description: Generate a payment link or take a merchant payment through the MTN Payments API, then poll transaction
  status, fetch history, and reverse when needed.
api: openapi/mtn-group-payments-v1.yml
operations:
- Payment_post_generatePaymentLink_paymentlink
- Payment_post_merchantPayment_merchantpayment
- Payment_post_payment
- Payment_post_feeCheck_fee
- Payment_get_getPaymentTransactionStatus_correlatorIdtransact
- Payment_get_getPaymentByTransactionId_detailstransactionid
- Payment_get_paymentHistory_idhistory
- Payment_post_reversePayment_reversepayment
provider: MTN Group
generated: '2026-07-25'
method: generated
---

# Collect and reconcile a payment

Generate a payment link or take a merchant payment through the MTN Payments API, then poll transaction status, fetch history, and reverse when needed.

## Authentication (every MTN Developer Platform call)

1. `POST https://api.mtn.com/v1/oauth/access_token?grant_type=client_credentials` with
   `Content-Type: application/x-www-form-urlencoded` and body
   `client_id={consumer-key}&client_secret={consumer-secret}`.
2. Read `access_token` from the response (`token_type` is `BearerToken`, `expires_in` is `3599`).
3. Send `Authorization: Bearer {access_token}` on every call, plus the `x-api-key` header carrying the
   app consumer key. Cache the token for its lifetime; do not mint one per request.

## Steps

1. Mint a token (see Authentication). Base URL `https://api.mtn.com/v1`.
2. Optional — quote the cost first: `POST /fee` — operationId `Payment_post_feeCheck_fee`.
3. Take the money one of three ways:
   - `POST /payment-link` — operationId `Payment_post_generatePaymentLink_paymentlink` — hand the payer a link.
   - `POST /merchant-payment` — operationId `Payment_post_merchantPayment_merchantpayment` — merchant collection.
   - `POST /payments` — operationId `Payment_post_payment` — pay a service provider.
4. Payments are asynchronous. Poll
   `GET /{correlatorId}/transactionStatus` — operationId
   `Payment_get_getPaymentTransactionStatus_correlatorIdtransact` — until the status is terminal,
   or `GET /details/{transactionid}` — operationId `Payment_get_getPaymentByTransactionId_detailstransactionid`.
5. Reconcile with `GET /{id}/history` — operationId `Payment_get_paymentHistory_idhistory`.
6. To undo: `POST /reverse-payment` — operationId `Payment_post_reversePayment_reversepayment` — and audit
   with `GET /reverse-payment/history`.

## Cautions

- Never retry a payment POST blind. Read status first; MTN error `6001` is insufficient funds and `1004`
  means the request is still pending (HTTP 102).
- Consent flows exist for USSD and SMS (`POST /payments/ussd/consent`, `POST /payments/sms/consent`) —
  capture consent before debiting where the market requires it.

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
