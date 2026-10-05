# Sugar Syrup Calculator

[![Latest release](https://img.shields.io/github/v/release/H4W9/syrup-calculator?style=flat&color=e0a100&label=release&cacheSeconds=1800)](https://github.com/H4W9/syrup-calculator/releases/latest)
[![Total downloads](https://img.shields.io/github/downloads/H4W9/syrup-calculator/total?style=flat&color=e0a100&label=downloads&cacheSeconds=1800)](https://github.com/H4W9/syrup-calculator/releases)
[![Live demo](https://img.shields.io/badge/live-demo-e0a100?style=flat&logo=githubpages&logoColor=white)](https://h4w9.github.io/syrup-calculator/)

A single-file HTML tool for mixing sugar syrup (e.g. for bee feeding). Pick a
sugar:water ratio by weight, enter any one of sugar, water, or finished syrup,
and the other two are calculated. Imperial (lb / gal) and metric (kg / L) are
supported, and you can add your own custom ratios.

**Live demo:** https://h4w9.github.io/syrup-calculator/

**Download the latest release:**
https://github.com/H4W9/syrup-calculator/releases/latest/download/syrup-calculator.html

## Open it

Double-click **`syrup-calculator.html`** — it runs in any browser. No install,
no internet needed.

## Privacy

Everything runs in your browser. There are no network calls and no accounts.
Custom ratios, the selected ratio, and the unit choice are saved in the
browser's `localStorage` on that device only.

## Releases & deployment

GitHub Pages serves the site from the `main` branch
(**Settings → Pages → "Deploy from a branch": `main` / root**), so every push to
`main` updates the live demo.

To cut a release:

```bash
# 1. Bump the version in syrup-calculator.html:
#      <meta name="app-version" content="1.0.1">
# 2. Commit it to main, then:
git tag v1.0.1
git push origin v1.0.1
```

Pushing a `vX.Y.Z` tag runs `.github/workflows/release.yml`, which stamps the tag
version into the page and publishes a GitHub Release with `syrup-calculator.html`
and `syrup-calculator.zip` attached.

## Files

| File | What it is |
|------|-----------|
| `syrup-calculator.html` | The entire tool — HTML, CSS, and JS in one file |
| `apple-touch-icon.png` | Home-screen icon used when saved to an iPhone/iPad |
| `index.html` | Tiny redirect to the tool, so Pages serves it at the repo root |
| `.github/workflows/release.yml` | CI: tag → GitHub Release |
| `README.md` | This document |
