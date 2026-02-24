# dataNerds Dashboard for Unity — Changelog

## v5.0.0 — 2026-02-23
### Security Hardening
- **Removed ALL 152 inline event handlers** (onclick, onchange, oninput, onmouseenter/leave)
- Replaced with CSP-compliant `data-action` delegated event system
- Zero inline JavaScript in HTML attributes — eliminates XSS injection surface
- Central event dispatcher handles all user interactions via delegation

### Bug Fixes
- **Archive + Fresh Export overlay**: Fixed `autoDetectStartDate` dropping archive data when loaded alongside a newer export. Previously used latest-of-earliest dates (filtering out older archive data); now uses earliest date across all files.
- **Withdrawal ADA amounts**: Fixed `₳0.00` display on archived withdrawals. Parser now supports flat `cryptoAmount` field (lovelace) in addition to nested `settlement.assetAmount` format.
- **Group Share donut chart**: Fixed broken image rendering by removing premature canvas render during build chain (Distribution page hidden at build time). Now renders only on page navigation.
- **showPage cascade failure**: Wrapped all page-switch render calls in try-catch to prevent one chart failure from blocking subsequent renders.

### Performance
- Removed redundant `renderDist()`, `renderGroupDonut()`, and `renderRadar()` calls from build chain — these charts now render on-demand when their page is shown.
- Removed 77 lines of dead code (unused functions, unreachable branches).

### Internal
- Added `VERSION` constant (`5.0.0` for secure, `5.0.0-dev` for development)
- All render calls crash-safe: build chain, resize handler, showPage navigation

---

## v4.3 — 2026-02-22
### Features
- Donation modal with Cardano (ADA) address
- Offline operation badge
- Session activity warnings
- File type validation hardening
- Clipboard copy protection on sensitive fields

### Fixes
- Build chain cascade failure (try-catch on all renders)
- Collapsed cards becoming unrestorable (CSS + initCardControls fix)
- Radar legend overlap
- localStorage versioning for settings persistence

---

## v4.2 — 2026-02-20
- Initial public release on GitHub Pages
- Full earnings dashboard with 10+ chart types
- Archive system for historical data
- Naming file for lease organization (groups, nodes, splits, notes)
- All processing client-side — zero network requests
