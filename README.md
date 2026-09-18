# DeadWatch plugin releases

Official builds of the DeadWatch site plugins. Each version is a GitHub Release with the package zip and its SHA-256; `manifest.json` on `main` always points at the current version of each plugin.

| Plugin | Slug | For |
|---|---|---|
| Dossier | `dw-dossier` | WordPress — SEO and site intelligence |
| Warden Scanner | `warden-scanner` | WordPress — malware and file-change scanner |
| Inspector | `deadwatch-inspector` | Chrome extension — records and replays browser flows |

A DeadWatch instance reads `manifest.json`, verifies the SHA-256, and mirrors the build so the sites paired with it update from that instance. Nothing here is fetched by a WordPress site directly unless its instance points it here.

Manifest shape:

```json
{ "updated_at": "…", "plugins": { "<slug>": { "version", "package", "sha256", "name", "requires_php", "tested", "changelog", "released_at" } } }
```
