---
name: ecosio-vertex-receive-messages
description: Poll, read and confirm messages on the Vertex e-invoicing Messaging API.
api: ecosio-vertex-messaging-api
operations:
- getMessageList
- getMessage
- getDocuments
- confirm
- sendMessage
generated: '2026-10-18'
method: generated
source: openapi/ecosio-vertex-messaging-api-openapi.yml
---

# Poll, read and confirm messages on the Vertex e-invoicing Messaging API.

## Steps

1. Obtain an OAuth2 client-credentials token.
2. Poll `getMessageList`, then read each with `getMessage` and `getDocuments`.
3. Mark processed messages with `confirm`.
4. Send outbound documents with `sendMessage`.

## Rules

- Confirm only after durable local storage of the documents.
- Grounded in operationIds from `openapi/ecosio-vertex-messaging-api-openapi.yml`; docs: https://connect.ecosio.com/reference/llms.txt
