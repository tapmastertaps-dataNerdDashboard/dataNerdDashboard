# dataNerd Dashboard for Unity

A comprehensive, fully offline analytics dashboard for Unity node operators. Single HTML file, zero external connections, security-first design.

## Features

**Core Analytics**
- Daily earnings trends with 7-day moving average
- License earning distribution (scatter plot by group/node)
- Earnings heatmap calendar
- Hour-of-day activity radar chart
- Revenue trend lines (Day/Week/Month aggregation)
- Period comparisons (Week-over-Week)

**Lease Management**
- Full lease table with sparkline trends, favorites, and CSV export
- Custom date range filtering
- Per-lease detail pages with earnings charts and stats
- Lease notes with auto-save
- Split percentage system (group + individual + history)
- Lease expiry tracking

**Node Operations**
- Multi-node support (up to 6 nodes, 200 leases each)
- Node health dashboard with uptime estimates
- Node map visualization with capacity tracking
- Per-node earnings efficiency comparison

**Insights & Alerts**
- Portfolio health score
- Earning streaks and consistency tracking
- Dark lease detection (inactive 3+ days)
- Outlier detection
- Silent alerts system

**Easy & Advanced Modes**
- Easy mode: Clean overview with essential charts
- Advanced mode: Full access to all analytics pages

**Data Management**
- Naming file system (lease names, groups, notes, splits, goals, favorites)
- CSV upload for earnings and withdrawal data
- Auto-sort file detection
- PDF report export
- Printable one-page summary
- SHA-256 file integrity verification

**Security**
- Fully offline — zero external network requests
- CSP headers (default-src 'none')
- HTML sanitization (safeHTML + sanitizeText)
- Prototype pollution guard
- Frame-busting protection
- File size validation (50MB limit)

## Quick Start

1. Download `dataNerdsDashboardForUnity.html`
2. Open in any modern browser
3. Upload your Unity earnings CSV files
4. Optionally upload a naming file for lease names and groups

No server, no installation, no dependencies.

## File Structure

```
dataNerdsDashboardForUnity.html  — The complete dashboard (single file)
CHANGELOG.md                     — Version history
LICENSE                          — MIT License
```

## Data Privacy

This dashboard processes all data locally in your browser. No data is ever transmitted anywhere. The only network request is a self-fetch for SHA-256 integrity verification.

## Export File Naming Convention

All exports follow a consistent pattern:
- `Earnings_File_UnityNodes_YYYY-MM-DD.csv`
- `Withdraw_File_UnityNodes_YYYY-MM-DD.csv`
- `Naming_File_UnityNodes_YYYY-MM-DD.txt`
- `Lease_Export_UnityNodes_YYYY-MM-DD.csv`

## Version

**v4.20** — 10,800+ lines, 200+ functions, 9 pages

## Author

Created by dataNerdsDash

## License

MIT License — see [LICENSE](LICENSE)
