# NCAA Division I Men's Basketball Advanced Stats

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

NCAA Division I men's basketball advanced stats with team records, adjusted efficiencies, tempo, Barthag, four factors and three\-point metrics\. Published dataset: 2,190 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/ncaa-division-i-men-s-basketball-advanced-stats-2026-27-5a06355b5589?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 1
- Last published: 2026-11-20T10:00:16.406653Z

## The brief

> I need this data: NCAA Division I men's basketball advanced stats with team records, adjusted efficiencies, tempo, Barthag, four factors and three\-point metrics\. Published dataset: 2,190 rows\.

Summary from the public dataset description.

## NCAA Division I Men's Basketball Advanced Stats 2026–27 / team\_captures

2,190 total rows · 50 sampled · Output revision 6
Published: 2026-11-20T10:00:16.406653Z · Producing pipeline version: 1

[CSV sample](outputs/3c02706620bf/team-captures-b62e049933b3/sample.csv) · [JSON sample](outputs/3c02706620bf/team-captures-b62e049933b3/sample.json) · [Schema](outputs/3c02706620bf/team-captures-b62e049933b3/schema.json)

| adjusted\_defensive\_efficiency | adjusted\_offensive\_efficiency | adjusted\_tempo | barthag | capture\_date | captured\_at | conference | def\_efg\_pct |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 106\.41528281636832 | 103\.56965113508844 | 68\.4906476858051 | 0\.4226984111045624 | 2026\-11\-17 | 2026\-11\-17T10:01:02\.490697\+00:00 | Sum | 41 |
| 108\.35725070982583 | 101\.94200857056421 | 70\.42740164128662 | 0\.33140447462165223 | 2026\-11\-18 | 2026\-11\-18T10:00:54\.789092\+00:00 | BSky | 51\.5 |
| 110\.00172882874884 | 102\.12370919751955 | 68\.87495074859797 | 0\.2984733082226603 | 2026\-11\-17 | 2026\-11\-17T10:01:02\.490697\+00:00 | Slnd | 50\.9 |
| 99\.27000818149743 | 113\.75832979009462 | 70\.53460092908331 | 0\.827309386108854 | 2026\-11\-16 | 2026\-11\-16T10:00:50\.668672\+00:00 | WCC | 51\.1 |
| 111\.8360698705549 | 95\.06654687214882 | 70\.44683131712478 | 0\.1337437081671452 | 2026\-11\-16 | 2026\-11\-16T10:00:50\.668672\+00:00 | NEC | 54\.6 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| adjusted\_defensive\_efficiency | double precision |
| adjusted\_offensive\_efficiency | double precision |
| adjusted\_tempo | double precision |
| barthag | double precision |
| capture\_date | text |
| captured\_at | text |
| conference | text |
| def\_efg\_pct | double precision |
| def\_free\_throw\_rate | double precision |
| def\_offensive\_rebound\_pct | double precision |
| def\_three\_point\_pct | double precision |
| def\_three\_point\_rate | double precision |
| def\_turnover\_pct | double precision |
| efg\_pct | double precision |
| free\_throw\_rate | double precision |
| games\_played | integer |
| offensive\_rebound\_pct | double precision |
| rank | integer |
| record | text |
| source\_url | text |
| statistics\_status | text |
| team | text |
| three\_point\_pct | double precision |
| three\_point\_rate | double precision |
| turnover\_pct | double precision |

## How the pipeline works

```mermaid
flowchart LR
  n0["ratings"]
  n1["factors"]
  n2["team#95;captures"]
  n0 --> n1
  n1 --> n2
```

- **ratings**: Read the complete 2026–27 T\-Rank ratings export, including records and adjusted efficiencies\.
- **factors**: Join the complete four\-factor and three\-point export by exact team name, preserving every team and flagging unavailable source statistics\.
- **team\_captures**: One row per Division I team per capture, with Lisbon capture date and source statistics\.

## Version history

- 2026-11-16T09:15:02.301564Z: v1: Added daily historical captures of all 365 teams’ T\-Rank ratings, four factors and three\-point statistics\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/ncaa-division-i-men-s-basketball-advanced-stats-2026-27-5a06355b5589?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
