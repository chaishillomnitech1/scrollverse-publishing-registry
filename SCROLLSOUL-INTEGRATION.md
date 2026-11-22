# ScrollSoul API — Integration Record

This surface is part of the ScrollSoul system-wide API network.
**API:** ScrollSoul Music Sync — Omniversal Music Licensing & Distribution API, v1.3.0
**API repo:** https://github.com/chaishillomnitech1/scrollsoul-music-sync
**Docs:** API.md · INTEGRATION.md · PLATFORM_INTEGRATIONS.md (in the API repo)
**Registry:** scrollsoul-registry-manifest.json in
https://github.com/chaishillomnitech1/scrollverse-publishing-registry

## This surface

- **Surface:** scrollverse-publishing-registry (https://github.com/chaishillomnitech1/scrollverse-publishing-registry)
- **Type:** repo
- **Integration tier:** 1 — Linked — see the registry manifest for the live record.
  Tier is claimed here only as high as the registry's verified evidence supports.

## How this surface connects

- **Base URL (documented):** `http://localhost:3000/api` — the API's documented
  address for a local/self-hosted instance.
- **Base URL (planned):** `https://api.scrollsoul.io` — planned in the API repo's
  DOMAIN_CONFIGURATION.md; **not verified live**. Do not treat as reachable.
- **Read the catalog:** `GET /api/music`, `GET /api/music/:id`
- **Licensing & placements:** `GET /api/licensing`, `GET /api/placements`
- **Royalties:** `GET /api/royalties`, `GET /api/royalties/summary/totals`
- **Distribution:** `GET /api/distribution/partners`, `POST /api/distribution/sync/:partnerId`
- **Analytics:** `GET /api/analytics/dashboard`
- **Cross-system:** `GET /api/integration/status`, `GET /api/integration/health`,
  `POST /api/integration/register-system`
- **Health:** `GET /health` (server root)

## Auth

The JS REST API is open as committed (API.md: "Currently, the API is open").
When the operator enables key auth, send `X-API-Key: <key>` (the API's
`apiKeyAuth` middleware also accepts `?api_key=`). The separate `/api/v1`
video API requires `Authorization: Bearer <key>`. Never commit a key to this repo.

## Verify (the API repo's own Quick Test)

    curl http://localhost:3000/
    curl http://localhost:3000/health
    curl http://localhost:3000/api/integration/status

A surface earns Tier 3 (Live Verified) only when one of these calls succeeds
from a real running instance and the date + response are recorded in the registry.

— ScrollSoul API network · registered by the system-wide rollout, 2026-11-22
