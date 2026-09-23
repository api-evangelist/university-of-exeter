# University of Exeter (university-of-exeter)

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

The University of Exeter is a public research university in Devon, United Kingdom, and a member of the Russell Group, with campuses at Streatham and St Luke's in Exeter and Penryn in Cornwall. This repository catalogs the institution's public developer and API footprint as an [APIs.json](https://apisjson.org) provider profile. Exeter publishes no developer portal and no OpenAPI. It does operate several real machine-readable surfaces — a Cognito-protected platform API behind the MyExeter app, its own Shibboleth SAML identity provider, a Microsoft Entra ID tenant, a Moodle VLE that is a live LTI 1.3 platform, and a public WordPress REST API on its news site — and it maintains a hand-authored `llms.txt` with explicit guidance for agents.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-exeter/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-exeter-api-evangelist&utm_content=repo

## Type

- university / Public Research University
- Index
- Consumer
- 3rd-Party

## Tags

University, Higher Education, Education, Research, United Kingdom, Russell Group, Identity Federation, Research Repository, Learning Management, Campus Life

## Who operates what

Every surface below carries an `x-operator` in `apis.yml`. A university is a federation of buyers, and most of what looks like an institutional API is a vendor's contract running under an institutional hostname.

### Institution-operated

- **MyExeter Platform API** (`x-operator: institution`) — `https://api.exeter.ac.uk`, an AWS API Gateway deployment in eu-west-2 serving the MyExeter app. Routes for campus events, space occupancy, check-ins, notifications and profile all return `401 {"message":"Unauthorized"}`, while unrouted paths return the gateway's `403 Missing Authentication Token`. OAuth2 against an Exeter-owned AWS Cognito user pool. No documentation, no registration, no specification.
- **Exeter Learning Environment (ELE)** (`x-operator: institution`) — Moodle at `ele.exeter.ac.uk`. Web services are enabled and token-gated, and the site is a live LTI 1.3 Advantage tool platform (`/mod/lti/certs.php` serves an RSA JWKS). The contract is Moodle's, so no spec is saved here.
- **News WordPress REST API** (`x-operator: institution`) — `https://news.exeter.ac.uk/wp-json/`, 20 namespaces, 553 routes, 2,596 posts, open for reads. The only unauthenticated Exeter-hosted API. The contract is WordPress core's.

### Federation (institution-operated by definition)

- **Shibboleth Identity Provider** — entityID `https://elibrary.exeter.ac.uk/idp/shibboleth`, publishing its own SAML 2.0 metadata and served as signed metadata by both the UK Access Management Federation MDQ and InCommon's MDQ via eduGAIN.
- **Microsoft Entra ID tenant** — `912a5d77-fb98-4eee-af32-1334d8f04a53`, with live OIDC discovery and WS-Fed/SAML federation metadata; `mytimetable.exeter.ac.uk` federates into it.

### Tenant (Exeter's data, a vendor's contract)

- **Open Research Exeter (ORE)** — a **Figshare** tenancy. `ore.exeter.ac.uk` is a CNAME to `proxy-eu-01.figshare.com`; Exeter's items carry Figshare `group_id` 58481 and handle prefix `10779/exe`. It is **not** a DSpace repository — see Corrections.
- **Exeter Experts directory** — a **Symplectic Elements Discovery** tenancy; `experts.exeter.ac.uk` is a CNAME to `uoe.discovery.symplectic.org`.

### Registry membership

- **DataCite** — provider `VUEX`, repository client `BL.EXETER` ("Open Research Exeter", 450 DOIs, re3data `10.17616/R3033Z`).
- **Crossref** — member `27616`, University of Exeter Press, prefixes `10.58182` and `10.47788`.
- **ROR** — `https://ror.org/03yghzc09`.

## Corrections (2026-09-01)

The June 2026 profile described ORE as a DSpace repository and recorded two endpoints for it — an OAI-PMH interface at `/repository/oai/request` and a DSpace 7 REST API at `/server/api`. Both were inferred from DSpace platform defaults rather than observed; ORE is a Figshare tenancy and neither endpoint exists. Both entries have been removed and replaced with a tenancy record. The MyExeter entry's `baseURL` pointed at `m.exeter.ac.uk`, which is the Flutter web client, not the API; it now points at `api.exeter.ac.uk`. The plans, rate-limit and FinOps artifacts asserted free "library, repository, course and open-metadata" APIs and throttled "OAI-PMH, IIIF and library" harvesting endpoints — Exeter operates none of those — and have been corrected and provenance-stamped.

## Artifacts

- [conformance/university-of-exeter-conformance.yml](conformance/university-of-exeter-conformance.yml) — probed conformance against the `education` regime standards (LTI, Shibboleth, SAML, DataCite and Crossref confirmed; OAI-PMH, SCIM, OneRoster, Ed-Fi, Caliper and QTI probed negative)
- [authentication/university-of-exeter-authentication.yml](authentication/university-of-exeter-authentication.yml)
- [errors/university-of-exeter-errors.yml](errors/university-of-exeter-errors.yml)
- [plans/university-of-exeter-plans-pricing.yml](plans/university-of-exeter-plans-pricing.yml)
- [rate-limits/university-of-exeter-rate-limits.yml](rate-limits/university-of-exeter-rate-limits.yml)
- [finops/university-of-exeter-finops.yml](finops/university-of-exeter-finops.yml)
- [json-ld/university-of-exeter-context.jsonld](json-ld/university-of-exeter-context.jsonld)
- [security/university-of-exeter-domain-security.yml](security/university-of-exeter-domain-security.yml)

No `openapi/` directory exists in this repository, and that is correct: Exeter publishes no OpenAPI, and the contracts behind its readable surfaces belong upstream to Moodle, WordPress, Shibboleth, Figshare and Symplectic.

## Timestamps

- Created: 2026-06-03
- Modified: 2026-09-01

## Common Properties

- Website: https://www.exeter.ac.uk/
- llms.txt: https://www.exeter.ac.uk/llms.txt
- GitHub: https://github.com/Uni-of-Exeter
- LinkedIn: https://www.linkedin.com/school/university-of-exeter/
- Twitter: https://twitter.com/UniofExeter
- Blog: https://news.exeter.ac.uk/
- Privacy: https://www.exeter.ac.uk/about/oursite/privacy/
- Copyright and disclaimer: https://www.exeter.ac.uk/about/oursite/copyright/
- Accessibility: https://www.exeter.ac.uk/about/oursite/accessibility/
- Authentication: https://libguides.exeter.ac.uk/eresources/shibboleth

## Notes

This profile reflects only publicly confirmable surfaces; no endpoints were fabricated and every status code cited was observed on 2026-09-01. Exeter has no public developer portal (`developer.exeter.ac.uk` and `developers.exeter.ac.uk` do not resolve) and no self-service credential for any surface it operates. `ore.exeter.ac.uk` sits behind an AWS WAF challenge that returns HTTP 202 with a zero-length body to every client, so nothing on it is readable; the WAF challenge page itself is what identified the host as Figshare. `srs.exeter.ac.uk` runs Tribal SITS:Vision and `libguides.exeter.ac.uk` is a Springshare tenancy; neither exposes a public API and neither is recorded as one.

## Maintainers

- Kin Lane — kin@apievangelist.com
