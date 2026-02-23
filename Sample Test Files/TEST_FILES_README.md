# dataNerdsDashboard Test Files

Drop all 4 files into the dashboard's upload zone simultaneously to see every feature in action.

## Files

| File | Type | Description |
|------|------|-------------|
| `Earnings_File_UnityNodes_2026-01-08.txt` | Earnings | 856 records — first half of data |
| `Earnings_File_UnityNodes_2026-02-22.txt` | Earnings | 857 records — second half (overlaps for dedup testing) |
| `Withdraw_File_UnityNodes_2026-02-22.txt` | Withdrawal | 6 withdrawals — 4 success, 1 pending, 1 failed ETH |
| `Lease_Names_UnityNodes_2026-02-22.txt` | Naming | 24 leases, 5 groups, 3 nodes, notes, splits, expiries |

## What to Expect

### Overview
- 24 leases across 3 nodes (Alpha-Prime, Bravo-East, Charlie-West)
- 45 days of data (Jan 8 – Feb 21, 2026)
- ~$2.19 total earnings, ~$0.049/day average
- 5 groups with distinct color coding

### Groups
| Group | Leases | Node | Split | Color |
|-------|--------|------|-------|-------|
| Powerhouse | 3 | N1 | 100% | Green |
| Workhorses | 7 | N1 | 85% | Blue |
| Scouts | 8 | N2 | 75% | Amber |
| New Fleet | 5 | N3 | 50% | Purple |
| Outpost | 1 | N3 | 60% | Red |

### Features Exercised
- **Dedup testing** — 342 overlapping records between the two earnings files
- **Multi-node analysis** — 3 nodes with different lease counts and performance
- **Split percentages** — group-level splits (50%-100%) plus individual overrides
- **Split history** — Phoenix (3e8f): 50% → 70% → 85% over time; Drift (6f7a): 90% → 75%
- **Gross vs Received toggle** — compare how splits affect rankings
- **Dark lease** — Ghost (a7e1) stops earning after day 28
- **Declining lease** — Drift (6f7a) trends downward over the period
- **Improving lease** — Phoenix (3e8f) trends upward over the period
- **Lease expiry dates** — 4 leases with upcoming expiry warnings
- **Withdrawals** — ADA successes, 1 pending, 1 failed ETH attempt
- **Date notes** — 8 notes marking key events across the timeline
- **Lease notes** — 7 individual lease notes with observations
- **Favorites** — 3 pre-pinned leases (Titan, Apex, Viper)
- **Monthly goal** — $75/month target
- **Alert thresholds** — lease min $0.005, daily min $0.02
- **Node names** — custom names for all 3 nodes
- **Weekend effect** — slightly lower earnings on Sat/Sun
- **Consistency variation** — 70%-92% across groups
- **Multiple txns/day** — 1-3 transactions per lease per day

### Pages to Check
1. **Overview** — KPI cards, group badges, participation gauge
2. **Earnings** — Daily bar chart with 7-day moving average, trend line
3. **Distribution** — Scatter plot showing lease spread, 1/3/5 day filters
4. **Insights** — Streaks, dark lease detection, node comparison, DOW analysis
5. **Leases** — Full table with sparklines, group/all views, sort options
6. **Archive** — Monthly breakdown, full archive export
7. **Names** — Group editor with all 5 groups populated
8. **Tools** — Goal tracker ($75 target), alerts, node map, health dashboard
9. **Easy Mode** — Simplified view with revenue trend + week vs week
10. **Lease Detail** — Click any lease for deep-dive stats and notes

### Intentional Test Scenarios
- Load both earnings files → dedup should reduce ~1713 to ~1371 unique records
- Toggle Received/Gross → Powerhouse stays same, New Fleet earnings double
- Check Insights → should flag Ghost as dark lease, Drift as declining
- Check lease expiry warnings on Leases page
- View split history on Phoenix and Drift lease detail pages
- Verify withdrawal summary shows net balance correctly
- Check heatmap for weekend dimming pattern
