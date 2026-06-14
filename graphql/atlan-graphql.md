# Atlan GraphQL API

Atlan exposes a tenant-scoped GraphQL API that provides flexible querying of the platform's knowledge graph — the unified metadata layer spanning 80+ data sources. Through GraphQL, clients can traverse relationships between assets (tables, columns, schemas, databases, dashboards, pipelines) and their associated metadata including Atlan Tags (classifications), business glossary terms, data lineage connections, custom metadata, and governance artifacts such as Personas and Purposes. The schema follows the Apache Atlas entity model extended with Atlan-specific types, meaning every asset is a subtype of the root `Asset` interface, which itself extends `Referenceable`.

Authentication uses the same credential model as the REST API: either a long-lived API token or a short-lived OAuth 2.0 access token obtained via the Client Credentials flow. Both are supplied as a `Bearer` token in the `Authorization` HTTP header. The API token is generated from the Atlan tenant UI under Settings → API Tokens; the OAuth client ID and secret are created under Settings → OAuth Clients. All requests must target the caller's own tenant subdomain — there is no shared multi-tenant endpoint.

The GraphQL endpoint is per-tenant and follows the pattern `https://{tenant}.atlan.com/api/graphql`, where `{tenant}` is the subdomain assigned to your Atlan deployment (for example `https://acme.atlan.com/api/graphql`). Queries support pagination via `offset` and `limit` arguments and can filter across all indexed asset attributes. The API is documented in the Atlan developer hub and the community knowledge base; the SDK source repositories (`atlan-python`, `atlan-java`, `atlan-go`) reflect the canonical type model used by the GraphQL schema.

**Endpoint:** `https://{tenant}.atlan.com/api/graphql`

**Documentation:** https://docs.atlan.com/

**References:**
- Documentation: https://docs.atlan.com/
- GettingStarted: https://docs.atlan.com/get-started/references/api-authentication
