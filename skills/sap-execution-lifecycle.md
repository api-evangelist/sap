---
name: sap-execution-lifecycle
description: Create an execution, retrieve its details, list executions, and stop the execution.
api: openapi/sap-executions-api-openapi.yml
operations:
- createExecution
- getExecution
- listExecutions
- deleteExecution
generated: '2026-10-03'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/sap-executions-api-openapi.yml ; every operationId checked against the contract
---

# sap-execution-lifecycle

Create an execution, retrieve its details, list executions, and stop the execution.

## Steps

1. 1. `createExecution` – body fields: `executionId`, `parameters`, `type`.
2. 2. `getExecution` – path parameter: `executionId`.
3. 3. `listExecutions` – query parameters: `page`, `pageSize`, `filter` (if supported).
4. 4. `deleteExecution` – path parameter: `executionId`.

## Rules

- Auth: include either a Basic Auth header, an OAuth2 Bearer token, or a sessionCookie API key as required by the endpoint.
- No rate limit is defined; on exhaustion the service returns no specific HTTP status.
