# Changelog

All notable changes to this project will be documented in this file.
The format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) and this project uses [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.1.0] - 2026-05-19

### Added
- **Location attribute** on Next Match and Last Result sensors. The venue is fetched from the individual match detail page on voetbal.nl and formatted as `<name>, <street>, <city>` (e.g. `Sporthallen Zuid, Burgerweeshuispad 54, Amsterdam`).
- **`match_url` attribute** on the Next Match sensor — direct link to the match detail page on voetbal.nl.

### Fixed
- Next Match and Last Result sensors no longer fall back to showing a random fixture when the configured team name does not match any team name in the voetbal.nl schedule. The sensor now correctly returns `No upcoming matches` / `No results yet` in that case. A debug log entry lists the team names actually present in the schedule to help correct the configuration.

---

## [1.0.0] - 2026-05-01

### Added
- Initial release.
- Standing sensor with league position and full standings table.
- Next Match sensor with date, time, home/away indicator, and opponent.
- Last Result sensor with score and win/loss/draw result.
- Calendar entity showing only the configured team's fixtures.
- Lovelace dashboard example (`lovelace_dashboard.yaml`).
- HACS support.
