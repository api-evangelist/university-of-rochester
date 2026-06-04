# University of Rochester (university-of-rochester)

The University of Rochester is a private research university in Rochester, New York, ranked #236 in the QS World University Rankings 2025. This repository catalogs its public developer and API footprint as an APIs.json provider profile. The university has no single centralized public developer portal; its verifiable programmatic surface is concentrated in library and research-data infrastructure (Figshare-hosted institutional repository and a legacy OAI-PMH interface) plus an active River Campus Libraries GitHub organization.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-rochester/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-rochester-api-evangelist&utm_content=repo

## Type

- Index / Consumer / 3rd-Party

## Tags

Education, Higher Education, University, Research, Library, Institutional Repository, Open Data, United States

## APIs

- **University of Rochester Research Repository (URRR) - Figshare API** — the institution's official research/data repository runs on Figshare, which exposes a public REST API. Docs: https://docs.figshare.com/ · Repository: https://rochester.figshare.com/
- **UR Research Institutional Repository OAI-PMH** — legacy institutional repository with a live OAI-PMH harvesting interface. Endpoint: https://urresearch.rochester.edu/oai/request · Docs: https://urresearch.rochester.edu/

## Plans

See [plans/university-of-rochester-plans-pricing.yml](plans/university-of-rochester-plans-pricing.yml)

## Rate Limits

See [rate-limits/university-of-rochester-rate-limits.yml](rate-limits/university-of-rochester-rate-limits.yml)

## FinOps

See [finops/university-of-rochester-finops.yml](finops/university-of-rochester-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.rochester.edu/
- GitHub: https://github.com/rochester-rcl
- LinkedIn: https://www.linkedin.com/school/university-of-rochester/

## Notes

- No official centralized University of Rochester developer portal was found at review time.
- The Figshare API is a third-party platform API used by the university for URRR, not a university-operated API.
- The legacy UR Research OAI-PMH endpoint was verified live (valid Identify response).
- Probed library discovery and SSO/identity hosts did not resolve publicly and appear gated; no endpoints were fabricated.
- See [review.yml](review.yml) for per-URL HTTP status verification.

## Maintainers

- Kin Lane — kin@apievangelist.com
