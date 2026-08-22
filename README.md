# Microsoft Azure API Management (microsoft-azure-api-management)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Microsoft Azure API Management is a hybrid, multicloud management platform for APIs across all environments. It is composed of an API gateway (data plane), a management plane, and a developer portal, and supports the complete API lifecycle for publishing, securing, monitoring, and transforming APIs for external, partner, and internal developers. It now includes an AI gateway for governing OpenAI Chat Completions, OpenAI Responses, Anthropic Messages, Microsoft Foundry models, Amazon Bedrock, MCP servers exposed from REST APIs or proxied from external MCP backends, and A2A agent APIs - with token rate limiting, semantic caching, content safety, backend load balancing, circuit breakers, and token emission to Application Insights. It pairs with Azure API Center for design-time inventory, governance, and discovery.

**URL:** [apis.yml](https://raw.githubusercontent.com/api-evangelist/microsoft-azure-api-management/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags
- A2A
- AI Gateway
- API Center
- API Gateway
- API Management
- Enterprise
- MCP
- Microsoft Azure

## Timestamps
- **Created:** 2026-03-16
- **Modified:** 2026-05-22

## APIs

### Azure API Management REST API
Programmatic management plane for API Management instances and their child entities (APIs, products, subscriptions, users, groups, policies, gateways, backends, certificates, workspaces). Uses Azure Resource Manager conventions; API versions through 2024-05-01. Over 100 operation groups.
- humanURL: https://learn.microsoft.com/en-us/rest/api/apimanagement/
- baseURL: https://management.azure.com/
- OpenAPI: `openapi/microsoft-azure-api-management-rest-api-openapi.yaml`
- Capabilities: 60+ entity-level capability YAMLs under `capabilities/rest-*.yaml`

### Azure API Management Gateway
Cloud-hosted data plane that accepts API calls, verifies credentials, applies policies (rate limits, quotas, transformations, caching, content safety), and emits telemetry.
- humanURL: https://learn.microsoft.com/en-us/azure/api-management/api-management-key-concepts
- baseURL: https://{instance}.azure-api.net
- OpenAPI: `openapi/microsoft-azure-api-management-gateway-openapi.yaml`
- Capabilities: `capabilities/gateway-gateway.yaml`, `capabilities/gateway-health.yaml`

### Azure API Management Self-Hosted Gateway
Linux-based container image of the gateway runtime, deployable to Kubernetes (AKS, Arc-enabled Kubernetes), Docker, or any orchestration platform, federated with a cloud-based API Management instance.
- humanURL: https://learn.microsoft.com/en-us/azure/api-management/self-hosted-gateway-overview
- baseURL: https://mcr.microsoft.com/product/azure-api-management/gateway
- OpenAPI: `openapi/microsoft-azure-api-management-self-hosted-gateway-openapi.yaml`
- Capabilities: `capabilities/self-hosted-gateway-gateway.yaml`, `capabilities/self-hosted-gateway-health.yaml`

### Azure API Management AI Gateway
AI gateway capabilities layered on the API Management gateway: TPM/token quota policies, semantic caching with Azure Managed Redis, backend load balancing (round-robin / weighted / priority / session-aware) with dynamic circuit breakers, Azure AI Content Safety policy, and `llm-emit-token-metric` for Application Insights. Supports OpenAI Chat Completions, OpenAI Responses, Anthropic Messages (v2 tiers), Microsoft Foundry models, Amazon Bedrock, self-hosted models, MCP servers, and A2A agent APIs. Available across Developer, Basic, Basic v2, Standard, Standard v2, Premium, and Premium v2 tiers.
- humanURL: https://learn.microsoft.com/en-us/azure/api-management/genai-gateway-capabilities
- OpenAPI: `openapi/microsoft-azure-api-management-ai-gateway-openapi.yaml`
- MCP server overview: https://learn.microsoft.com/en-us/azure/api-management/mcp-server-overview
- Capabilities: `capabilities/ai-gateway-ai.yaml`, `capabilities/ai-gateway-mcp.yaml`

### Azure API Center
Design-time API inventory, governance, and discovery service that complements API Management's runtime governance. Includes a VS Code extension with linting and breaking-change detection, an enterprise API Center portal, MCP server registry, and Copilot Studio connector. Standard plan included at no extra cost when linked to API Management Standard, Standard v2, Premium, or Premium v2.
- humanURL: https://learn.microsoft.com/en-us/azure/api-center/overview
- baseURL: https://management.azure.com/
- MCP registry: https://learn.microsoft.com/en-us/azure/api-center/register-discover-mcp-server

### Azure API Management Developer Portal
Auto-generated, fully customizable developer portal. Open-source TypeScript codebase (latest 2.34.0, October 2025) that can be self-hosted and extended with custom branding.
- humanURL: https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-developer-portal-customize
- baseURL: https://{instance}.developer.azure-api.net
- OpenAPI: `openapi/microsoft-azure-api-management-developer-portal-openapi.yaml`
- Source: https://github.com/Azure/api-management-developer-portal
- Capabilities: `capabilities/developer-portal-apis.yaml`, `capabilities/developer-portal-authentication.yaml`, `capabilities/developer-portal-portal.yaml`, `capabilities/developer-portal-products.yaml`, `capabilities/developer-portal-user.yaml`

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
| SDK (.NET) | https://github.com/Azure/azure-sdk-for-net/tree/main/sdk/apimanagement |
| SDK (Java) | https://github.com/Azure/azure-sdk-for-java/tree/main/sdk/apimanagement |
| SDK (JavaScript) | https://github.com/Azure/azure-sdk-for-js/tree/main/sdk/apimanagement |
| SDK (Python) | https://github.com/Azure/azure-sdk-for-python/tree/main/sdk/apimanagement |
| SDK (Go) | https://github.com/Azure/azure-sdk-for-go/tree/main/sdk/resourcemanager/apimanagement |
| VSCodeExtension | https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-apimanagement |
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
| PolicySnippets | https://github.com/Azure/api-management-policy-snippets |
| PolicyToolkit | https://github.com/Azure/azure-api-management-policy-toolkit |
| AIGatewaySamples | https://github.com/Azure-Samples/ai-gateway |
| AIGatewayWorkshop | https://aka.ms/ai-gateway/workshop |
| AIHubReferenceArchitecture | https://github.com/Azure-Samples/ai-hub-gateway-solution-accelerator |
| APICenter | https://learn.microsoft.com/en-us/azure/api-center/overview |
| FoundryIntegration | https://learn.microsoft.com/en-us/azure/ai-foundry/configuration/enable-ai-api-management-gateway-portal |
| MCPServer | https://github.com/Azure/azure-api-mcp |

## Pricing Tiers (May 2026)

| Tier | Capacity | Notable Features | List Price |
|---|---|---|---|
| Consumption | Auto-scaled, per-call | Serverless, no dedicated capacity | First 1M calls/month free; ~$3.50 per additional 1M |
| Developer | 1 scale unit | Non-production, all features, no SLA | Hourly per unit |
| Basic | Up to 2 units | 50 MB cache, production SLA | ~$0.21/hour (~$150/unit/month) |
| Basic v2 | Up to 10 units | Autoscaling, 250 MB cache, includes 10M req/month | ~$150/unit/month + ~$3 per additional 1M |
| Standard | Up to 4 units | 1 GB cache, backup/restore | ~$0.96/hour (~$700/unit/month) |
| Standard v2 | Up to 10 units | Outbound VNet integration, autoscaling, includes 50M req/month, free linked API Center Standard | ~$700/unit/month + ~$2.50 per additional 1M |
| Premium | Up to 12 units per region | Multi-region, VNet injection, self-hosted gateway, workspaces, 5 GB cache | ~$3.83/hour (~$2,795/unit/month) |
| Premium v2 | Up to 30 units | Availability zones, outbound VNet integration, workspaces, unlimited requests, 99.99% SLA, free linked API Center Standard | starts ~$2,801/unit/month |

See `plans/microsoft-azure-api-management-plans-pricing.yml`, `rate-limits/microsoft-azure-api-management-rate-limits.yml`, and `finops/microsoft-azure-api-management-finops.yml` for machine-readable detail.

## Notable Breaking Changes and Retirements
Source: https://learn.microsoft.com/en-us/azure/api-management/breaking-changes/overview
- **stv1 platform retirement** — Global Azure (Aug 31, 2024); sovereign clouds (Feb 24, 2025).
- **Git repository retirement** and **Direct management API retirement** — March 15, 2025.
- **Managed certificates suspension** — Aug 15, 2025 through March 15, 2026.
- **ADAL-based Microsoft Entra ID identity provider retirement** — Sep 30, 2025.
- **Trusted service connectivity retirement** — March 15, 2026.
- **Built-in analytics dashboard retirement** — March 15, 2027.

## Artifacts

### openapi/
- microsoft-azure-api-management-ai-gateway-openapi.yaml
- microsoft-azure-api-management-developer-portal-openapi.yaml
- microsoft-azure-api-management-gateway-openapi.yaml
- microsoft-azure-api-management-rest-api-openapi.yaml
- microsoft-azure-api-management-self-hosted-gateway-openapi.yaml

### capabilities/
72 capability YAMLs covering:
- AI gateway: `ai-gateway-ai.yaml`, `ai-gateway-mcp.yaml`
- Cloud gateway: `gateway-gateway.yaml`, `gateway-health.yaml`
- Self-hosted gateway: `self-hosted-gateway-gateway.yaml`, `self-hosted-gateway-health.yaml`
- Developer portal: `developer-portal-apis.yaml`, `developer-portal-authentication.yaml`, `developer-portal-portal.yaml`, `developer-portal-products.yaml`, `developer-portal-user.yaml`
- REST API management plane: 60+ `rest-*.yaml` capabilities (apis, products, subscriptions, gateways, backends, certificates, named values, policies, workspaces, tags, users, groups, etc.)

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

### rules/
- microsoft-azure-api-management-rules.yaml

### vocabulary/
- microsoft-azure-api-management-vocabulary.yaml

### plans/, rate-limits/, finops/
- plans/microsoft-azure-api-management-plans-pricing.yml
- rate-limits/microsoft-azure-api-management-rate-limits.yml
- finops/microsoft-azure-api-management-finops.yml

## Maintainers
- Kin Lane — kin@apievangelist.com
