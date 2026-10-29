# Bupa Australia

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

Bupa Australia is the Australian market unit of the UK-headquartered Bupa group and one of the country's largest private health insurers, trading as Bupa HI Pty Ltd (ABN 81 000 057 590). It writes private health insurance — hospital and ancillary "extras" cover, overseas visitor and overseas student health cover, and corporate health plans — and, unusually for a carrier, also owns the provision that consumes those benefits through Bupa Dental, Bupa Optical, Bupa Medical Visa Services and Bupa Aged Care. Its lines of business are health and care rather than property and casualty or life, so the ACORD data standards that shape most of the insurance sector are entirely absent from its published surface; no reference to ACORD, AL3, ACORD XML or NGDS appears anywhere on its public web estate. Australia gives it no forcing function either: the Consumer Data Right was designated to extend to general insurance and then deferred, and a first-hand query of the CDR participant register at api.cdr.gov.au on 2026-07-25 returned 203 data-holder brands drawn only from banking and energy, with no insurance sector and no Bupa brand present. Bupa Australia's API posture is accordingly partner-gated. It does run a genuine first-party developer portal at portal.api.bupa.com.au — an Azure API Management managed portal whose meta author tag names Bupa HI Pty Ltd — but the portal returns HTTP 200 while listing nothing: its /apis and /products routes render empty "APIs: List" and "Products: List" headings to anonymous visitors, its config.json points at an internal-only management host, and its Get Started page routes every onboarding step through the "Bupa Integration Fabric Team" before any API specification is released. No public OpenAPI or Swagger definition, Postman collection, GraphQL schema, gRPC service or webhook catalog could be confirmed, and none of the four insurance verbs — quote, bind, issue or FNOL — is exposed to unauthenticated developers. The real integration surface for Bupa Australia's counterparties is not an API at all: ancillary providers claim through HICAPS and HealthPoint terminals, hospital providers check patient eligibility and lodge claims through ECLIPSE, the national Services Australia claiming channel reached via Civica's ECF web front-end, and access to the Bupa Partner Portal at partner.bupa.com.au is requested by downloading and returning a PDF form.

**Areas:** Insurance · Australia · Health Insurance · Private Health Insurance · Carrier · Healthcare · Claims · Policy Administration · Employee Benefits

## Bupa Australia on APIs.io

Everything profiled for Bupa Australia is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/bupa-australia/](https://apis.io/providers/bupa-australia/)** — or go straight to one of the APIs or properties below.

### APIs (1)

- [Bupa Australia Developer Portal APIs](https://apis.io/apis/bupa-australia/bupa-australia-developer-portal-apis/) — Bupa HI Pty Ltd's Azure API Management developer portal ("Discover Bupa APIs"). The portal lists no APIs or products to anonymous visitors; its Get Started…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Bupa Australia Authentication](https://apis.io/security/bupa-australia/bupa-australia-authentication/)
- [Bupa Australia Domain Security](https://apis.io/security/bupa-australia/bupa-australia-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Bupa Australia Scopes](https://apis.io/scopes/bupa-australia/bupa-australia-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Bupa Australia Plans Pricing](https://apis.io/plans/bupa-australia/bupa-australia-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Bupa Australia Rate Limits](https://apis.io/rate-limits/bupa-australia/bupa-australia-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.bupa.com.au/)
- [Documentation](https://portal.api.bupa.com.au/get-started)
- [Getting started](https://portal.api.bupa.com.au/get-started)
- [API reference](https://portal.api.bupa.com.au/apis)
- [Pricing](https://www.bupa.com.au/health-insurance/quote)
- [Sign up](https://portal.api.bupa.com.au/signin)
- [Support](https://www.bupa.com.au/contact-us)
- [Blog](https://www.bupa.com.au/healthcare-guide)
- [Terms of service](https://www.bupa.com.au/terms-and-conditions)
- [Privacy policy](https://www.bupa.com.au/privacy)

## API Evangelist rating

**Kin Score 23.2** — emerging · rubric 0.24.0 · scored 2026-10-21

| Facet | Score |
|---|---|
| Discoverability | 64.3 |
| Contract quality | 0.0 |
| Contract governance | 18.2 |
| Operational transparency | 0.0 |
| Developer ergonomics | 50.0 |
| Access clarity | 13.2 |

**Agent readiness 8.1** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 29.8** — Insurance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/bupa-australia/](https://apis.io/providers/bupa-australia/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Bupa Australia: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/bupa-australia/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
