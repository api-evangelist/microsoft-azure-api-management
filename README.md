# Microsoft Azure API Management (microsoft-azure-api-management)
Microsoft Azure API Management is a hybrid, multicloud management platform for APIs across all environments. It provides an API gateway, management plane, and developer portal supporting the complete API lifecycle including publishing, securing, monitoring, and transforming APIs for external, partner, and internal developers. It includes an AI gateway for governing LLM deployments, MCP servers, and agentic AI workloads.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/microsoft-azure-api-management/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:
- AI Gateway
- API Gateway
- API Management
- Enterprise
- Microsoft Azure

## Timestamps:
- **Created:** 2026-03-16
- **Modified:** 2026-04-21

## APIs

### Azure API Management REST API
The Azure API Management REST API provides programmatic access to manage API Management service instances and their entities, including APIs, products, subscriptions, users, groups, policies, gateways, backends, certificates, and workspaces. It uses Azure Resource Manager conventions and supports API versions up to 2024-05-01 with over 100 operation groups covering the full management plane.
- **humanURL:** https://learn.microsoft.com/en-us/rest/api/apimanagement/
- **baseURL:** https://management.azure.com/

#### Properties:
| Type | URL |
|---|---|
| Documentation | https://learn.microsoft.com/en-us/rest/api/apimanagement/ |
| APIReference | https://learn.microsoft.com/en-us/rest/api/apimanagement/operation-groups |
| Authentication | https://learn.microsoft.com/en-us/azure/api-management/authentication-authorization-overview |
| SDK | https://github.com/Azure/azure-sdk-for-python/tree/main/sdk/apimanagement |
| SDK | https://github.com/Azure/azure-sdk-for-net/tree/main/sdk/apimanagement |
| SDK | https://github.com/Azure/azure-sdk-for-java/tree/main/sdk/apimanagement |
| SDK | https://github.com/Azure/azure-sdk-for-js/tree/main/sdk/apimanagement |
| SDK | https://github.com/Azure/azure-sdk-for-go/tree/main/sdk/resourcemanager/apimanagement |
| OpenAPI | openapi/microsoft-azure-api-management-rest-api-openapi.yaml |
| NaftikoCapability | capabilities/shared/rest-api.yaml |

#### Tags:
- Azure Resource Manager
- Configuration
- Management Plane
- REST

### Azure API Management Gateway
The Azure API Management gateway (data plane) acts as a facade to backend services, routing API requests, enforcing policies, verifying credentials, applying rate limits and quotas, caching responses, and emitting telemetry. It supports managed cloud-hosted and self-hosted containerized deployments for hybrid and multicloud environments.
- **humanURL:** https://learn.microsoft.com/en-us/azure/api-management/api-management-key-concepts
- **baseURL:** https://azure-api.net

#### Properties:
| Type | URL |
|---|---|
| Documentation | https://learn.microsoft.com/en-us/azure/api-management/api-management-key-concepts |
| APIReference | https://learn.microsoft.com/en-us/azure/api-management/api-management-policies |
| Authentication | https://learn.microsoft.com/en-us/azure/api-management/authentication-authorization-overview |
| GettingStarted | https://learn.microsoft.com/en-us/azure/api-management/import-and-publish |
| Tutorials | https://learn.microsoft.com/en-us/azure/api-management/transform-api |
| PolicySnippets | https://github.com/Azure/api-management-policy-snippets |
| Tools | https://github.com/Azure/azure-api-management-policy-toolkit |
| OpenAPI | openapi/microsoft-azure-api-management-gateway-openapi.yaml |
| NaftikoCapability | capabilities/shared/gateway.yaml |

#### Tags:
- API Gateway
- Policies
- Proxy
- Traffic Management

### Azure API Management Self-Hosted Gateway
The Azure API Management self-hosted gateway is a containerized, Linux-based Docker image that can be deployed to Kubernetes, Docker, or any container orchestration platform in on-premises or other cloud environments. It federates with a cloud-based API Management instance for centralized configuration and management while routing API traffic locally to reduce latency and address compliance requirements.
- **humanURL:** https://learn.microsoft.com/en-us/azure/api-management/self-hosted-gateway-overview
- **baseURL:** https://mcr.microsoft.com/product/azure-api-management/gateway

#### Properties:
| Type | URL |
|---|---|
| Documentation | https://learn.microsoft.com/en-us/azure/api-management/self-hosted-gateway-overview |
| GettingStarted | https://learn.microsoft.com/en-us/azure/api-management/how-to-deploy-self-hosted-gateway-azure-kubernetes-service |
| GitHubRepository | https://github.com/Azure/api-management-self-hosted-gateway |
| HelmChart | https://github.com/Azure/api-management-self-hosted-gateway/tree/main/helm-charts/azure-api-management-gateway |
| CodeExamples | https://github.com/Azure/api-management-self-hosted-gateway-ingress |
| OpenAPI | openapi/microsoft-azure-api-management-self-hosted-gateway-openapi.yaml |
| NaftikoCapability | capabilities/shared/self-hosted-gateway.yaml |

#### Tags:
- Hybrid
- Kubernetes
- On-Premises
- Self-Hosted

### Azure API Management AI Gateway
The Azure API Management AI gateway is a set of capabilities for managing, securing, scaling, and observing AI backends including Microsoft Foundry and Azure OpenAI deployments, OpenAI-compatible LLM endpoints, MCP servers, and A2A agent APIs. It provides token rate limiting and quotas, semantic caching, load balancing across AI backends, content safety enforcement, and token usage observability through Application Insights.
- **humanURL:** https://learn.microsoft.com/en-us/azure/api-management/genai-gateway-capabilities
- **baseURL:** https://management.azure.com/

#### Properties:
| Type | URL |
|---|---|
| Documentation | https://learn.microsoft.com/en-us/azure/api-management/genai-gateway-capabilities |
| GettingStarted | https://learn.microsoft.com/en-us/azure/api-management/azure-openai-api-from-specification |
| Quickstart | https://learn.microsoft.com/en-us/azure/api-management/azure-ai-foundry-api |
| OpenAPI | openapi/microsoft-azure-api-management-ai-gateway-openapi.yaml |
| JSONSchema | json-schema/ai-gateway-chat-completion-request-schema.json |
| JSONSchema | json-schema/ai-gateway-chat-completion-response-schema.json |
| JSONSchema | json-schema/ai-gateway-completion-request-schema.json |
| JSONSchema | json-schema/ai-gateway-completion-response-schema.json |
| JSONSchema | json-schema/ai-gateway-embedding-request-schema.json |
| JSONSchema | json-schema/ai-gateway-embedding-response-schema.json |
| JSONSchema | json-schema/ai-gateway-mcp-request-schema.json |
| JSONSchema | json-schema/ai-gateway-mcp-response-schema.json |
| JSONStructure | json-structure/ai-gateway-chat-completion-request-structure.json |
| JSONStructure | json-structure/ai-gateway-chat-completion-response-structure.json |
| JSONStructure | json-structure/ai-gateway-completion-request-structure.json |
| JSONStructure | json-structure/ai-gateway-completion-response-structure.json |
| JSONStructure | json-structure/ai-gateway-embedding-request-structure.json |
| JSONStructure | json-structure/ai-gateway-embedding-response-structure.json |
| JSONStructure | json-structure/ai-gateway-mcp-request-structure.json |
| JSONStructure | json-structure/ai-gateway-mcp-response-structure.json |
| JSONLD | json-ld/microsoft-azure-api-management-ai-gateway-context.jsonld |
| Example | examples/ai-gateway-chat-completion-request-example.json |
| Example | examples/ai-gateway-chat-completion-response-example.json |
| Example | examples/ai-gateway-completion-request-example.json |
| Example | examples/ai-gateway-completion-response-example.json |
| Example | examples/ai-gateway-embedding-request-example.json |
| Example | examples/ai-gateway-embedding-response-example.json |
| Example | examples/ai-gateway-mcp-request-example.json |
| Example | examples/ai-gateway-mcp-response-example.json |
| NaftikoCapability | capabilities/shared/ai-gateway.yaml |

#### Tags:
- AI Gateway
- Azure OpenAI
- LLM
- MCP

### Azure API Management Developer Portal
The Azure API Management developer portal is an automatically generated, fully customizable website that allows API consumers to discover APIs, read documentation, test APIs through an interactive console, create accounts, subscribe to API products, and manage API keys. It can be self-hosted and extended with custom content and branding.
- **humanURL:** https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-developer-portal-customize
- **baseURL:** https://developer.azure-api.net

#### Properties:
| Type | URL |
|---|---|
| Documentation | https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-developer-portal-customize |
| Tutorials | https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-developer-portal-customize |
| GitHubRepository | https://github.com/Azure/api-management-developer-portal |
| OpenAPI | openapi/microsoft-azure-api-management-developer-portal-openapi.yaml |
| NaftikoCapability | capabilities/shared/developer-portal.yaml |

#### Tags:
- API Discovery
- Developer Portal
- Documentation
- Self-Service

## Common Properties
| Type | URL |
|---|---|
| Website | https://azure.microsoft.com/products/api-management/ |
| Documentation | https://learn.microsoft.com/en-us/azure/api-management/ |
| GettingStarted | https://learn.microsoft.com/en-us/azure/api-management/get-started-create-service-instance |
| Quickstart | https://learn.microsoft.com/en-us/azure/api-management/get-started-create-service-instance-cli |
| APIReference | https://learn.microsoft.com/en-us/rest/api/apimanagement/ |
| Authentication | https://learn.microsoft.com/en-us/azure/api-management/authentication-authorization-overview |
| Pricing | https://azure.microsoft.com/pricing/details/api-management/ |
| Tiers | https://learn.microsoft.com/en-us/azure/api-management/api-management-features |
| ChangeLog | https://learn.microsoft.com/en-us/azure/api-management/breaking-changes/overview |
| Support | https://learn.microsoft.com/answers/tags/29/azure-api-management/ |
| Console | https://portal.azure.com/ |
| CLI | https://learn.microsoft.com/en-us/cli/azure/apim |
| SDK | https://github.com/Azure/azure-sdk-for-python/tree/main/sdk/apimanagement |
| Tutorials | https://learn.microsoft.com/en-us/azure/api-management/import-and-publish |
| Training | https://learn.microsoft.com/en-us/training/modules/explore-api-management/ |
| Security | https://learn.microsoft.com/en-us/azure/api-management/authentication-authorization-overview |
| BestPractices | https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-policies |
| Blog | https://techcommunity.microsoft.com/t5/azure/ct-p/Azure |
| GitHubRepository | https://github.com/Azure/api-management-samples |
| GitHubOrganization | https://github.com/Azure |
| TermsOfService | https://azure.microsoft.com/support/legal/ |
| PrivacyPolicy | https://privacy.microsoft.com/privacystatement |
| Regions | https://azure.microsoft.com/explore/global-infrastructure/products-by-region/ |
| Compliance | https://learn.microsoft.com/en-us/azure/compliance/ |
| TrustCenter | https://www.microsoft.com/trust-center |
| SignUp | https://azure.microsoft.com/free/ |
| StatusPage | https://status.azure.com/ |
| DeveloperPortal | https://learn.microsoft.com/en-us/azure/api-management/developer-portal-overview |
| SDK | https://github.com/Azure/azure-sdk-for-net/tree/main/sdk/apimanagement |
| SDK | https://github.com/Azure/azure-sdk-for-java/tree/main/sdk/apimanagement |
| SDK | https://github.com/Azure/azure-sdk-for-js/tree/main/sdk/apimanagement |
| SDK | https://github.com/Azure/azure-sdk-for-go/tree/main/sdk/resourcemanager/apimanagement |
| CodeExamples | https://github.com/Azure/api-management-samples |
| PolicySnippets | https://github.com/Azure/api-management-policy-snippets |
| Tools | https://github.com/Azure/azure-api-management-policy-toolkit |
| ChangeLog | https://github.com/Azure/API-Management/blob/master/changelogs/api-management-service.md |
| SpectralRules | rules/microsoft-azure-api-management-rules.yaml |
| Vocabulary | vocabulary/microsoft-azure-api-management-vocabulary.yaml |
| NaftikoCapability | capabilities/ai-gateway-management.yaml |
| NaftikoCapability | capabilities/api-lifecycle-management.yaml |
| NaftikoCapability | capabilities/developer-onboarding.yaml |
| NaftikoCapability | capabilities/gateway-operations.yaml |

## Artifacts

### openapi/
- microsoft-azure-api-management-ai-gateway-openapi.yaml
- microsoft-azure-api-management-developer-portal-openapi.yaml
- microsoft-azure-api-management-gateway-openapi.yaml
- microsoft-azure-api-management-rest-api-openapi.yaml
- microsoft-azure-api-management-self-hosted-gateway-openapi.yaml

### json-schema/
- ai-gateway-chat-completion-request-schema.json
- ai-gateway-chat-completion-response-schema.json
- ai-gateway-completion-request-schema.json
- ai-gateway-completion-response-schema.json
- ai-gateway-embedding-request-schema.json
- ai-gateway-embedding-response-schema.json
- ai-gateway-mcp-request-schema.json
- ai-gateway-mcp-response-schema.json

### json-structure/
- ai-gateway-chat-completion-request-structure.json
- ai-gateway-chat-completion-response-structure.json
- ai-gateway-completion-request-structure.json
- ai-gateway-completion-response-structure.json
- ai-gateway-embedding-request-structure.json
- ai-gateway-embedding-response-structure.json
- ai-gateway-mcp-request-structure.json
- ai-gateway-mcp-response-structure.json

### json-ld/
- microsoft-azure-api-management-ai-gateway-context.jsonld

### examples/
- ai-gateway-chat-completion-request-example.json
- ai-gateway-chat-completion-response-example.json
- ai-gateway-completion-request-example.json
- ai-gateway-completion-response-example.json
- ai-gateway-embedding-request-example.json
- ai-gateway-embedding-response-example.json
- ai-gateway-mcp-request-example.json
- ai-gateway-mcp-response-example.json

### capabilities/shared/
- ai-gateway.yaml
- developer-portal.yaml
- gateway.yaml
- rest-api.yaml
- self-hosted-gateway.yaml

### capabilities/
- ai-gateway-management.yaml
- api-lifecycle-management.yaml
- developer-onboarding.yaml
- gateway-operations.yaml

### vocabulary/
- microsoft-azure-api-management-vocabulary.yaml

### rules/
- microsoft-azure-api-management-rules.yaml

## Maintainers
- FN: Kin Lane
  email: kin@apievangelist.com
