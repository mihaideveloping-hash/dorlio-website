# Dorlio website

Public, static marketing site for **Dorlio**, served at **dorlio.com** via GitHub
Pages (deployed straight from the **root** of `main` — no build step, no Actions).

This is a standalone, public repo so the app's source can stay private. The only
content here is the public-facing marketing site and legal pages.

## Files

- `index.html` — landing page (self-contained: inline CSS + a tiny inline script)
- `privacy.html` / `terms.html` — legal pages
- `404.html` — themed not-found page
- `CNAME` — custom domain (`dorlio.com`)
- `assets/` — logo + favicon

## One-time GitHub setup

In this repo: **Settings → Pages → Build and deployment**:

1. **Source:** "Deploy from a branch".
2. **Branch:** `main`, folder **`/ (root)`**, then **Save**.
3. **Custom domain:** `dorlio.com`, then enable **Enforce HTTPS** (after DNS propagates).

DNS at your registrar for `dorlio.com`:

- Four `A` records → `185.199.108.153`, `185.199.109.153`,
  `185.199.110.153`, `185.199.111.153`
- (optional) `AAAA` records → `2606:50c0:8000::153` … `8003::153`
- `www` → `CNAME` → `mihaideveloping-hash.github.io`

**dorlio.app:** point it to redirect to `https://dorlio.com` at your registrar
(GitHub Pages supports only one custom domain per repo).

## Updating the site

Edit the files and push to `main` — GitHub Pages republishes automatically within
a minute or so.

## Keeping legal pages in sync

`privacy.html` / `terms.html` are the public copies. The source of truth lives in
the **private app repo** under `/legal`. When you change one, copy the change to the
other so they don't drift.

## Operator

Dorlio is operated by **MIHAINTELLIGENCE SRL** (Focsani, Romania · CUI 51480000 ·
Trade Register No. J2025019742006). Contact: **contact@mihaintelligence.com**.

App Store and Google Play both require a reachable privacy policy URL
(`https://dorlio.com/privacy.html`), so this site must be live before submission.
