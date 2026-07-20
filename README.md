# loom-legal

Public legal + support pages for the **Loom** iOS app, served by GitHub Pages.

Live at <https://derekvallar.github.io/loom-legal/>

| Page | URL |
| --- | --- |
| Privacy Policy | `/loom-legal/privacy` |
| Terms of Service | `/loom-legal/terms` |
| Community Guidelines | `/loom-legal/guidelines` |
| Support | `/loom-legal/support` |

## Why this repo is separate and public

GitHub Pages on a private repo requires a paid plan, and App Review must be able to fetch the
privacy policy without a login. The Loom app repo stays private; only these documents are public.

## Editing

Each page is Markdown with a pinned `permalink` in its front matter. **Don't change the
permalinks** — the iOS app hardcodes these URLs in `Loom/Loom/Utils/LegalLinks.swift`, and App
Store Connect stores the privacy and support URLs.

Cross-links between pages use `{{ site.baseurl }}` rather than hardcoded paths.

## Moving to a custom domain later

1. Add a `CNAME` file containing the domain.
2. Point DNS at GitHub Pages.
3. Set `baseurl: ""` in `_config.yml`.
4. Update the three constants in `LegalLinks.swift` and the URLs in App Store Connect.

Page paths stay identical, so nothing else changes.

## Note

These documents have not been reviewed by legal counsel.
