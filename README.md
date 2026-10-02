# mem0-dashboard

Docker image for the [Mem0](https://github.com/mem0ai/mem0) self-hosted
dashboard (`server/dashboard` in the upstream repo), built from upstream
source and published to GHCR for the [Bumbrel
Store](https://github.com/BubbyWoodz/Bumbrel-Store) (`bubbywoodz-mem0`
package).

- Upstream source is pinned via the `MEM0_SHA` build arg (currently
  `abb81c88e1f7`, mem0 main @ 2026-10-01). Bump it in the Dockerfile and
  push to pick up upstream dashboard changes.
- The image is built by GitHub Actions on every push to `main`
  (plus manual dispatch) and pushed to
  `ghcr.io/bubbywoodz/mem0-dashboard:latest`.
- Runtime config comes from environment, same as upstream:
  `NEXT_PUBLIC_API_URL` (browser-reachable Mem0 API URL),
  `NEXT_PUBLIC_INSTANCE_NAME`, `PORT`, `HOSTNAME`.
