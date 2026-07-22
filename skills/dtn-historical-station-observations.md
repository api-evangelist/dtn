---
generated: '2026-07-22'
name: Pull historical station observations from DTN
method: generated
description: >-
  Find weather stations and pull near-real-time or historical observations
  (up to 30 years) from the DTN Observation API.
api: openapi/dtn-observation-api-openapi.json
operations: [get_stations_v2_observations_stations_get, get_parameters_v2_observations_parameters_get, get_observations_v2_observations_get]
---

# Pull historical station observations from DTN

## Auth
Same OAuth2 client-credentials flow as all DTN APIs: Bearer token from `https://api.auth.dtn.com/v1/tokens/authorize`. Base URL: `https://obs.api.dtn.com`.

## Steps
1. Locate stations with `get_stations_v2_observations_stations_get` (`GET /v2/observations/stations`) — filter geographically (bounding box / radius) to get station ids near your point of interest.
2. Enumerate the parameters each station reports with `get_parameters_v2_observations_parameters_get` (`GET /v2/observations/parameters`).
3. Fetch observations with `get_observations_v2_observations_get` (`GET /v2/observations`) using the station ids, an observed time interval (ISO 8601 `start/end`), and a parameter subset.

## Rules
- Respect the documented `limit` cap on observation requests; page by narrowing the time window rather than assuming cursors.
- Multiple stations can be queried in one request (pipe-separated) — prefer batching over per-station loops.
- Read-only GET surface; 429 signals plan-based rate limiting.
