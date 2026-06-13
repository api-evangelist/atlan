# Atlan

Atlan is a data catalog and metadata management platform — the Context Layer for AI — that unifies metadata from 80+ business systems into a single knowledge graph. It provides REST and GraphQL APIs for managing data assets, lineage, classifications, glossary terms, and data governance workflows. Customers execute 10,000+ API calls per week powering automated documentation, metadata enrichment, and custom integrations across the modern data stack.

**Website:** https://atlan.com/
**Documentation:** https://docs.atlan.com/
**Developer GitHub:** https://github.com/atlanhq
**Blog:** https://blog.atlan.com/
**Status:** https://status.atlan.com/
**LinkedIn:** https://www.linkedin.com/company/atlan-hq/
**X:** https://x.com/atlanhq

## APIs

- **REST API** — Full platform access for assets, lineage, glossary, classifications, governance, personas, and purposes via versioned REST endpoints.
- **GraphQL API** — Flexible graph traversal of the metadata knowledge graph.
- **Webhooks API** — Real-time event delivery for metadata change notifications.

## SDKs

| Language | Repository |
|---|---|
| Python | https://github.com/atlanhq/atlan-python |
| Java / Kotlin / Scala / Clojure | https://github.com/atlanhq/atlan-java |
| Go | https://github.com/atlanhq/atlan-go |
| Application SDK (Python) | https://github.com/atlanhq/application-sdk |
| AI Agent Toolkit | https://github.com/atlanhq/agent-toolkit |

## Authentication

Atlan supports two authentication methods:

- **API Tokens** — Static bearer tokens tied to a user or service account. Simple setup for scripts and local development.
- **OAuth 2.0 Client Credentials** — Short-lived scoped tokens for server-to-server workloads (CI/CD pipelines, backend services). Recommended for production.

Set `ATLAN_BASE_URL` and `ATLAN_API_KEY` (or `ATLAN_OAUTH_CLIENT_ID` / `ATLAN_OAUTH_CLIENT_SECRET`) as environment variables.

## Rate Limits

Atlan enforces per-tenant rate limits and returns HTTP 429 when exceeded. SDKs automatically retry with exponential backoff (Python: 5 retries; Java: 3 retries). Specific numeric thresholds are tenant-specific and not publicly disclosed.

## Pricing

Enterprise, quote-based pricing. No public self-serve tiers. Contracts range from ~$10,000/year (small teams) to $500,000+/year (large enterprise). Contact Atlan sales for a custom proposal.

- [Plans and Pricing](plans/atlan-plans-pricing.yml)
- [Rate Limits](rate-limits/atlan-rate-limits.yml)
- [FinOps](finops/atlan-finops.yml)

---

*Maintained by [Kin Lane](mailto:kin@apievangelist.com) — [APIs.json](apis.yml)*
