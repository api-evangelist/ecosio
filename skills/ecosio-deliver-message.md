---
name: ecosio-deliver-message
description: Send an EDI message or e-invoice to the ecosio Integration Hub and track its status and acknowledgement.
api: ecosio-api
operations:
- securityCredentials
- deliverMessage
- getStatusOfDeliveredMessage
- getAcknowledgement
generated: '2026-10-18'
method: generated
source: openapi/ecosio-api-openapi.yml
---

# Send an EDI message or e-invoice to the ecosio Integration Hub and track its status and acknowledgement.

## Steps

1. Verify credentials with `securityCredentials` (HTTP Basic user id/user key plus `X-APP-KEY` header).
2. POST the document with `deliverMessage`; keep the returned messageId.
3. Poll `getStatusOfDeliveredMessage` with the messageId until processing completes.
4. For e-invoices, read the receiver acknowledgement with `getAcknowledgement`.

## Rules

- deliverMessage creates a new message on each call: the spec documents no idempotency key, so do not blindly retry a POST that may have succeeded — check status first.
- Grounded in operationIds from `openapi/ecosio-api-openapi.yml`; docs: https://connect.ecosio.com/reference/llms.txt
