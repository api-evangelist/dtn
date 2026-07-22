---
generated: '2026-07-22'
method: generated
name: Get current conditions and forecast weather from DTN
description: >-
  Authenticate with OAuth2 client credentials and retrieve current, forecast,
  or historical weather for a location from the DTN Weather Conditions API,
  selecting only the fields you need.
api: openapi/dtn-weather-conditions-api-openapi.json
operations: [weatherConditions, weatherParameters, weatherCodes]
---

# Get current conditions and forecast weather from DTN

## Auth
1. Obtain a Bearer token via OAuth2 client credentials: `POST https://api.auth.dtn.com/v1/tokens/authorize` with your Client ID/Secret from the DTN Developer Portal (devportal.dtn.com). Tokens are short-lived; cache and refresh.
2. Send `Authorization: Bearer <token>` on every call.

## Steps
1. Discover valid parameter names first with `weatherParameters` (`GET /v2/conditions/parameters`) — field names are long-form with units embedded (e.g. `airTemperatureInCelsius`, `windSpeedInMeterPerSecond`).
2. Call `weatherConditions` (`GET /v2/conditions`) with:
   - a location (lat,lon pair or station id),
   - an ISO 8601 interval for forecast/historical windows (`startISO8601/endISO8601`),
   - `fields=` a comma-separated subset (keeps payloads small — the API supports sparse field selection),
   - `units=US|SI` (default SI).
3. Decode `weatherSymbol` and other coded values via `weatherCodes` (`GET /v2/conditions/codes`).

## Rules
- Read-only surface: all operations are GET; there is no idempotency-key contract (see conventions/dtn-conventions.yml).
- Expect `429` when exceeding your contracted rate plan (rate-limits/dtn-rate-limits.yml); back off and retry.
- Errors use a `code`/`message` envelope (errors/dtn-problem-types.yml).
- Historical data extends back 10 years (from 2013-01-01) per the v2.1.0 release notes.
