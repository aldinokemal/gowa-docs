# GOWA documentation

This repository contains the Mintlify guides and API reference for [GOWA](https://github.com/aldinokemal/go-whatsapp-web-multidevice).

## Run locally

Install the Mintlify CLI, then run it from this directory.

```bash
npm install -g mint
mint dev
```

Open the local URL printed by the CLI. The default is `http://localhost:3000`.

## Validate changes

```bash
mint validate
mint broken-links
```

## Maintain the API reference

`docs.json` generates endpoint pages from `openapi.yml`. Start with GOWA's `docs/openapi.yaml`, then verify changed routes, DTOs, validation, and response envelopes against the implementation. The current local spec also documents the merged `/send/interactive` route, which is absent from the source spec at the audited revision.

The guides track merged `main`, including changes after v9.7.0. Do not describe open PRs as available features. Release binaries and pinned container tags may lag behind these docs.

Use root-relative links without file extensions. Add new guide pages to `docs.json`, and keep runnable examples consistent with authentication and device selection.

## Publish

Open a pull request against `main`. Merging to the connected deployment branch triggers Mintlify publishing. A successful local preview does not confirm a production deployment.
