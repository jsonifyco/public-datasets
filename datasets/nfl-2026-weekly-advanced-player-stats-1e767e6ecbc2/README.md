# NFL player stats: 2026 advanced stats dataset \(EPA, CPOE, target share\)

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

NFL 2026 regular\-season player stats, including passing, rushing and receiving totals, EPA, CPOE, air yards, target share and WOPR\. Source: nflverse \(CC BY 4\.0\)\. Export to CSV, Excel or Google Sheets\.

[Get the full dataset for free](https://www.jsonify.com/datasets/nfl-2026-weekly-advanced-player-stats-1e767e6ecbc2?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 1
- Last published: 2026-11-24T10:00:34.106723Z

## The brief

> I need this data: NFL 2026 regular\-season player stats, including passing, rushing and receiving totals, EPA, CPOE, air yards, target share and WOPR\. Source: nflverse \(CC BY 4\.0\)\. Export to CSV, Excel or Google Sheets\.

Summary from the public dataset description.

## NFL 2026 Advanced Player Stats History / player\_stats

1,118 total rows · 50 sampled · Output revision 2
Published: 2026-11-24T10:00:34.106723Z · Producing pipeline version: 1

[CSV sample](outputs/d6fc2b3224fd/player-stats-daac3ba5b816/sample.csv) · [JSON sample](outputs/d6fc2b3224fd/player-stats-daac3ba5b816/sample.json) · [Schema](outputs/d6fc2b3224fd/player-stats-daac3ba5b816/schema.json)

| snapshot\_key | capture\_date | capture\_at | season | season\_type | player\_id | player | team |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 2026\-11\-24T10:00:26\.731522\+00:00:00\-0040583 | 2026\-11\-24 | 2026\-11\-24T10:00:26\.731522\+00:00 | 2026 | REG | 00\-0040583 | Woody Marks | HOU |
| 2026\-11\-24T10:00:26\.731522\+00:00:00\-0034351 | 2026\-11\-24 | 2026\-11\-24T10:00:26\.731522\+00:00 | 2026 | REG | 00\-0034351 | Dallas Goedert | PHI |
| 2026\-11\-23T10:23:04\.344758\+00:00:00\-0028986 | 2026\-11\-23 | 2026\-11\-23T10:23:04\.344758\+00:00 | 2026 | REG | 00\-0028986 | Case Keenum | CHI |
| 2026\-11\-24T10:00:26\.731522\+00:00:00\-0038621 | 2026\-11\-24 | 2026\-11\-24T10:00:26\.731522\+00:00 | 2026 | REG | 00\-0038621 | DeMario Douglas | NE |
| 2026\-11\-24T10:00:26\.731522\+00:00:00\-0041040 | 2026\-11\-24 | 2026\-11\-24T10:00:26\.731522\+00:00 | 2026 | REG | 00\-0041040 | Antonio Williams | WAS |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| snapshot\_key | text |
| capture\_date | text |
| capture\_at | text |
| season | integer |
| season\_type | text |
| player\_id | text |
| player | text |
| team | text |
| position | text |
| games | integer |
| completions | double precision |
| attempts | double precision |
| passing\_yards | double precision |
| passing\_tds | double precision |
| passing\_interceptions | double precision |
| sacks\_suffered | double precision |
| sack\_yards\_lost | double precision |
| sack\_fumbles | double precision |
| sack\_fumbles\_lost | double precision |
| passing\_air\_yards | double precision |
| passing\_yards\_after\_catch | double precision |
| passing\_first\_downs | double precision |
| passing\_epa | double precision |
| passing\_cpoe | double precision |
| passing\_2pt\_conversions | double precision |
| pacr | double precision |
| passing\_10 | double precision |
| passing\_16 | double precision |
| passing\_20 | double precision |
| passing\_40 | double precision |
| carries | double precision |
| rushing\_yards | double precision |
| rushing\_tds | double precision |
| rushing\_fumbles | double precision |
| rushing\_fumbles\_lost | double precision |
| rushing\_first\_downs | double precision |
| rushing\_epa | double precision |
| rushing\_2pt\_conversions | double precision |
| rushing\_10 | double precision |
| rushing\_12 | double precision |
| rushing\_20 | double precision |
| rushing\_40 | double precision |
| receptions | double precision |
| targets | double precision |
| receiving\_yards | double precision |
| receiving\_tds | double precision |
| receiving\_fumbles | double precision |
| receiving\_fumbles\_lost | double precision |
| receiving\_air\_yards | double precision |
| receiving\_yards\_after\_catch | double precision |
| receiving\_first\_downs | double precision |
| receiving\_epa | double precision |
| receiving\_2pt\_conversions | double precision |
| receiving\_10 | double precision |
| receiving\_16 | double precision |
| receiving\_20 | double precision |
| receiving\_40 | double precision |
| racr | double precision |
| target\_share | double precision |
| air\_yards\_share | double precision |
| wopr | double precision |
| source\_url | text |
| source\_last\_modified | text |
| source\_sha256 | text |
| licence\_note | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["check#95;licence"]
  n1["capture#95;stats"]
  n2["player#95;stats"]
  n0 --> n1
  n1 --> n2
```

- **check\_licence**: Confirm that the public nflverse data licence remains the reviewed CC BY 4\.0 licence before downloading statistics\.
- **capture\_stats**: Download the complete 2026 regular\-season player summary, keep all players with offensive activity, and attach capture time and attribution\.
- **player\_stats**: Historical season\-to\-date offensive player captures, retaining passing, rushing and receiving statistics with CC BY 4\.0 attribution\.

## Version history

- 2026-11-23T10:16:28.298200Z: v1: Added licensed nflverse 2026 regular\-season advanced player statistics with dated historical captures and attribution\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/nfl-2026-weekly-advanced-player-stats-1e767e6ecbc2?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
