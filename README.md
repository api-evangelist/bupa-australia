# Bupa Australia (bupa-australia)

Bupa Australia is the Australian market unit of the UK-headquartered Bupa group and one of the country's largest private health insurers, trading as Bupa HI Pty Ltd (ABN 81 000 057 590). It writes hospital and ancillary "extras" cover, overseas visitor and overseas student health cover, and corporate health plans — and, unusually for a carrier, also owns the provision that consumes those benefits through Bupa Dental, Bupa Optical, Bupa Medical Visa Services and Bupa Aged Care.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/bupa-australia/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/bupa-australia/refs/heads/main/apis.yml)

## Tags

- Insurance
- Australia
- Health Insurance
- Private Health Insurance
- Carrier
- Healthcare
- Claims
- Policy Administration
- Employee Benefits
- Partner Gated

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

None listed.

Bupa Australia publishes no public, self-serve API. It does run a **real first-party developer portal** — and the portal is empty.

- **[portal.api.bupa.com.au](https://portal.api.bupa.com.au/) — live (HTTP 200), first-party, and gated.** It is an Azure API Management managed portal whose meta author tag reads *"Bupa HI Pty Ltd ABN 81 000 057 590"*, so it belongs to the Australian entity rather than the UK group. But `/apis` and `/products` both return HTTP 200 and render bare "APIs: List" and "Products: List" headings with **no catalog** for anonymous visitors, and `config.json` points the portal at `https://management.api.internal.bupa.com.au/...` (APIM service `banzprodapim01`), a host that does not resolve publicly. The [Get Started](https://portal.api.bupa.com.au/get-started) page routes every step through a human team: *"Contact the Bupa Integration Fabric Team with your interest to get access to our API specifications."*
- **`api.bupa.com.au` — 502 to everyone.** The custom gateway host resolves behind Imperva but returns HTTP 502 to anonymous callers on every path probed, including `/openapi.json`, `/swagger.json`, `/api-docs`, `/graphql` and `/.well-known/openid-configuration`.
- **Nothing on the marketing estate.** `developer.`, `developers.`, `docs.`, `apis.` and `sandbox.bupa.com.au` do not resolve. `/developers`, `/developer`, `/api`, `/apis`, `/partners`, `/partner` and `/integrations` all return 404. The three public sitemaps hold **810 URLs and not one developer, API or SDK page**.

### What Bupa Australia's counterparties actually integrate with

The honest finding for this record is that the real integration surface is not an API at all:

- **Ancillary providers claim through HICAPS and HealthPoint terminals.** The [for-providers](https://www.bupa.com.au/for-providers) page states Bupa "has engaged HICAPS and HealthPoint to activate their adjusted charge processing feature".
- **Hospital providers use ECLIPSE.** Patient eligibility checking and hospital claiming run over the national Services Australia channel, reached from Bupa's own [hospital providers](https://www.bupa.com.au/for-providers/hospital) page at `https://eclipse.civica.com.au/ECFWeb/login` — Civica's Electronic Claim Form web client. Registration is a **PDF form**.
- **The Bupa Partner Portal is a login wall reached by paper.** [partner.bupa.com.au](https://partner.bupa.com.au/) is a Microsoft Dynamics 365 Power Pages portal that 302s to Azure AD B2C, and access is requested by downloading and returning "Bupa Partner Portal Access Form.pdf".

## Sector signals

- **ACORD posture:** *no ACORD reference found.* No mention of ACORD, AL3, ACORD XML, NGDS or ACORD certification appears on `www.bupa.com.au` or on any page of the developer portal. Consistent with the line of business — private health insurance and healthcare provision, not P&C or life — and with the market, which has no IVANS-style agency-download plumbing. The standards that actually carry Bupa Australia's transactions are domestic health-claiming ones (ECLIPSE, HICAPS, HealthPoint), none of which is ACORD and none of which Bupa publishes.
- **Quote / bind / issue / FNOL:** none publicly exposed. Quoting is the consumer web funnel and gated corporate channels; claiming runs over ECLIPSE, terminals, the myBupa app, and in several paths still PDF forms.
- **Auth model:** OAuth2 authorization code via **Azure AD B2C** (`partnerlogin.bupa.com.au`, tenant `52bddae3-…`, policy `B2C_1A_PROD_01_SIGNUP_SIGNIN`) guards the partner portal, and OAuth2 via **Microsoft Entra ID** (tenant `fee9c112-…`, region scope OC) plus a B2C path guards developer-portal sign-in. Both discovery documents were fetched anonymously at HTTP 200. Azure APIM subscription keys are implied by the portal copy but are not documented publicly.
- **CDR:** Australia designated the Consumer Data Right for general insurance and then deferred it. A direct query of the [CDR participant register](https://api.cdr.gov.au/cdr-register/v1/all/data-holders/brands/summary) (HTTP 200) returned **203 data-holder brands, banking and energy only — no insurance sector and no Bupa brand.** The seam that made Australian banking legible stops before insurance.
- **Webhooks / events / Postman / GraphQL / gRPC / public source:** none found. No GitHub organization exists under `bupa`, `bupa-australia`, `bupaanz` or `bupa-anz`.
- **OpenAPI harvested:** 0 specifications. No `openapi/` directory is included, because nothing real was available to save.

Full probe log, HTTP statuses and provenance are in [review.yml](review.yml).

## Links

- [Website](https://www.bupa.com.au/)
- [About Bupa Australia](https://www.bupa.com.au/about-us)
- [Bupa Developer Portal](https://portal.api.bupa.com.au/)
- [Get Started](https://portal.api.bupa.com.au/get-started)
- [Bupa Partner Portal](https://partner.bupa.com.au/)
- [For Providers](https://www.bupa.com.au/for-providers)
