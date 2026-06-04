# University of Exeter (university-of-exeter)

The University of Exeter is a public research university in Devon, United Kingdom, and a member of the Russell Group, ranked #169 in the QS World University Rankings 2025. This repository catalogs the institution's public developer and API footprint as an [APIs.json](https://apisjson.org) provider profile. Exeter does not publish a dedicated developer portal; its confirmed surfaces are largely institutional — a DSpace research repository (Open Research Exeter), federated SAML identity, the MyExeter mobile backend, and an official GitHub organization.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-exeter/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-exeter-api-evangelist&utm_content=repo

## Type

- Index
- Consumer
- 3rd-Party

## Tags

Education, Higher Education, University, Research, Open Data, Repository, Identity, United Kingdom

## APIs

- **Open Research Exeter (ORE) OAI-PMH** — DSpace OAI-PMH metadata harvesting interface for the institutional research repository. Docs: https://www.exeter.ac.uk/research/researchdatamanagement/after/discovery/ (repository: https://ore.exeter.ac.uk/repository/)
- **Open Research Exeter (ORE) DSpace REST API** — Standard DSpace REST API for communities, collections, items, and bitstreams. Docs: https://www.exeter.ac.uk/research/researchdatamanagement/after/discovery/
- **Shibboleth Identity Provider (SAML SSO)** — Federated SAML single sign-on for library e-resources and federated services. Docs: https://libguides.exeter.ac.uk/eresources/shibboleth
- **MyExeter Mobile App Backend** — Private, undocumented mobile-app APIs powering the official student app. Docs: https://www.exeter.ac.uk/students/myexeter/

## Plans

- [plans/university-of-exeter-plans-pricing.yml](plans/university-of-exeter-plans-pricing.yml)

## Rate Limits

- [rate-limits/university-of-exeter-rate-limits.yml](rate-limits/university-of-exeter-rate-limits.yml)

## FinOps

- [finops/university-of-exeter-finops.yml](finops/university-of-exeter-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.exeter.ac.uk/
- GitHub: https://github.com/Uni-of-Exeter
- Source Code: https://github.com/Uni-of-Exeter
- LinkedIn: https://www.linkedin.com/school/university-of-exeter/
- Twitter: https://twitter.com/UniofExeter
- Authentication: https://libguides.exeter.ac.uk/eresources/shibboleth

## Notes

This profile reflects only publicly confirmable surfaces; no endpoints were fabricated. The University of Exeter has no dedicated public developer portal or packaged API program. The Open Research Exeter (ORE) repository host responds but sits behind a bot-mitigation gateway (HTTP 202 with empty bodies on OAI-PMH/REST probes), so those DSpace endpoints are documented per platform defaults rather than verified live. The Shibboleth/SAML identity service and MyExeter mobile backend are gated and not self-service developer APIs. The official GitHub organization (Uni-of-Exeter) was verified via the GitHub API and publishes some middleware (WSO2 Micro Integrator) and research code.

## Maintainers

- Kin Lane — kin@apievangelist.com
