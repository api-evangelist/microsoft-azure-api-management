---
name: microsoft-azure-api-management-create-or-update-service
description: Create a new API Management service or update an existing one and retrieve its details.
api: openapi/microsoft-azure-api-management-apimanagementservice-api-openapi.yml
operations:
- ApiManagementService_CreateOrUpdate
- ApiManagementService_Get
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/microsoft-azure-api-management-apimanagementservice-api-openapi.yml ; every operationId checked against the contract
---

# microsoft-azure-api-management-create-or-update-service

Create a new API Management service or update an existing one and retrieve its details.

## Steps

1. 1. Call `ApiManagementService_CreateOrUpdate` with path parameters `subscriptionId`, `resourceGroupName`, `serviceName` and a request body containing the service definition.
2. 2. Call `ApiManagementService_Get` with the same `subscriptionId`, `resourceGroupName`, and `serviceName` to verify the service was created or updated.

## Rules

- Authentication: Include an `Authorization: Bearer <token>` header using the `azure_auth` OAuth2 scheme.
- Idempotency: `ApiManagementService_CreateOrUpdate` is idempotent when the same `serviceName` and request body are provided.
