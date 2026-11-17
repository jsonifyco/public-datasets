# Prevailing Wage Rates: California, Washington, Missouri and New York

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Published prevailing wage rates for public works in California, Washington, Missouri and New York, with basic, fringe and total hourly rates where available\. Dataset snapshot: 17 November 2026; 44,264 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/prevailing-wage-rates-us-states-47b2aa83a625?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 2
- Last published: 2026-11-17T06:26:08.099606Z

## The brief

> I need this data: Published prevailing wage rates for public works in California, Washington, Missouri and New York, with basic, fringe and total hourly rates where available\. Dataset snapshot: 17 November 2026; 44,264 rows\.

Summary from the public dataset description.

## Prevailing wage rates \(US states\) / rates

44,264 total rows · 50 sampled · Output revision 6
Published: 2026-11-17T06:26:08.099606Z · Producing pipeline version: 2

[CSV sample](outputs/209ff3a0d0d7/rates-ff24aad2c015/sample.csv) · [JSON sample](outputs/209ff3a0d0d7/rates-ff24aad2c015/sample.json) · [Schema](outputs/209ff3a0d0d7/rates-ff24aad2c015/schema.json)

| basic\_hourly\_rate\_usd | classification | county\_or\_area | determination\_id | effective\_date | expiration\_date | first\_seen\_date | fringe\_benefits\_hourly\_usd |
| --- | --- | --- | --- | --- | --- | --- | --- |
| None | Building Construction: Linoleum Layers &amp; Cutter | Johnson | Annual Wage Order No\. 33 | 2026\-05\-29 | None | 2026\-11\-12 | None |
| None | Building Construction: Operating Engineer \- Group IV | Polk | Annual Wage Order No\. 33 | 2026\-05\-29 | None | 2026\-11\-12 | None |
| 42\.59 | Barrier machine: \(Zipper\) | Spokane | None | 2026\-09\-02 | None | 2026\-11\-12 | 25\.42 |
| 58\.18 | Concrete Finish Machine \- Laser Screed | Island | None | 2026\-09\-02 | None | 2026\-11\-12 | 30\.03 |
| None | Building Construction: Operating Engineer \- Group I | Cole | Annual Wage Order No\. 33 | 2026\-05\-29 | None | 2026\-11\-12 | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| basic\_hourly\_rate\_usd | double precision |
| classification | text |
| county\_or\_area | text |
| determination\_id | text |
| effective\_date | text |
| expiration\_date | text |
| first\_seen\_date | text |
| fringe\_benefits\_hourly\_usd | double precision |
| overtime\_hourly\_rate\_usd | double precision |
| source\_name | text |
| source\_url | text |
| state | text |
| total\_hourly\_rate\_usd | double precision |
| trade | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["existing#95;rates"]
  n1["rate#95;documents"]
  n2["source#95;sections"]
  n3["discover#95;documents"]
  n4["unique#95;documents"]
  n5["search#95;remaining#95;pages"]
  n6["prepare#95;rate#95;documents"]
  n7["read#95;rates"]
  n8["validate#95;rates"]
  n9["rates"]
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n6 --> n7
  n7 --> n8
  n8 --> n9
  n0 --> n2
  n1 --> n2
  n1 --> n6
  n0 --> n8
```

- **existing\_rates**: Previously published rates\. Empty only for the first backfill; later refreshes read the saved rates table\.
- **rate\_documents**: Optional saved official\-document manifest to reuse established discovery without repeating searches\.
- **source\_sections**: Read the public New York county selector and prepare the four states and California regional indexes\.
- **discover\_documents**: Discover current county wage orders, regional craft PDFs, Washington county queries and New York schedules\.
- **unique\_documents**: Deduplicate shared schedules before collection, retaining each public determination once\.
- **search\_remaining\_pages**: Read additional New York search pages and California pages linking predetermined increases\.
- **prepare\_rate\_documents**: Remove repeated New York schedules and order independent documents for small checkpointed batches\.
- **read\_rates**: Read each county or craft document, extract journey rates, and skip and count unreadable documents\.
- **validate\_rates**: Check required fields and unique rate keys before saving source\-confirmed journey rates\.
- **rates**: Journey\-level prevailing wage rates from four state labour departments\.

## Version history

- 2026-11-12T09:31:51.788180Z: v1: Fill Washington and New York hourly benefits and add California’s published predetermined wage increases\. Keep rates unique, update corrections and preserve first\-seen dates\.
- 2026-11-12T10:03:17.272642Z: v2: Corrected saved\-table merging so each five\-field key stays unique\. Monthly limits now count new keys only, while allowing corrections\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/prevailing-wage-rates-us-states-47b2aa83a625?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
