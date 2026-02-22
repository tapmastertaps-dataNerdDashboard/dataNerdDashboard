# Changelog

## v4.20 (2026-02-22)

### New Features
- **Easy/Advanced Mode** — Clean easy mode with essential charts, advanced mode for full analytics
- **Favorites** — Star/pin leases to sort them to the top of the table
- **Sparklines** — 7-day mini trend chart in each lease table row
- **Custom Date Range** — Filter all earnings to a specific date range
- **CSV Export** — Download the full lease table as CSV
- **Onboarding Tour** — 6-step guided walkthrough for new users
- **Node Map** — Visual layout showing lease distribution across nodes (X/200 capacity)
- **Week vs Week Comparison** — This week vs last week earnings snapshot
- **Printable Summary** — One-page report card (opens in new tab, print-ready)
- **Animated Transitions** — Smooth fade when switching easy/advanced mode
- **Side-by-Side Layout** — Distribution chart (2/3) + Heatmap calendar (1/3) in easy mode

### Improvements
- Muted dark mode — softer, desaturated colors instead of neon
- Lease notes auto-save on navigation (no save button needed)
- Notes 📝 icon appears on leases with notes across all charts
- Read-only note popup when clicking 📝 icon
- Goal, alerts, and favorites persist in naming file
- Settings export/import via naming file

### Bug Fixes
- Fixed node assignments being overwritten by auto-detection
- Fixed Names Editor import regex not handling split/expiry flags
- Fixed safeHTML stripping onclick handlers from note buttons
- Fixed easy mode hover tooltip on daily bar chart

### Security (Session 28 Audit)
- Added FileReader error handlers (5 instances)
- Migrated 10 high-risk innerHTML to safeHTML
- Added 50MB file size validation
- Fixed parseInt radix parameters
- Wrapped JSON.parse in try/catch

## v3.3 (2026-02-22)
- Security audit and hardening
- Bug prevention pass

## v3.2 (2026-02-21)
- Split percentage system (group + individual + history)
- Gross/Received toggle affecting 65+ calculations
- Lease expiry tracking

## v3.1 (2026-02-20)
- Distribution chart with node shape markers
- Revenue trend chart with period aggregation
- Share snapshots
- Silent alerts

## v3.0 (2026-02-19)
- Complete UI redesign
- Multi-node support
- Naming file system with groups
- Insights page with AI-powered analysis
- Node health dashboard
- PDF export

## v2.0 (2026-02-15)
- Heatmap calendar
- Lease detail pages
- Withdrawal tracking
- Archive system

## v1.0 (2026-02-10)
- Initial release
- Basic earnings overview
- Daily bar chart
- KPI cards
