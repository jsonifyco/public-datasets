# NCAA Division I Men's Basketball Advanced Stats

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

NCAA Division I men's basketball advanced stats with team records, adjusted efficiencies, tempo, Barthag, four factors and three\-point metrics\. Published dataset: 3,650 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/ncaa-division-i-men-s-basketball-advanced-stats-2026-27-5a06355b5589?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 1
- Last published: 2026-11-24T10:00:34.969006Z

## The brief

> I need this data: NCAA Division I men's basketball advanced stats with team records, adjusted efficiencies, tempo, Barthag, four factors and three\-point metrics\. Published dataset: 3,650 rows\.

Summary from the public dataset description.

## NCAA Division I Men's Basketball Advanced Stats 2026–27 / team\_captures

3,650 total rows · 50 sampled · Output revision 10
Published: 2026-11-24T10:00:34.969006Z · Producing pipeline version: 1

[CSV sample](outputs/3c02706620bf/team-captures-b62e049933b3/sample.csv) · [JSON sample](outputs/3c02706620bf/team-captures-b62e049933b3/sample.json) · [Schema](outputs/3c02706620bf/team-captures-b62e049933b3/schema.json)

| adjusted\_defensive\_efficiency | adjusted\_offensive\_efficiency | adjusted\_tempo | barthag | capture\_date | captured\_at | conference | def\_efg\_pct |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 107\.98036752839172 | 106\.2474821220303 | 69\.83531293476553 | 0\.45362104028085765 | 2026\-11\-21 | 2026\-11\-21T10:00:11\.249744\+00:00 | UAC | 55\.6 |
| 105\.19256583056404 | 109\.22031061595314 | 68\.01283959545437 | 0\.6063763811151638 | 2026\-11\-24 | 2026\-11\-24T10:00:26\.869200\+00:00 | MVC | 46\.3 |
| 100\.12661450977834 | 114\.21083208066557 | 69\.40981690027397 | 0\.8195825902807369 | 2026\-11\-23 | 2026\-11\-23T10:00:19\.478972\+00:00 | BSth | 44\.8 |
| 109\.27402540277279 | 95\.51073065665929 | 64\.88465812208749 | 0\.17535632234862175 | 2026\-11\-22 | 2026\-11\-22T10:00:11\.099154\+00:00 | NEC | 53\.8 |
| 106\.41528281636832 | 103\.56965113508844 | 68\.4906476858051 | 0\.4226984111045624 | 2026\-11\-17 | 2026\-11\-17T10:01:02\.490697\+00:00 | Sum | 41 |

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
