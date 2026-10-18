---
name: ecosio-manage-connectors
description: Create and maintain ecosio connectors, the companies they serve and their credentials.
api: ecosio-management-api
operations:
- findConnectors
- createConnector
- getConnector
- updateConnector
- replaceCompanies
- regenerateCredentials
generated: '2026-10-18'
method: generated
source: openapi/ecosio-management-api-openapi.yml
---

# Create and maintain ecosio connectors, the companies they serve and their credentials.

## Steps

1. List with `findConnectors`, or create with `createConnector`.
2. Inspect with `getConnector` and change settings with `updateConnector`.
3. Set the companies a connector serves with `replaceCompanies` (full replacement, not append).
4. Rotate secrets with `regenerateCredentials` — old credentials stop working.

## Rules

- `regenerateCredentials` is destructive for existing integrations; confirm with a human first.
- Grounded in operationIds from `openapi/ecosio-management-api-openapi.yml`; docs: https://connect.ecosio.com/reference/llms.txt
