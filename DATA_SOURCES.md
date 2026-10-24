# Sources, permissions and coverage

Primary integrated source: [hoopR NBA / SportsDataverse](https://github.com/sportsdataverse/hoopR-nba-data).

CC BY 4.0; modified by this research application

Other source-specific links:

- nflverse data and license: https://github.com/nflverse/nflverse-data
- hoopR NBA data: https://github.com/sportsdataverse/hoopR-nba-data
- hoopR D-I data: https://github.com/sportsdataverse/hoopR-mbb-data
- cfbfastR data publication: https://github.com/sportsdataverse/cfbfastR-cfb-data
- fastRhockey NHL data: https://github.com/sportsdataverse/fastRhockey-nhl-data
- baseballr schedule archive: https://github.com/sportsdataverse/baseballr-data
- Retrosheet permissions and downloads: https://www.retrosheet.org/downloads/csvdownloads.html
- Retrosheet game-log fields: https://www.retrosheet.org/gamelogs/glfields.txt

Only this sport’s adapter runs. No source requires an existing Odds API key. The data worker has an explicit host allowlist and rejects other API hosts. No direct ESPN scraping is enabled. No proprietary logo or premium statistical dataset is distributed. Preserve upstream notices and verify original league/dataset rights before public redistribution; an open-source wrapper license does not by itself license every underlying league asset. College football’s dataset-specific redistribution terms remain a public-release blocker.

## Snapshot coverage at build time

```json
[
  {
    "season": 2024,
    "teams_with_completed_games": 30,
    "registered_teams": 30,
    "schedule_games": 1321,
    "latest_final": "2024-06-17"
  },
  {
    "season": 2025,
    "teams_with_completed_games": 30,
    "registered_teams": 30,
    "schedule_games": 1326,
    "latest_final": "2025-06-22"
  },
  {
    "season": 2026,
    "teams_with_completed_games": 30,
    "registered_teams": 30,
    "schedule_games": 1326,
    "latest_final": "2026-06-13"
  },
  {
    "season": 2027,
    "teams_with_completed_games": 30,
    "registered_teams": 30,
    "schedule_games": 1200,
    "latest_final": "2026-10-22"
  }
]
```

These counts describe source observations, not independently certified official membership completeness. The current college-basketball preseason registry uses the latest available standings plus published conference membership; verify new-season changes when an official standings file becomes available. See the live coverage table for later updates.

## Expanded integrations and remaining gaps

Bench points are reconstructed from player boxes only when exactly five reported starters and the sum of player points reconcile with the final score. Observed rotations include reported starters, recorded minutes and recent lineup changes, with source timestamps. Conflicting provider active/DNP/reason fields are not used to infer injury status. These observations do not automatically adjust forecasts.

Official MLB season and probable-pitcher data use a few bounded personal-research summary requests; no game-log/player-history bulk API fetch is enabled. Original MLB terms apply. No paid feed, Odds API key or premium grades are used. See the runtime source/coverage metadata and each per-metric sample count. Injury, weather, future goalie confirmations and proprietary metrics remain incomplete.
