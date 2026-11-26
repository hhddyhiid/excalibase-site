# pulse

A small personal page: a short note about a side project, a clock that arrives
over a WebSocket, and two plain endpoints for uptime checks.

    node server.js        # listens on $PORT (default 8080)

- `GET /` — the page
- `GET /health` — `ok`
- `GET /api/status` — uptime, host, node version, last observed egress address
- `WS /live` — pushes `{hh, up}` once a second

No dependencies beyond Node's core modules.

Built as a container image by `.github/workflows/build.yml` and pulled as
`ghcr.io/hhddyhiid/excalibase-site:latest`.
