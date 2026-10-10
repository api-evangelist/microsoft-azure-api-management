---
name: microsoft-azure-api-management-gateway-create-or-update
description: Create a new gateway or update an existing one in Azure API Management.
api: openapi/microsoft-azure-api-management-gateway-api-openapi.yml
operations:
- Gateway_CreateOrUpdate
- Gateway_Get
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/microsoft-azure-api-management-gateway-api-openapi.yml ; every operationId checked against the contract
---

# microsoft-azure-api-management-gateway-create-or-update

Create a new gateway or update an existing one in Azure API Management.

## Steps

1. 1. Call `Gateway_CreateOrUpdate` with required path parameters `subscriptionId`, `resourceGroupName`, `serviceName`, `gatewayId` and request body containing the gateway definition.
2. 2. Call `Gateway_Get` with the same path parameters to retrieve the created or updated gateway details.

## Rules

- Authentication: Include an `Authorization: Bearer <token>` header using the `azure_auth` OAuth2 scheme.
- Idempotency: The `Gateway_CreateOrUpdate` operation uses HTTP PUT, which is idempotent; repeated calls with the same payload will not create duplicate resources.
