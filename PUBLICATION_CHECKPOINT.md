# NBA publication checkpoint — 2026-10-24

Repository: https://github.com/Pokered03/NBA-Statistical-Research

Independent private repository created and populated. At commit e5edf68055c679d3751f5c51019da9a18760f87c, all **46 original tracked files** matched the downloaded archive byte for byte. Five explanatory directory/package files were additionally present. Temporary SQLite build journals were excluded. The real independently managed SQLite store is **6,361,088 bytes**.

## Verification

- Python 3.12; PyArrow pinned to 24.0.0 to match the stable version observed on Streamlit hosting.
- Updated application: **38 tests passed, 3 unrelated sport tests skipped**, 2.18 seconds locally. The downloaded archive was also tested independently.
- SQLite integrity and foreign keys passed; schedule rows 2024: 1321, 2025: 1326, 2026: 1326, 2027: 1200. These are ending-year season labels, and schedule counts include future games. All 30 current teams are registered.
- Local isolated HTTP server: health OK, root status 200, 0.512 seconds to health.
- 64-switch AppTest: cold render 0.696 seconds, first matchup 0.049 seconds, switching p95 0.085 seconds, peak process RSS 143.65 MiB. All local resource targets passed. These are not hosted/mobile measurements.
- The app reads prepared summaries only; collection and modeling run outside the web process. Hosted memory diagnostics are included for deployment checks.

## Statistical limitations

Box-derived offensive/defensive ratings, pace, shooting efficiency, rebounding and turnover metrics are available with observed samples. Reconciled player boxes supply historical bench scoring and reported starters/minutes/role changes. These are not verified live injury reports and do not implement calibrated player-role forecast adjustments. Unsupported advanced metrics remain N/A.

Historical win-probability validation and scoring error reports are included in reports/backtest.json. They do not guarantee future accuracy. Spread/total confidence remains PASS without integrated historical-line/category validation. Early current-season matchups may also lack the minimum observed games for probabilities.

## Deployment boundary

Streamlit Community Cloud permits one private app in this workspace, which is already occupied. The NFL project received separate user approval for public visibility and is live. This NBA project awaits its own public-visibility approval before that free deployment route can proceed. No visibility change, paid hosting or private-runner spending has been authorized here.

The guarded independent daily update schedule is prepared for **10:23 UTC**, subject to scheduler delays. It requires ENABLE_FREE_REFRESH=true and a public repository, uses a standard free public runner, and creates no cache/artifact storage. It remains inactive until deployment authorization.

After approval, deploy main/app.py/Python 3.12, test scheduled/manual comparisons, current/historical seasons, source timestamps, probability limitations and host memory, then run and verify a real hosted refresh. Actual mobile checks, concurrent load, restart recovery, extended stability and remaining advanced-data coverage are still outstanding.

**Status: published and locally verified development build; not deployed or complete.**
