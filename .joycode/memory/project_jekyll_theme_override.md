---
name: Jekyll github-pages default theme overrides local style.css
description: >-
  Why _site CSS turns into normalize.css on this Jekyll site, and the fix —
  relevant to any missing-CSS/build-output issue
type: project
---

Fact: github-pages gem with no explicit `theme:` in `_config.yml` defaults to `jekyll-theme-primer`. Primer's `assets/css/style.scss` (imports normalize.css) outputs to the SAME path as local `assets/css/style.css`, written last and overwriting it — so the site shows normalize.css instead of custom styles.

**Why:** Confirmed 2026-07-21 via `jekyll build --verbose` (logs: `Theme: jekyll-theme-primer` + duplicate `Writing: .../style.css`). Empty front matter did NOT fix it — front matter controls output, not theme injection at the same path.

**How to apply:** Fix = explicit empty `theme:` line in `_config.yml` (disables gem themes; site has own `_layouts/`, keeps GH Pages compat). If custom CSS vanishes again, run `--verbose` and grep `Theme:` / duplicate `Writing:` before touching front matter. Local env: PowerShell terminal lacks PATH; prefix with `$env:PATH='C:\Ruby33-x64\bin;'+$env:PATH`. Ruby 3.3.x at C:\Ruby33-x64\bin.