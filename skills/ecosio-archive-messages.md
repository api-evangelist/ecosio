---
name: ecosio-archive-messages
description: Request an archive of exchanged messages from ecosio.
api: ecosio-api
operations:
- create-archive
generated: '2026-10-18'
method: generated
source: openapi/ecosio-api-openapi.yml
---

# Request an archive of exchanged messages from ecosio.

## Steps

1. Create the archive request with `create-archive`; keep the archiveId.
2. Poll GET /api/v1/archives/{archiveId} (no published operationId; overlay names it getArchiveStatus) until ready.
3. Download with GET /api/v1/downloads/{archiveId} (overlay names it downloadArchive).

## Rules

- The status and download operations have no operationId in the provider spec; the overlay adds names for them.
- Grounded in operationIds from `openapi/ecosio-api-openapi.yml`; docs: https://connect.ecosio.com/reference/llms.txt
