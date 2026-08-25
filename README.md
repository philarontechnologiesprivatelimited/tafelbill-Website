# TafelBill — marketing site

The public site at **https://tafelbill.com**. One static page, no build step and
no dependencies: `index.html` carries its own CSS and JavaScript.

## Run it locally

```bash
node .claude/static-server.js
```

Then open http://localhost:3000 (set `PORT` to use another port).

## What's in here

| File | Purpose |
| --- | --- |
| `index.html` | The whole site, including JSON-LD structured data |
| `robots.txt` | Crawler access, including AI search engines, and the sitemap pointer |
| `sitemap.xml` | Submitted to Google Search Console and Bing Webmaster Tools |
| `llms.txt` | Plain-text product summary written for AI assistants |
| `og-image.png` | 1200x630 link preview image |
| `favicon-*.png` | Icons |
| `CNAME` | Custom domain for GitHub Pages |

## Related

- `app.tafelbill.com` — the POS itself, deployed from its own repository
- `admin.tafelbill.com` — internal outlet provisioning, not yet public

## When editing

Absolute URLs in the `<head>` and in the JSON-LD point at `https://tafelbill.com/`.
If the domain ever changes, update the canonical link, the Open Graph and Twitter
tags, `sitemap.xml`, `robots.txt` and `llms.txt` together — a stale canonical
quietly costs you the ranking you were building.
