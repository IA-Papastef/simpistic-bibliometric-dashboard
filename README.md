# Bibliometric Research Dashboard

A simple browser-based tool for tracking how often specific terms show up in academic journals and Google Scholar over time. Useful for literature reviews, bibliometric analyses, or just satisfying your curiosity about research trends.

It's a single HTML file. No install, no server, no Node.js — just download and open in your browser.

**[Try the live demo here](https://ia-papastef.github.io/simpistic-bibliometric-dashboard/)**

![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)

## Why this exists

I needed to track term frequency across a few journals for a research project. Existing tools like Scopus and Web of Science are great but require institutional access, and Google Scholar doesn't have built-in trend analysis. So I made this.

It doesn't scrape anything automatically (Google Scholar blocks that). Instead, it gives you pre-built search links for every term/year/journal combination — you click the link, note the result count, and type it in. Charts update as you go.

## What it does

- Configurable search terms, target journals, and year range
- Pre-built Google Scholar search links for every data point
- Line charts, bar charts, and stacked area charts (via Chart.js)
- Data saved in your browser's localStorage, so it survives page refreshes
- CSV and JSON export
- JSON import to move data between machines
- Works offline after the first load
- Print-friendly layout for including charts in papers

## How to use it

1. Download `index.html` (or clone this repo)
2. Open it in any browser
3. Go to **Settings** — enter your search terms, journals, and year range
4. Click **Apply & Rebuild**
5. Switch to the **Google Scholar Data** tab
6. Click the 🔗 links, note the "About X results" number, type it in
7. Check **Overview** for your charts

You can also enable GitHub Pages on your fork and use it online.

## Data quality note

Google Scholar counts are approximate and can vary between sessions. For publication-quality bibliometrics, Scopus, Web of Science, or Dimensions are better options. This tool is more for quick exploratory analysis or when you don't have institutional database access.

There's a **Methodology** tab inside the app with more detail on this, including links to alternative tools.

## Technical details

Single HTML file, no build step. Chart.js loaded from CDN, fonts from Google Fonts, everything else is vanilla JS and CSS. Data lives in localStorage — nothing is sent anywhere.

Kept it as one file on purpose so it's easy to download, share, and fork without dealing with npm or bundlers.

## Contributing

Pull requests welcome — just keep it in the single-file format. No build tools or frameworks, please. See [CONTRIBUTING.md](CONTRIBUTING.md) for a few more notes.

## License

MIT
