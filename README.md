# weai-web

Landing page for **WeAI** — the private, peer-to-peer AI node for macOS.

Live at **https://avantigroupai.github.io/weai-web/**

## What is here

| File | |
|---|---|
| `index.html` | the landing page — version, size and SHA-256 of the current build are written into it by `scripts/update-website.sh` in the app repo |
| `docs.html` | the documentation page |
| `release.json` | machine-readable release metadata (version, build, sha256, size, notarized) |
| `.nojekyll` | serve the files as-is; no Jekyll build |

The DMG is **not** stored here. Downloads point at
[avantigroupai/WeAI-releases](https://github.com/avantigroupai/WeAI-releases/releases), so this
repository stays small and the page never has to be re-pointed at a new file.

## Updating after a release

In the app repo, `./scripts/release.sh` then `./scripts/update-website.sh` refresh
`website/index.html` and `website/release.json`. Publish the new DMG to `WeAI-releases` (as both
`WeAI-<version>.dmg` and `WeAI.dmg`), then copy the two refreshed files here and push — the
download links need no change, because they use the `releases/latest/download/` alias.
