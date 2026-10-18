---
name: ecosio-onboard-company
description: Create a company on ecosio, apply a compliance/connectivity scenario and track the approval.
api: ecosio-management-api
operations:
- findCompanies
- createCompany
- listAvailableScenarios
- createScenario
- listAppliedScenarios
- getStatus
generated: '2026-10-18'
method: generated
source: openapi/ecosio-management-api-openapi.yml
---

# Create a company on ecosio, apply a compliance/connectivity scenario and track the approval.

## Steps

1. Check whether the company exists with `findCompanies`; otherwise `createCompany`.
2. Pick a scenario from `listAvailableScenarios`.
3. Apply it with `createScenario` for the companyUuid.
4. Track the resulting approval with `getStatus` and confirm via `listAppliedScenarios`.

## Rules

- Search before creating to avoid duplicate companies; the spec documents no idempotency key.
- Grounded in operationIds from `openapi/ecosio-management-api-openapi.yml`; docs: https://connect.ecosio.com/reference/llms.txt
