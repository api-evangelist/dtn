---
generated: '2026-07-22'
method: generated
name: Query commodity quotes and price history from DTN Market Data
description: >-
  Search symbols, check market hours, and pull quote snapshots and daily/minute/tick
  price history from the DTN (Prophet X) Market Data API.
api: openapi/dtn-financial-market-data-openapi.json
operations: [symbolSearch, getMarketHours, getQuoteSnap, getDailyHistory, getMinuteHistory, getForwardCurve]
---

# Query commodity quotes and price history from DTN Market Data

## Auth
OAuth2 client-credentials Bearer token (`https://api.auth.dtn.com/v1/tokens/authorize`). Production base URL: `https://pxweb.dtn.com`; a Customer Acceptance Testing environment exists at `https://pxwebcat.dtn.com` (see sandbox/dtn-sandbox.yml).

## Steps
1. Resolve instruments with `symbolSearch` (`GET /market_data/symbol-search`) — DTN symbology covers grain, livestock, energy, and equity markets.
2. Check trading sessions with `getMarketHours` (`GET /market_data/metadata/market-hours`) before interpreting quotes as live.
3. Snapshot quotes with `getQuoteSnap` (`GET /market_data/quotes`).
4. Pull history at the resolution you need: `getDailyHistory` (`/market_data/history/daily`), `getMinuteHistory` (`/market_data/history/minute`), or the forward curve with `getForwardCurve` (`/market_data/history/forward-curve`).

## Rules
- Read-only GET surface; no idempotency contract needed.
- Use the CAT environment for integration testing before production.
- Entitlements are contract-based: symbols outside your subscription return authorization errors, not empty data.
