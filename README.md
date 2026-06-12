```markdown
# Thailand Tourism Outlook — May 2026

An interactive, bilingual (Thai / English) web recreation of the Tourism Authority of Thailand (TAT) market-trends infographic for **May 2026 (พฤษภาคม 2569)**. It turns a static 4-page PDF into a single scrolling web page with live charts, data tables, and a language toggle.

> Built from `situation_may_26_infographic-compressed.pdf` (TAT, Marketing Strategy Division — International Market Analysis). Data as of 27–30 April 2026.

## Preview

Open `index.html` in any modern browser. No build step, no server required.

## Features

- **Single self-contained file** — HTML, CSS, and JS inline; only external dependency is Chart.js via CDN.
- **TH / EN toggle** — one button swaps every label, including chart axes and tooltips.
- **Four sections**
  1. **Foreign Market** — TOP 5 short-haul & long-haul arrivals, market split, forward bookings, flight plan.
  2. **Drivers of Foreign Demand** — supporting factors (China Labour Day, concert-driven tourism) vs. headwinds (energy crisis, IMF GDP cuts, regional competition).
  3. **Domestic Market** — trips & revenue by region, TOP 5 main and emerging cities.
  4. **Domestic Factors** — long-weekend travel, rail trend, festivals vs. economic and weather headwinds.
- **Interactive charts** — animated bar charts with growth-rate annotations and hover tooltips (Chart.js).
- **Responsive** — adapts from desktop to mobile; sticky header with section navigation.

## Headline figures (May 2026 forecast, YoY)

| Metric | Value | Change |
|---|---|---|
| Foreign arrivals | 2.0M | −8% |
| Air seat capacity | 3.6M | −2% |
| Domestic trips | 16.59M | −3% |
| Domestic revenue | ฿89,989M | −12% |

## Project structure

```
.
├── index.html        # the entire website (markup + styles + scripts + data)
├── situation_may_26_infographic-compressed.pdf   # source infographic
├── specs/            # source materials
└── LICENSE
```

## Tech

- Plain HTML5 / CSS3 (CSS grid, no framework)
- Vanilla JavaScript (no bundler)
- [Chart.js 4.4.1](https://www.chartjs.org/) via cdnjs
- Fonts: IBM Plex Sans Thai + Inter (Google Fonts)

## Editing the data

All figures live in the `const T = { ... }` object inside the `<script>` block in `index.html`. Each series carries Thai labels (`labels_th`), English labels (`labels_en`), values (`vals`), and growth strings (`g`). Update those arrays to refresh the charts; section tables and KPI cards are plain HTML with paired `data-th` / `data-en` spans.

## Deployment

Static hosting only — drop `index.html` onto GitHub Pages, Netlify, Cloudflare Pages, S3, or any web server.

## Attribution

Data and original infographic © Tourism Authority of Thailand (TAT), Marketing Strategy Division. Underlying sources cited in the infographic: ForwardKeys, OAG, Google Trends, IMF, Agoda Travel Outlook 2026. This web version is a presentation layer over that published material.
```

Want me write this to `README.md` in your folder?
