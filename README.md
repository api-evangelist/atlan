# Atlan

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
