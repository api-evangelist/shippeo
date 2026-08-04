# Shippeo (shippeo)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Shippeo is a real-time transportation and multimodal supply-chain visibility platform, giving shippers, carriers, and logistics teams predictive and real-time information for all their deliveries across road, rail, sea, and air. Through its developer portal ([developers.shippeo.com](https://developers.shippeo.com)) Shippeo exposes REST APIs and webhooks so TMS, ERP, and control-tower systems can submit transport orders (tours) for tracking, feed GPS positions, retrieve predictive ETAs, statuses, and milestone events, and subscribe to real-time "Events-out" notifications.

## Access model (read first)

Shippeo is **enterprise, customer-provisioned SaaS**. There is no self-service signup or public pricing for the API. You must have a contracted Shippeo account; API applications and OAuth2 client IDs are then created inside the developer portal, and calls are authenticated with an OAuth2 client-credentials access token presented as an HTTP `Bearer` token. The full Swagger/OpenAPI definitions are behind the portal login.

**What is confirmed vs. modeled in this entry:**

- **Confirmed:** the live API host `https://api.shippeo.com` (its `/health` endpoint responds `{"http-server":{"healthy":true}}`); OAuth2 Bearer authentication; webhook / "Events-out" event delivery; real-time tracking with predictive ETAs across road, rail, sea, and air.
- **Modeled (honest stub):** the individual operation paths and request/response schemas in the OpenAPI and collections. They are derived from Shippeo's public product and marketing documentation because the exact portal Swagger is login-gated. Treat paths as representative, not verified.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/shippeo/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/shippeo/refs/heads/main/apis.yml)

## Tags

- Supply Chain
- Transportation Visibility
- Real-Time Visibility
- Logistics
- Shipment Tracking
- ETA
- Freight
- Supply Chain Visibility
- SaaS

## Timestamps

- **Created:** 2026-07-12
- **Modified:** 2026-07-12

## APIs

### Shippeo Transport Orders API

Submit and manage transport orders (tours) for real-time tracking - origin, destination, stops, references, carrier, and planned times - which Shippeo enriches with predictive ETAs and milestone events.

- **Human URL:** [https://developers.shippeo.com/catalog/all](https://developers.shippeo.com/catalog/all)
- **Base URL:** `https://api.shippeo.com`

#### Tags

- Transport Orders
- Shipment Tracking
- Logistics

#### Properties

- [Documentation](https://developers.shippeo.com)
- [API Reference](https://developers.shippeo.com/catalog/all)
- [OpenAPI](openapi/shippeo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shippeo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shippeo.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shippeo Positions API

Carrier position feed - submit GPS positions (latitude, longitude, timestamp) for vehicles and transports, and retrieve a transport's position history, so Shippeo can track shipments and recompute predictive ETAs.

- **Human URL:** [https://developers.shippeo.com/catalog/all](https://developers.shippeo.com/catalog/all)
- **Base URL:** `https://api.shippeo.com`

#### Tags

- Positions
- Geolocation
- Telematics

#### Properties

- [Documentation](https://developers.shippeo.com)
- [OpenAPI](openapi/shippeo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shippeo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shippeo.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shippeo ETA and Status API

Retrieve Shippeo's predictive ETAs, current statuses, and milestone events (site arrival/departure) for tracked transports - the pull side of the "Events-out" product, blended from carrier positions, routing, and historical patterns.

- **Human URL:** [https://developers.shippeo.com/catalog/all](https://developers.shippeo.com/catalog/all)
- **Base URL:** `https://api.shippeo.com`

#### Tags

- ETA
- Real-Time Visibility
- Events

#### Properties

- [Documentation](https://developers.shippeo.com)
- [OpenAPI](openapi/shippeo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shippeo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shippeo.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shippeo Event Subscriptions (Events-out Webhooks) API

Manage Events-out webhook subscriptions - register callback URLs and event types (status changes, ETA updates, milestone events, carbon-emissions data) so Shippeo POSTs real-time notifications to your systems.

- **Human URL:** [https://developers.shippeo.com/catalog/all](https://developers.shippeo.com/catalog/all)
- **Base URL:** `https://api.shippeo.com`

#### Tags

- Webhooks
- Events
- Real-Time Visibility

#### Properties

- [Documentation](https://developers.shippeo.com)
- [OpenAPI](openapi/shippeo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shippeo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shippeo.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Domain Security](security/shippeo-domain-security.yml)
- [Authentication](authentication/shippeo-authentication.yml)
- [Website](https://www.shippeo.com)
- [Documentation](https://developers.shippeo.com)
- [Sign Up](https://developers.shippeo.com)
- [Status Page](https://shippeo.statuspage.io)
- [LinkedIn](https://www.linkedin.com/company/shippeo)
- [Plans](plans/shippeo-plans-pricing.yml)
- [Rate Limits](rate-limits/shippeo-rate-limits.yml)
- [Fin Ops](finops/shippeo-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
