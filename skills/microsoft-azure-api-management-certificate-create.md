---
name: microsoft-azure-api-management-certificate-create
description: Create a new certificate in an Azure API Management service.
api: openapi/microsoft-azure-api-management-certificate-api-openapi.yml
operations:
- Certificate_CreateOrUpdate
- Certificate_Get
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/microsoft-azure-api-management-certificate-api-openapi.yml ; every operationId checked against the contract
---

# microsoft-azure-api-management-certificate-create

Create a new certificate in an Azure API Management service.

## Steps

1. 1. Use `Certificate_CreateOrUpdate` with required path parameters `subscriptionId`, `resourceGroupName`, `serviceName`, `certificateId` and request body containing the certificate properties.
2. 2. Use `Certificate_Get` with the same path parameters to retrieve and verify the created certificate.

## Rules

- Auth header: Include an `Authorization: Bearer <token>` header using the `azure_auth` OAuth2 scheme.
- Idempotency: The `Certificate_CreateOrUpdate` PUT operation is idempotent; repeating the request with the same `certificateId` will not create duplicate resources.
