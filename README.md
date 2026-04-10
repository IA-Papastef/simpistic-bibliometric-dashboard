# 📊 Bibliometric Research Dashboard

A free, open-source, browser-based tool for tracking and visualizing the frequency of search terms across academic journals and Google Scholar over time.

**No installation. No server. No dependencies.** Just open `index.html` in your browser.

[![🚀 Open Live Demo](https://img.shields.io/badge/🚀_Open_Live_Demo-Click_Here-c45d3e?style=for-the-badge&logoColor=white)](https://ia-papastef.github.io/simpistic-bibliometric-dashboard/)

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
![No Dependencies](https://img.shields.io/badge/dependencies-0-brightgreen)
![Status: Stable](https://img.shields.io/badge/status-stable-green)

> **👉 [Try it now in your browser](https://ia-papastef.github.io/simpistic-bibliometric-dashboard/)** — no download needed!

---

## 🎯 What It Does

Researchers often need to track how frequently specific terms appear in academic literature over time — a basic bibliometric analysis. This tool provides:

- **Pre-built Google Scholar search links** for every term × year × journal combination
- **Editable data tables** where you enter the result counts you find
- **Auto-generated charts** (line, bar, stacked area) that update as you type
- **Data persistence** via browser `localStorage` — your work is saved automatically
- **CSV and JSON export** for further analysis in R, Python, SPSS, or Excel
- **Fully configurable** — change the search terms, journals, and year range to suit any research question

## 🚀 Quick Start

### Option 1: Download and Open
1. Download `index.html` (just the one file)
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. Start entering data

### Option 2: Clone the Repository
```bash
git clone https://github.com/IA-Papastef/simpistic-bibliometric-dashboard.git
cd bibliometric-dashboard
# Open in browser — no build step needed
firefox index.html
# or
google-chrome index.html
# or
xdg-open index.html
```

### Option 3: GitHub Pages
This project works out-of-the-box with [GitHub Pages](https://pages.github.com/). Enable it in your repository settings and access the dashboard at `https://IA-Papastef.github.io/simpistic-bibliometric-dashboard/`.

## 📖 How to Use

### 1. Configure Your Research (Settings Tab)
The dashboard ships with default terms and journals for philosophy of education research. Customize them:
- **Search Terms**: One per line (e.g., `cosmopolitanism`, `global justice`)
- **Journals**: One per line (the full journal name as it appears on Google Scholar)
- **Year Range**: Start and end year for your analysis

Click **Apply & Rebuild** to regenerate the dashboard.

### 2. Collect Data (Google Scholar Data / Journal Data Tabs)
Each cell in the data tables has a 🔗 button that opens a pre-built Google Scholar search. The search query is:
- **General**: `"exact term"` filtered to a single year
- **Journal-specific**: `"exact term" source:"Journal Name"` filtered to a single year

Look at the **"About X results"** count at the top of the Google Scholar results page and enter it in the corresponding cell.

### 3. View Charts (Overview Tab)
Charts update automatically when you switch to the Overview tab:
- **Line Chart**: Trend over time for all terms
- **Bar Chart**: Year-by-year comparison across terms
- **Stacked Area Charts**: Per-term breakdown by journal

### 4. Export Your Data
- **CSV**: For spreadsheet software and statistical tools
- **JSON**: For programmatic use or backup/restore
- **Print**: Clean print stylesheet for including charts in documents

## 🏗️ Architecture

```
bibliometric-dashboard/
├── index.html          # The entire application (single file)
├── README.md           # This file
├── LICENSE             # MIT License
├── CONTRIBUTING.md     # Contribution guidelines
├── CHANGELOG.md        # Version history
└── docs/
    └── screenshots/    # Screenshots for documentation
```

The application is deliberately a **single HTML file** with no build step, no bundler, and no package manager. This makes it:
- **Portable**: Copy one file, it works anywhere
- **Archivable**: No dependency rot, no broken npm packages
- **Accessible**: Anyone can open an HTML file
- **Forkable**: Everything is in one place, easy to modify

### External Resources (CDN)
- [Chart.js 4.4.1](https://www.chartjs.org/) — Charting library (loaded from cdnjs with SRI hash)
- [Google Fonts](https://fonts.google.com/) — Libre Baskerville + DM Sans

Both are optional for functionality (charts degrade gracefully, fonts fall back to system defaults).

### Data Storage
All data is stored in the browser's `localStorage` under the key `bibliometric_dashboard_v1`. No data ever leaves your machine. Use the JSON export/import to back up or transfer data between browsers.

## ⚠️ Methodological Caveats

This tool helps you **organize and visualize** bibliometric data — it does not automatically collect it. Important notes:

1. **Google Scholar counts are approximate** — they are rounded and can fluctuate between sessions
2. **The `source:` filter is imperfect** — Google Scholar may miss or misclassify some articles
3. **For publication-quality research**, use [Scopus](https://www.scopus.com/), [Web of Science](https://www.webofscience.com/), or [Dimensions](https://app.dimensions.ai/) which provide exact counts and structured exports
4. **Always record your data collection date** — counts change over time
5. **Partial-year data** (e.g., the current year) will naturally show lower numbers
6. **The tool [Publish or Perish](https://harzing.com/resources/publish-or-perish)** (free) can automate Google Scholar data collection

## 🤝 Contributing

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Some ideas for contributions:
- [ ] Dark mode toggle
- [ ] More chart types (heatmap, pie charts)
- [ ] Direct integration with Scopus/Crossref APIs
- [ ] Multi-language support (i18n)
- [ ] Offline service worker for full offline support
- [ ] Keyboard navigation improvements

## 📋 Changelog

See [CHANGELOG.md](CHANGELOG.md) for version history.

## 📄 License

This project is licensed under the **MIT License** — see [LICENSE](LICENSE) for details.

You are free to use, modify, and distribute this tool for any purpose, including commercial use.

## 🙏 Acknowledgments

- [Chart.js](https://www.chartjs.org/) for the charting library
- [Google Scholar](https://scholar.google.com/) for making academic search accessible
- The academic community for inspiring this tool

---

**If this tool helps your research, consider giving it a ⭐ on GitHub!**
