# NBA hosted validation — 2026-10-24

Live dashboard: https://nba-statistical-research.streamlit.app/

Repository: https://github.com/Pokered03/NBA-Statistical-Research

The user approved public repositories and dashboards for NBA and the remaining four sports. This NBA app runs independently from NFL and the existing Multi-Sport Value Engine, neither of which was changed.

## Completed verification

- The 46 original tracked files were downloaded from GitHub and compared byte for byte, with no missing or changed files. Five explanatory directory/package files were also present. The downloaded archive independently passed **38 tests**, with 3 unrelated sport cases skipped (2.37 seconds).
- Local 64-switch AppTest: cold render **0.696 seconds**, first matchup **0.049 seconds**, switching p95 **0.085 seconds**, peak process RSS **143.65 MiB**. Local HTTP health and root status 200 passed, about 0.512 seconds to health.
- Deployed main/app.py with tested Python 3.12 and PyArrow 24.0.0.
- The hosted page renders current-season schedules and NBA offense, defense and situational comparisons. October 24 exposed **8 scheduled matchups**. Miami–Charlotte and Golden State–Phoenix comparisons were exercised.
- Manual comparison, ending-year 2026/2027 season switching, neutral venue, last 3/5/10 windows, and manual spread -4.5 / total 225.5 inputs worked. Historical Atlanta–Boston comparison rendered.
- Historical validation exposes 1,655 held-out games, Brier 0.207, margin MAE 11.612 points and total MAE 15.108 points. These are the documented historical results, not promised future accuracy. Early 2026–27 games correctly show PASS when there are too few observed games. Spread/total remain PASS because their historical-line/category validation is unavailable.
- The sampled hosted process peaked at **170.7 MiB**, below the 350 MiB development target. The host exposed **3072 MiB** cgroup limit; sampled container usage **691.8–700.9 MiB** includes other processes and file cache. Long-term peaks and a load test remain unverified.
- Independent hosted refresh https://github.com/Pokered03/NBA-Statistical-Research/actions/runs/40114310755 **succeeded in 42 seconds** (job 36 seconds), running tests, collection, rebuild, integrity checks and publication.

- A second independent browser session loaded while the first stayed active. It picked up the **2026-10-24T17:03:06.252958+00:00** worker timestamp and refreshed Miami/Charlotte records from one to two observed games. This is a basic concurrency check, not a load test.
- A final NBA label/source cleanup also passed all 38 tests (3 unrelated sport cases skipped, 2.15 seconds locally).

## Independent automatic refresh

ENABLE_FREE_REFRESH=true is set. Daily cron **10:23 UTC** (6:23 AM Eastern during daylight time; 5:23 AM Eastern during standard time), subject to GitHub scheduling delays. The workflow requires a public repository, uses the standard ubuntu-latest free runner, and creates no cache/artifact storage. No paid sports APIs, Odds API credits, paid hosting or larger paid runners are used. This is daily updating, not immediate end-of-game updating; public schedules may require re-enabling after inactivity.

The first successful job reported non-blocking Node20 action deprecation and ubuntu-latest migration notices; maintain the action/runner versions as upstream support changes.

## Remaining work

Real mobile/iPhone and MacBook-specific verification, sustained concurrent load, forced restart recovery, longer hosted stability testing, verified live injuries and calibrated player-role adjustments remain outstanding. Observed player boxes are historical role/minute context and bench scoring, not confirmed injury availability. Missing statistics stay N/A. A daily scheduled trigger has been configured, while the first worker test was manually dispatched.

The full six-dashboard project is not complete. NFL and NBA have deployed development builds with initial hosted checks; the other four remain separate development builds awaiting publication/deployment and their own live tests.
