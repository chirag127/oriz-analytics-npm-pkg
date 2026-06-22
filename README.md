# @chirag127/oriz-analytics

[![npm](https://img.shields.io/npm/v/@chirag127/oriz-analytics.svg)](https://www.npmjs.com/package/@chirag127/oriz-analytics)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

Single wrapper around Cloudflare Web Analytics + GA4 + Microsoft Clarity + Sentry. One init() call, four backends, zero PII.

## Install

```bash
pnpm add @chirag127/oriz-analytics
```

## Status

v0.1.0 is a slug-reservation stub. Real implementation lands when oriz apps consume it.

## Planned API

- `init({ cloudflare, ga4, clarity, sentry })` — one call, four backends; each provider is optional.
- `track(event, props)` — fan-out to every configured backend with PII stripping.
- `identify(userId)` — hashed before being forwarded; never raw.
- Server-side GA4 Measurement Protocol for cookieless tracking.
- Built-in `Do Not Track` and GPC respect; no-ops when consent is denied.

## License

MIT (c) 2026 Chirag Singhal
