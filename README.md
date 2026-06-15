# Tracxn — What's new

A redesign of the Tracxn product-announcements page, modeled on the Webflow
[`/updates`](https://webflow.com/updates) pattern. Light theme, Roboto, single
blue accent.

## Pages

- [`product-announcements-v2.html`](./product-announcements-v2.html) — main page
  with hero, 4 featured cards (1 large + 3 small stacked), a chronological
  timeline with sticky title panes, and a support section.
- [`pa-detail.html`](./pa-detail.html) — article template for a single
  product announcement.

The root URL (`/`) rewrites to `product-announcements-v2.html` via
[`vercel.json`](./vercel.json).

## Stack

- Pure HTML / CSS / vanilla JS — no build step
- Roboto (Google Fonts)
- Light theme with Webflow blue (`#146EF5`) accent
- Timeline uses a CSS "punch-through" trick — a 1px line with
  `padding-bottom: 300px` bleeds into each following item, and per-item
  dot wrappers use the page background colour to mask the line behind the
  dot, producing one continuous vertical track without JavaScript

## Local preview

```bash
python3 -m http.server 8765
# open http://localhost:8765
```
