# dtn (dtn)

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

The operation intelligence you can rely on to make confident desicions. Empower your business with the best data resource possible.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/dtn/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/dtn/refs/heads/main/apis.yml)

## Timestamps

- **Modified:** 2026-04-28

## APIs

### DTN Weather Conditions API

DTN Weather Conditions API delivers worldwide forecast, current condition, and historical weather data. The API leverages cloud technology and global forecast models to provide validated, continuously calibrated weather data. Supports geospatial queries, time-based filtering, and multi-station requests across over 70,000 weather stations worldwide. OpenAPI/Swagger spec, Postman collections, and release notes available via the developer portal.

- **Human URL:** [https://devportal.dtn.com/catalog/Weather/dtn-weather-conditions-api/documentation](https://devportal.dtn.com/catalog/Weather/dtn-weather-conditions-api/documentation)
- **Base URL:** `https://weather.api.dtn.com/conditions`

#### Tags

- Agriculture
- Climate
- Forecast
- REST
- Weather

#### Properties

- [Documentation](https://devportal.dtn.com/catalog/Weather/dtn-weather-conditions-api/documentation)
- [Reference](https://devportal.dtn.com/catalog/Weather/dtn-weather-conditions-api/documentation)
- [Portal](https://devportal.dtn.com/)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/dtn/refs/heads/main/openapi/dtn-weather-conditions-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### DTN Point Observation API

DTN Point Observation API delivers high-quality weather observation data from weather stations and locations worldwide. Supports near real-time and up to 30 years of historical weather observations. Authentication uses OAuth2 with Client ID and Client Secret. Access tokens obtained via POST to auth.weather.mg/oauth/token, valid for approximately 1 hour, delivered as Bearer tokens.

- **Human URL:** [https://api.weather.mg/api-detail-pages/observation-parameter.html](https://api.weather.mg/api-detail-pages/observation-parameter.html)
- **Base URL:** `https://point-observation.weather.mg`

#### Tags

- Agriculture
- Historical Data
- Observations
- Weather

#### Properties

- [Documentation](https://api.weather.mg/api-detail-pages/observation-parameter.html)
- [Portal](https://api.weather.mg/)

### DTN Point Forecast API

DTN Point Forecast API delivers high-quality weather forecasts for specified locations. Provides hourly and daily forecast data for agriculture, aviation, shipping, and utilities use cases. Uses the same OAuth2 authentication as the Point Observation API.

- **Human URL:** [https://api.weather.mg/api-detail-pages/forecast-parameter.html](https://api.weather.mg/api-detail-pages/forecast-parameter.html)
- **Base URL:** `https://point-forecast.weather.mg`

#### Tags

- Agriculture
- Aviation
- Forecast
- Weather

#### Properties

- [Documentation](https://api.weather.mg/api-detail-pages/forecast-parameter.html)
- [Portal](https://api.weather.mg/)

### DTN Radar Precipitation Forecast API

DTN Radar Precipitation Forecast API provides short-term precipitation forecasts derived from radar data. Supports agricultural, utility, and renewable energy operational planning. Uses OAuth2 authentication with Client ID and Client Secret credentials.

- **Human URL:** [https://api.weather.mg/](https://api.weather.mg/)
- **Base URL:** `https://precipitation-forecast.weather.mg`

#### Tags

- Precipitation
- Radar
- Short-Term Forecast
- Weather

#### Properties

- [Documentation](https://api.weather.mg/)

### DTN Commodity & Market Data API

DTN provides real-time and historical commodity price data, grain and livestock prices, planting condition indices, and market analysis APIs for precision agriculture and commodity trading workflows.

- **Human URL:** [https://www.dtn.com/resources/api-data-integrations/](https://www.dtn.com/resources/api-data-integrations/)
- **Base URL:** `https://api.dtn.com`

#### Tags

- Agriculture
- Commodity Prices
- Grain
- Livestock
- Market Data

#### Properties

- [Documentation](https://www.dtn.com/resources/api-data-integrations/)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/dtnllc)
- [Website](https://www.dtn.com/)
- [OpenAPI](https://raw.githubusercontent.com/api-evangelist/dtn/refs/heads/main/openapi/dtn-weather-conditions-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [JSON Schema](https://raw.githubusercontent.com/api-evangelist/dtn/refs/heads/main/json-schema/dtn-weather-observation-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [J S O N L D Context](https://raw.githubusercontent.com/api-evangelist/dtn/refs/heads/main/json-ld/dtn-context.jsonld)
- [Portal](https://devportal.dtn.com/)
- [Documentation](https://www.dtn.com/resources/api-data-integrations/)
- [Reference](https://api.weather.mg/)
- [Terms of Service](https://www.dtn.com/subscription-agreement-standard-terms-conditions/)
- [Privacy Policy](https://www.dtn.com/wp-content/uploads/2020/04/DTN-External-Privacy-Statement.pdf)
- [Getting Started](https://www.dtn.com/weather/)

## Maintainers

**Email:** kin@apievangelist.com
