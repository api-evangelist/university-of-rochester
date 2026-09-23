# University of Rochester (university-of-rochester)

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

The University of Rochester is a private research university in Rochester, New York, and an AAU
member, ranked #236 in the QS World University Rankings 2025. This repository catalogs its public
API footprint as an APIs.json provider profile, under the API Evangelist **university pipeline** —
which settles *who operates* each surface before saving any contract, because a university is a
federation of buyers rather than a producer.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-rochester/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-rochester-api-evangelist&utm_content=repo

## Type

- university / Private Research University / Index / Consumer / Public

## Tags

University, Higher Education, Education, United States, New York, Private Research University,
Association of American Universities, Research Repository, Institutional Repository, OAI-PMH,
Identity Federation, Library, Research Computing

## Surfaces

Each entry carries an `x-operator` saying who runs the thing it describes.

### Institution-operated

- **UR Research OAI-PMH Interface** (`x-operator: institution`) — OAI-PMH 2.0 harvesting interface
  for the legacy institutional repository, on the university's own domain, running IR+ — repository
  software the River Campus Libraries wrote and released under Apache 2.0. Verified live
  2026-08-30: `repositoryName` "UR Research", `earliestDatestamp` 2003-07-17, formats `oai_dc`,
  `dcterms`, `marc21`, hierarchical collection sets, spec-correct `badVerb` errors.
  Endpoint: https://urresearch.rochester.edu/oai2 · Source: https://github.com/rochester-rcl/irplus
- **Shibboleth Identity Provider** (`x-operator: institution`) — SAML 2.0 federation metadata
  published at its own entityID, `shibmd:Scope` of `rochester.edu`.
  Endpoint: https://idp.rochester.edu/idp/shibboleth

### Tenant relationships (institution's data, vendor's contract)

- **University of Rochester Research Repository (URRR)** (`x-operator: tenant`) — a Figshare
  tenancy at https://rochester.figshare.com/. The programmatic surface is the generic Figshare v2
  API at `api.figshare.com`, shared by fourteen other institutions in this cohort; that contract is
  Figshare's and is deliberately **not** stored here.
- **Library discovery** (`x-operator: tenant`) — Ex Libris Primo VE, view `01ROCH_INST:UR01`, at
  https://rochester.primo.exlibrisgroup.com/. Catalogue is Rochester's; platform and contract are
  Ex Libris/Clarivate's.

## Conformance (Kin Score `education` regime)

Confirmed by live probe: `oai-pmh`, `shibboleth`, `saml`. See
[conformance/university-of-rochester-conformance.yml](conformance/university-of-rochester-conformance.yml).

## Artifacts

- [openapi/](openapi/) — one description, of the UR Research OAI-PMH endpoint, `method: derived`
  from live probes (API Evangelist authored it; the university does not publish an OpenAPI).
- [examples/](examples/) — verbatim probed responses, `method: probed`.
- [conformance/](conformance/) · [plans/](plans/) · [rate-limits/](rate-limits/) ·
  [finops/](finops/) · [security/](security/)

## Corrections applied 2026-08-30

This profile was first built on 2026-06-03, before the ownership check existed. Two defects were
corrected:

1. **Vendor contract misattributed.** Eleven `apis[]` entries and ten OpenAPI documents were
   recorded as the University of Rochester's. Every one was Figshare's generic contract —
   `info.title` "Figshare altmetric ...", `info.contact` "Figshare Support", `servers[]`
   `https://api.figshare.com/v2`, a host claimed by fourteen other institutions in this cohort.
   The specs and everything derived from them (JSON Schema, JSON Structure, examples, Spectral
   rules, vocabulary, JSON-LD context, OAuth scopes, authentication, agentic-access, capability
   edges, Postman/OpenCollection collections) have been removed. The tenancy itself is kept, as a
   `tenant` entry.
2. **Dead endpoint recorded as verified.** The catalogued OAI-PMH base URL
   `https://urresearch.rochester.edu/oai/request` returns HTTP 200 with an "Unknown Action" HTML
   page — a soft 404 that a status-code-only check reads as live. The working endpoint is `/oai2`.

Two surfaces were **added**: the corrected OAI-PMH endpoint and the Shibboleth/SAML identity
provider, which the June profile had recorded as "did not resolve publicly and appear gated".

**Expect this correction to lower the composite score.** The June figure was substantially
Figshare's contract quality, not Rochester's.

## Notes

- No central University of Rochester developer portal exists; `api.rochester.edu` and
  `data.rochester.edu` do not resolve, and `www.rochester.edu/llms.txt` returns 404.
- Administrative systems (SIS, HR, finance, registrar/course data) are gated behind institutional
  identity and are not publicly documented.
- `rochester.figshare.com` answers HTTP 202 with an empty body behind a bot challenge — live, but
  not readable by probe.
- The River Campus Libraries GitHub organisation (`rochester-rcl`, 112 public repositories, active
  through August 2026) is the clearest evidence of the institution's own engineering output.
- See [review.yml](review.yml) for per-URL HTTP status verification.

## Timestamps

- Created: 2026-06-03
- Modified: 2026-08-30

## Maintainers

- Kin Lane — kin@apievangelist.com
