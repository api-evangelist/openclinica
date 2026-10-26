# OpenClinica (openclinica)

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

OpenClinica is a clinical-trial electronic data capture (EDC) and clinical data management platform used to build studies, capture case report form (CRF) data, schedule study events, and manage participants across sites. It ships as a free, open-source Community Edition (LGPL) and as a fully supported, hosted Enterprise Edition. OpenClinica exposes a documented REST web services API - authenticated with OAuth 2.0 bearer tokens - for programmatically adding and updating participants (single and bulk), scheduling and updating study events, and importing and retrieving clinical data. Data is interchanged using the CDISC ODM (Operational Data Model) standard as XML or JSON, so studies remain portable and standards-based.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/openclinica/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/openclinica/refs/heads/main/apis.yml)

## Tags

- Clinical Trials
- Electronic Data Capture
- EDC
- Clinical Data Management
- CDISC ODM
- Healthcare
- Open Source

## Timestamps

- **Created:** 2026-07-05
- **Modified:** 2026-07-05

## APIs

### OpenClinica Authentication API

Obtain an OAuth 2.0 bearer access token by POSTing credentials to the OpenClinica user-service token endpoint. The returned token is passed as an Authorization Bearer header on every subsequent REST API call.

- **Human URL:** [https://docs.openclinica.com/oc4/how-and-when-to-use-apis/](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/)
- **Base URL:** `https://{subdomain}.build.openclinica.io/user-service/api`

#### Tags

- Authentication
- OAuth
- Tokens

#### Properties

- [Documentation](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/)
- [API Reference](https://docs.openclinica.com/3-1-technical-documents/rest-api-specifications/rest-api-specifications-oauth-and-openclinica/)
- [OpenAPI](openapi/openclinica-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### OpenClinica Participants API

Add or update study participants at study or site level, list participants scoped to a study or site, and extract participant contact information. Participants are the human subjects enrolled in a clinical study.

- **Human URL:** [https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-openclinica-4-technical-documentation-participants-add/](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-openclinica-4-technical-documentation-participants-add/)
- **Base URL:** `https://{subdomain}.build.openclinica.io/pages/auth/api`

#### Tags

- Participants
- Subjects
- Enrollment

#### Properties

- [Documentation](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-openclinica-4-technical-documentation-participants-add/)
- [API Reference](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-openclinica-4-technical-documentation-participants-get-participants-study-level-or-site-level/)
- [OpenAPI](openapi/openclinica-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/openclinica.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/openclinica.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### OpenClinica Study Events API

Schedule (create) and update study events for a participant - the visits or time points at which case report forms are collected. Supports single-event operations and bulk create/update of study events.

- **Human URL:** [https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-openclinica-4-technical-documentation-events-create-and-update-single-study-event/](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-openclinica-4-technical-documentation-events-create-and-update-single-study-event/)
- **Base URL:** `https://{subdomain}.build.openclinica.io/pages/auth/api`

#### Tags

- Study Events
- Scheduling
- Visits

#### Properties

- [Documentation](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-openclinica-4-technical-documentation-events-create-and-update-single-study-event/)
- [OpenAPI](openapi/openclinica-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/openclinica.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/openclinica.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### OpenClinica Clinical Data API

Import and retrieve clinical (case report form) data using the CDISC ODM standard as XML or JSON. Retrieval can return study metadata and/or clinical data including audit logs, discrepancy notes (queries), and archived forms, scoped by study, participant, event, and form.

- **Human URL:** [https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-clinicaldata-import-crf-data/](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-clinicaldata-import-crf-data/)
- **Base URL:** `https://{subdomain}.build.openclinica.io/pages/auth/api`

#### Tags

- Clinical Data
- CRF
- CDISC ODM

#### Properties

- [Documentation](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-clinicaldata-import-crf-data/)
- [OpenAPI](openapi/openclinica-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/openclinica.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/openclinica.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### OpenClinica ODM Metadata API

Read the ODM metadata that describes a study's design - event definitions, forms, item groups, and items - qualified by a study OID. The requesting user must have read privileges for the study. Returns CDISC ODM.

- **Human URL:** [https://docs.openclinica.com/3-1-technical-documents/rest-api-specifications/rest-api-specifications-read-openclinica-odm-metadata-rest-service/](https://docs.openclinica.com/3-1-technical-documents/rest-api-specifications/rest-api-specifications-read-openclinica-odm-metadata-rest-service/)
- **Base URL:** `https://{subdomain}.build.openclinica.io/pages/auth/api`

#### Tags

- Metadata
- CDISC ODM
- Study Design

#### Properties

- [Documentation](https://docs.openclinica.com/3-1-technical-documents/rest-api-specifications/rest-api-specifications-read-openclinica-odm-metadata-rest-service/)
- [API Reference](https://docs.openclinica.com/3-1-technical-documents/rest-api-specifications/openclinica-restful-urls/)
- [OpenAPI](openapi/openclinica-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### OpenClinica Bulk Operations API

Add or update a bulk list of participants in a single request and review the outcome of asynchronous bulk actions through the bulk actions log. Used for high-volume participant onboarding and batch operations.

- **Human URL:** [https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-participantsbulk-add-bulk-list-participant-ids/](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-participantsbulk-add-bulk-list-participant-ids/)
- **Base URL:** `https://{subdomain}.build.openclinica.io/pages/auth/api`

#### Tags

- Bulk
- Batch
- Jobs

#### Properties

- [Documentation](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/oc4-participantsbulk-add-bulk-list-participant-ids/)
- [OpenAPI](openapi/openclinica-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [GitHub Organization](https://github.com/OpenClinica)
- [LinkedIn](https://www.linkedin.com/company/openclinica)
- [Website](https://www.openclinica.com)
- [Documentation](https://docs.openclinica.com/oc4/how-and-when-to-use-apis/)
- [Plans](plans/openclinica-plans-pricing.yml)
- [Rate Limits](rate-limits/openclinica-rate-limits.yml)
- [Fin Ops](finops/openclinica-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
