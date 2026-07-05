# OpenClinica (openclinica)

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
