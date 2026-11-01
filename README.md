# University of Exeter

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

The University of Exeter is a public research university in Devon, United Kingdom, and a member of the Russell Group, with campuses at Streatham and St Luke's in Exeter and Penryn in Cornwall. It operates no public developer portal and publishes no OpenAPI, and most of what appears to be an Exeter API is a vendor platform running under an exeter.ac.uk hostname. What Exeter genuinely operates is: a Cognito-protected platform API at api.exeter.ac.uk behind the MyExeter app (campus events, space occupancy, notifications, profile - every route returns 401 without a token and none are documented); its own Shibboleth SAML identity provider, published in both the UK Access Management Federation and InCommon/eduGAIN metadata; a Microsoft Entra ID tenant fronting SSO for timetabling; a Moodle VLE at ele.exeter.ac.uk that is a live LTI 1.3 platform and exposes Moodle's own web-service endpoint; and a public WordPress REST API on its news site. Its research repository Open Research Exeter is a Figshare tenancy, and its expert profiles are a Symplectic Elements tenancy - neither contract is Exeter's engineering. Exeter also maintains a hand-authored llms.txt with explicit guidance for agents, which is rare in this cohort.

**Areas:** University · Higher Education · Education · Research · United Kingdom · Russell Group · Identity Federation · Research Repository · LMS · Campus Life

## University of Exeter on APIs.io

Everything profiled for University of Exeter is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/university-of-exeter/](https://apis.io/providers/university-of-exeter/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [MyExeter Platform API](https://apis.io/apis/university-of-exeter/myexeter-platform-api/) — api.exeter.ac.uk is an institution-operated AWS API Gateway deployment in eu-west-2 that serves the MyExeter student app (the Flutter PWA at m.exeter.ac.uk…
- [University of Exeter Shibboleth Identity Provider](https://apis.io/apis/university-of-exeter/shibboleth-idp/) — Exeter operates its own SAML 2.0 Shibboleth identity provider with entityID https://elibrary.exeter.ac.uk/idp/shibboleth. The IdP publishes its own metadata…
- [University of Exeter Microsoft Entra ID Tenant](https://apis.io/apis/university-of-exeter/entra-id-tenant/) — Exeter runs a Microsoft Entra ID tenant (912a5d77-fb98-4eee-af32-1334d8f04a53) used for staff and student single sign-on; mytimetable.exeter.ac.uk redirects…
- [Exeter Learning Environment (ELE) - Moodle Web Services and LTI 1.3 Platform](https://apis.io/apis/university-of-exeter/ele-moodle/) — ELE is Exeter's virtual learning environment, a Moodle deployment on the institution's own host ele.exeter.ac.uk. Two machine-readable surfaces are live:…
- [University of Exeter Website (WordPress REST)](https://apis.io/apis/university-of-exeter/news-exeter-ac-uk-website-wordpress-rest/) — The public WordPress REST API (wp-json) of the University of Exeter website at news.exeter.ac.uk: the route index of the site's content management system,…
- [Open Research Exeter (ORE) - Figshare Tenancy](https://apis.io/apis/university-of-exeter/ore-figshare-tenancy/) — Open Research Exeter is Exeter's institutional research repository and it is a Figshare tenancy, not institution-run software. ore.exeter.ac.uk is a CNAME…
- [Exeter Experts Directory - Symplectic Elements Discovery Tenancy](https://apis.io/apis/university-of-exeter/experts-symplectic-tenancy/) — experts.exeter.ac.uk is the university's staff expertise, publications and research output directory, and Exeter's own llms.txt names it as the…
- [DataCite Membership and Open Research Exeter DOI Registration](https://apis.io/apis/university-of-exeter/datacite-membership/) — Exeter is a registered DataCite member - provider symbol VUEX, name "University of Exeter", memberType consortium_organization, rorId…
- [University of Exeter Press Crossref Membership](https://apis.io/apis/university-of-exeter/crossref-membership/) — The university's publishing arm is a Crossref member - member id 27616, primary name "University of Exeter Press" - registering DOIs under prefixes 10.58182…
- [University of Exeter ROR Registration](https://apis.io/apis/university-of-exeter/ror-registration/) — Exeter is registered in the Research Organization Registry with ROR identifier https://ror.org/03yghzc09, the identifier DataCite carries on the…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [University Of Exeter Context](https://apis.io/jsonld/university-of-exeter/university-of-exeter-context/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [University Of Exeter Authentication](https://apis.io/security/university-of-exeter/university-of-exeter-authentication/)
- [University Of Exeter Domain Security](https://apis.io/security/university-of-exeter/university-of-exeter-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [University Of Exeter Plans Pricing](https://apis.io/plans/university-of-exeter/university-of-exeter-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [University Of Exeter Rate Limits](https://apis.io/rate-limits/university-of-exeter/university-of-exeter-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [University Of Exeter Finops](https://apis.io/finops/university-of-exeter/university-of-exeter-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.exeter.ac.uk/)
- [Support](https://www.exeter.ac.uk/contact/)
- [Blog](https://news.exeter.ac.uk/)
- [Terms of service](https://www.exeter.ac.uk/about/oursite/copyright/)
- [Privacy policy](https://www.exeter.ac.uk/about/oursite/privacy/)
- [GitHub](https://github.com/Uni-of-Exeter)

## API Evangelist rating

**Kin Score 26.8** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 69.6 |
| Contract quality | 14.3 |
| Contract governance | 18.2 |
| Operational transparency | 7.9 |
| Developer ergonomics | 28.6 |
| Access clarity | 26.3 |

**Agent readiness 3.1** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
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

**Regulatory alignment 32.4** — Education & Research

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/university-of-exeter/](https://apis.io/providers/university-of-exeter/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for University of Exeter: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/university-of-exeter/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
