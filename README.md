# Om Kumbhar — portfolio

Static site, no build step, no dependencies. Drop these files in the repo root and GitHub Pages serves them as-is.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole site — markup, styles and scripts in one file |
| `om-kumbhar.webp` | Portrait, 600×600 |
| `om-kumbhar-og.jpg` | Link preview card, 1200×630 (WhatsApp, LinkedIn, X) |
| `404.html` | Not-found page, served automatically by GitHub Pages |
| `robots.txt` | Points crawlers at the sitemap |
| `sitemap.xml` | One entry — update `lastmod` when you change the page |
| `.nojekyll` | Stops GitHub running Jekyll over the files |

## Deploy

1. Copy everything into the repo root, replacing the old `index.html`.
2. Commit and push to `main`.
3. Settings → Pages → Source: `main`, folder `/ (root)`.
4. Wait a minute, then hard-refresh (Ctrl/Cmd + Shift + R) — Pages caches aggressively.

## Before you publish

- [ ] Photo loads. If it doesn't, the frame shows "OK" initials instead of a broken image.
- [ ] Paste your Google Search Console verification tag — there's a comment in `<head>` marking the spot.
- [ ] Check it on a phone. The portrait moves above the text under 860px.
- [ ] Paste the URL into a WhatsApp message to yourself and confirm the preview card renders.

## Changing the URL later

Every URL in `index.html`, `404.html` and `sitemap.xml` is the full address. To move:

```
find & replace:  omskumbhar1.github.io/OM-KUMBHAR  →  your new domain
```

For a custom domain, add a file named `CNAME` (no extension) containing just the domain, e.g. `omkumbhar.com`, then point the DNS at GitHub Pages. Don't add this file until the domain actually exists — a wrong `CNAME` takes the site offline.

## Ranking on "Om Kumbhar"

On-page work is done. The rest is off-page, in order of impact.

**1. Fix the address.** `omskumbhar1.github.io/OM-KUMBHAR/` is a project subpath with uppercase in it — the weakest possible URL for a name search.
- Free: rename the repo to exactly `omskumbhar1.github.io`, and the site serves from the root.
- Better: register `omkumbhar.com`. An exact-match name domain is the strongest single signal for a name query.

**2. Link to it from everything you already own.** Google needs corroboration that this page is you.
- [ ] GitHub profile → Website field
- [ ] GitHub profile README (repo named `omskumbhar1`)
- [ ] YouTube channel → Links
- [ ] Instagram bio
- [ ] **trovro.com → a founder line linking back.** A link from a domain you own outweighs the rest combined.
- [ ] LinkedIn. It ranks near-automatically on names, so own that result rather than lose it to someone else with your name.

**3. Get indexed.**
- [ ] Google Search Console → add property → submit `sitemap.xml` → URL Inspection → Request Indexing
- [ ] Bing Webmaster Tools (two minutes, and it covers DuckDuckGo)

Expect four to twelve weeks for a name query to settle. It moves faster once Trovro is public on Play — a Play Store listing naming you as developer is an entity signal you can't manufacture.

Don't chase "web developer Mumbai" or similar. Those queries belong to agencies and directories with years of backlinks, and the effort is better spent elsewhere.

## Editing content

**Add a project** — copy an `<article class="entry">` block in the Work section and edit it. Entries run newest first. The `<span class="status">` label is free text; add `class="status live"` to give it the yellow background, which is currently only on Trovro.

**The yellow highlight** — wrap text in `<span class="mark" data-mark>`. It draws itself when scrolled into view. Used three times on purpose; more and it stops meaning anything.

**Colours and fonts** — all in the `:root` block at the top of the `<style>` section.

## Notes

- Roughly 31KB of HTML. The old version was around 380KB, almost all of it a base64 image inlined in the markup.
- Fonts: Bricolage Grotesque, Newsreader, IBM Plex Mono, loaded from Google Fonts.
- `prefers-reduced-motion` is respected — animations off, highlights drawn immediately.
- Includes a print stylesheet, so printing to PDF for applications gives a clean document with link URLs written out.
