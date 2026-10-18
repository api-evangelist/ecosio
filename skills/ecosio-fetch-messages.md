---
name: ecosio-fetch-messages
description: Fetch newly received messages from the ecosio Integration Hub and acknowledge processing.
api: ecosio-api
operations:
- getMessageList
- getReceivedMessage
- callback
generated: '2026-10-18'
method: generated
source: openapi/ecosio-api-openapi.yml
---

# Fetch newly received messages from the ecosio Integration Hub and acknowledge processing.

## Steps

1. List newly received messages with `getMessageList`.
2. Download each one with `getReceivedMessage`.
3. Report success or failure of local processing with `callback` for that messageId.

## Rules

- Always call `callback` after processing so the Hub does not keep re-offering the message.
- Grounded in operationIds from `openapi/ecosio-api-openapi.yml`; docs: https://connect.ecosio.com/reference/llms.txt
