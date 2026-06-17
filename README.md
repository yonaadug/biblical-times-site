# Biblical Times — Public Site

The public-facing pages for [Biblical Times](https://apps.apple.com/) — a weekly devotional iPhone app.

This is the satellite of the main (private) project repo. Its only job is to host:

- `index.html` — landing page
- `privacy.html` — the Privacy Policy URL Apple requires
- `support.html` — the Support URL Apple requires

When v1.1 ships the donation flow, the full Stripe Checkout site (currently in the private repo's `web/` directory) will be deployed separately and the Give links updated.

## One-time setup

```bash
# After creating an EMPTY public repo on GitHub named "biblical-times-site":
cd ~/Documents/GitHub/biblical-times-site
git remote add origin https://github.com/yonaadug/biblical-times-site.git
git push -u origin main
```

Then in the browser:

1. Open https://github.com/yonaadug/biblical-times-site/settings/pages
2. Source: **Deploy from a branch**
3. Branch: **main** · Folder: **/ (root)**
4. Save.

Live URLs after ~30 seconds:

- https://yonaadug.github.io/biblical-times-site/
- https://yonaadug.github.io/biblical-times-site/privacy.html
- https://yonaadug.github.io/biblical-times-site/support.html

Paste those two HTTPS URLs into App Store Connect (Privacy Policy URL, Support URL).

## Local preview

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Editing

Three static HTML files + one CSS file. Edit in place; pushes to `main` deploy automatically via GitHub Pages. No build step.

The visual identity is locked to match the Biblical Times mobile app (cream `#F4EFE4`, maroon `#8A3324`, gold `#B08537`, Lora serif masthead with double-rule).
