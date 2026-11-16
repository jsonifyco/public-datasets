# NCAA Division I Men's Basketball Advanced Stats

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

NCAA Division I men's basketball advanced stats with team records, adjusted efficiencies, tempo, Barthag, four factors and three\-point metrics\. Published dataset: 365 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/ncaa-division-i-men-s-basketball-advanced-stats-2026-27-5a06355b5589?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 1
- Last published: 2026-11-16T09:15:30.422120Z

## The brief

> I need this data: NCAA Division I men's basketball advanced stats with team records, adjusted efficiencies, tempo, Barthag, four factors and three\-point metrics\. Published dataset: 365 rows\.

Summary from the public dataset description.

## NCAA Division I Men's Basketball Advanced Stats 2026–27 / team\_captures

365 total rows · 50 sampled · Output revision 1
Published: 2026-11-16T09:15:30.422120Z · Producing pipeline version: 1

[CSV sample](outputs/3c02706620bf/team-captures-b62e049933b3/sample.csv) · [JSON sample](outputs/3c02706620bf/team-captures-b62e049933b3/sample.json) · [Schema](outputs/3c02706620bf/team-captures-b62e049933b3/schema.json)

| adjusted\_defensive\_efficiency | adjusted\_offensive\_efficiency | adjusted\_tempo | barthag | capture\_date | captured\_at | conference | def\_efg\_pct |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 98\.56546060030439 | 112\.4518321742314 | 70\.57929659355834 | 0\.8199113209912104 | 2026\-11\-16 | 2026\-11\-16T09:15:24\.866383\+00:00 | B12 | 46\.7 |
| 108\.05101750806 | 105\.39216980201101 | 68\.23014942820473 | 0\.42885498710330533 | 2026\-11\-16 | 2026\-11\-16T09:15:24\.866383\+00:00 | SB | 45\.1 |
| 104\.17212268715446 | 110\.04808668166967 | 68\.99358459224092 | 0\.6527247763391655 | 2026\-11\-16 | 2026\-11\-16T09:15:24\.866383\+00:00 | MVC | 54\.1 |
| 107\.42347374225122 | 98\.36311800221372 | 69\.8791867336541 | 0\.2663350677991396 | 2026\-11\-16 | 2026\-11\-16T09:15:24\.866383\+00:00 | Metro | 52\.3 |
| 104\.15812338304747 | 112\.92573162367566 | 72\.09466521234116 | 0\.7169600943461305 | 2026\-11\-16 | 2026\-11\-16T09:15:24\.866383\+00:00 | B10 | 46\.2 |

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
