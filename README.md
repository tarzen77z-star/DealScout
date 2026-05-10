# DealScout 🏷️
### by SBB

A mobile-friendly live deals dashboard that pulls real-time discounts, sales, and promotions from multiple sources automatically.

## What it does

DealScout aggregates live deals from 6 RSS feeds and displays them as a scrollable card feed. No backend, no database — just open the file in a browser and deals load instantly.

**Live sources:**
- Slickdeals (frontpage deals)
- DealNews (Electronics)
- DealNews (Home & Garden)
- DealNews (Fashion & Clothing)
- DealNews (Travel)
- Reddit r/deals

## Features

- 📡 Live RSS feed — auto-loads on open, refresh anytime
- 🔍 Hidden search — tap Search to filter loaded deals
- 🏷️ Filter by source with one tap
- 🕐 Sort by newest, oldest, or A–Z
- ❤️ Save deals (persists in browser storage)
- ⚠️ Per-source error indicators if a feed is down
- 📱 Mobile-first, works on any screen size

## How to use

### Option 1 — Open locally
Just open `index.html` in any browser. No setup needed.

### Option 2 — Host on GitHub Pages
1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set source to **main branch / root**
4. Your dashboard will be live at `https://yourusername.github.io/dealscout`

## Powered by

- [rss2json.com](https://rss2json.com) — converts RSS feeds to JSON (free tier, 10,000 req/day)
- No other dependencies — pure HTML, CSS, and vanilla JavaScript

## Updating deals / adding sources

Open `index.html` and find the `SOURCES` array near the top of the `<script>` section. Each source looks like this:

```js
{
  id: 'my_source',
  label: 'My Source',
  url: 'https://example.com/rss-feed-url',
  color: '#FF6B6B',
  badgeBg: '#FFF0F0',
  badgeColor: '#CC2200'
}
```

Add, remove, or swap any RSS feed URL there.

## Notes

- rss2json free tier returns **10 deals per feed** — sign up at rss2json.com for a free API key to get up to 50
- Search only filters **currently loaded deals** — refresh first to get the latest before searching
- Saved deals are stored in **browser localStorage** — clearing browser data will remove them

---

Built by **SBB**
