# UK and Irish Horse Racing Odds

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

UK and Irish horse racing odds data\. The published dataset contains 21,120 rows in total, all in the odds table, with fields describing races, runners, bookmakers, prices and collection times\.

[Get the full dataset for free](https://www.jsonify.com/datasets/dilantix-uk-irish-horse-racing-odds-37c92430d0aa?action=get) — CSV or JSON · Email required

- Refresh: hourly
- Active pipeline version: 3
- Last published: 2026-11-07T20:17:21.654187Z

## The brief

> I need this data: UK and Irish horse racing odds data\. The published dataset contains 21,120 rows in total, all in the odds table, with fields describing races, runners, bookmakers, prices and collection times\.

Summary from the public dataset description.

## Dilantix Horse Racing Odds / odds

21,120 total rows · 50 sampled · Output revision 13
Published: 2026-11-07T20:17:21.654187Z · Producing pipeline version: 3

[CSV sample](outputs/eb5416d66779/odds-1fd5faa9b5cf/sample.csv) · [JSON sample](outputs/eb5416d66779/odds-1fd5faa9b5cf/sample.json) · [Schema](outputs/eb5416d66779/odds-1fd5faa9b5cf/schema.json)

| bookmaker | collected\_at | country | course | each\_way\_terms | jockey | phase\_basis | price\_phase |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Coral | 2026\-11\-07T09:19:44\.451221\+00:00 | UK | Southwell | 1/5 odds, 3 places | H Crouch | before\_scheduled\_start; no\_source\_result\_or\_in\_play\_marker | pre\_race |
| Sky Bet | 2026\-11\-07T17:20:48\.536105\+00:00 | UK | Kelso | 1/5 odds, 4 places | Jack Power \(5\) | source\_result\_present | post\_race |
| Bet365 | 2026\-11\-07T09:19:53\.802730\+00:00 | UK | Southwell | 1/5 odds, 4 places | Daniel Muscutt | before\_scheduled\_start; no\_source\_result\_or\_in\_play\_marker | pre\_race |
| William Hill | 2026\-11\-07T09:19:08\.537108\+00:00 | UK | Doncaster | 1/5 odds, 5 places | Rossa Ryan | before\_scheduled\_start; no\_source\_result\_or\_in\_play\_marker | pre\_race |
| Sky Bet | 2026\-11\-07T10:31:53\.869725\+00:00 | UK | Kelso | 1/5 odds, 4 places | Jamie Brace \(5\) | before\_scheduled\_start; no\_source\_result\_or\_in\_play\_marker | pre\_race |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| bookmaker | text |
| collected\_at | text |
| country | text |
| course | text |
| each\_way\_terms | text |
| jockey | text |
| phase\_basis | text |
| price\_phase | text |
| race\_date | text |
| race\_name | text |
| race\_time | text |
| runner\_name | text |
| runner\_number | text |
| trainer | text |
| win\_odds\_decimal | text |
| win\_odds\_fractional | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["discover#95;races"]
  n1["collect#95;odds"]
  n2["odds"]
  n0 --> n1
  n1 --> n2
```

- **discover\_races**: Find every UK and Irish race listed for today on Oddschecker\.
- **collect\_odds**: Read the eight named bookmakers' displayed win prices and match each runner to its racecard details\.
- **odds**: Displayed bookmaker win odds via Oddschecker\. Past races retain last displayed prices and are not live offers\. Blank odds mean no numeric price shown\.

## Version history

- 2026-11-06T18:44:18.991626Z: v1: Added daily UK and Irish runner odds across the eight requested sportsbooks using Oddschecker fallback, with jockey, trainer, each\-way terms and timestamped history\.
- 2026-11-06T20:20:21.089750Z: v2: Added explicit price\-phase flags and hourly collection within the racing day\. Manual after\-hours snapshots remain available without changing scheduled defaults\.
- 2026-11-07T09:18:49.254691Z: v3: Repeated links to the same race no longer stop the odds update\. Conflicting race details still stop collection for checking\.

## Recorded repairs

- 2026-11-07T09:16:28.327425Z: no change
- 2026-11-07T09:18:58.521830Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/dilantix-uk-irish-horse-racing-odds-37c92430d0aa?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
