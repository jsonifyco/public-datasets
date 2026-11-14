# Marktplaats Car Dealers

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Marktplaats car dealer dataset with seller profiles, locations, membership tenure and active listing counts\. The published table contains 50 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/marktplaats-car-dealers-16546ec450b2?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 2
- Last published: 2026-11-14T18:18:27.556780Z

## The brief

> I need this data: Marktplaats car dealer dataset with seller profiles, locations, membership tenure and active listing counts\. The published table contains 50 rows\.

Summary from the public dataset description.

## Marktplaats car dealers / sellers

50 total rows · 10 sampled · Output revision 1
Published: 2026-11-14T18:18:27.556780Z · Producing pipeline version: 2

[CSV sample](outputs/1aa6bc551c5b/sellers-02dc9cc87f93/sample.csv) · [JSON sample](outputs/1aa6bc551c5b/sellers-02dc9cc87f93/sample.json) · [Schema](outputs/1aa6bc551c5b/sellers-02dc9cc87f93/schema.json)

| active\_listing\_count | category | collected\_at | location | member\_since | seller\_name | seller\_profile\_url | seller\_type |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 6 | Auto's | 2026\-11\-14T18:17:48\.007771\+00:00 | Rijssen | 11 jaar | V\.O\.F\. Autoservice Jan ten Hove | [https://www\.marktplaats\.nl/u/v\-o\-f\-autoservice\-jan\-ten\-hove/22607457/](<https://www.marktplaats.nl/u/v-o-f-autoservice-jan-ten-hove/22607457/>) | business |
| 31 | Auto's | 2026\-11\-14T18:17:30\.433792\+00:00 | Rijssen | 11 jaar | TCK Automotive | [https://www\.marktplaats\.nl/u/tck\-automotive/23015711/](<https://www.marktplaats.nl/u/tck-automotive/23015711/>) | business |
| 40 | Auto's | 2026\-11\-14T18:17:39\.877579\+00:00 | Hillegom | 16 jaar | Autocentrum Rijnland | [https://www\.marktplaats\.nl/u/autocentrum\-rijnland/14415863/](<https://www.marktplaats.nl/u/autocentrum-rijnland/14415863/>) | business |
| 79 | Auto's | 2026\-11\-14T18:17:54\.109141\+00:00 | Wergea | 18 jaar | Autobedrijf W\. van de Zweep | [https://www\.marktplaats\.nl/u/autobedrijf\-w\-van\-de\-zweep/9625496/](<https://www.marktplaats.nl/u/autobedrijf-w-van-de-zweep/9625496/>) | business |
| 19 | Auto's | 2026\-11\-14T18:17:35\.374431\+00:00 | 's\-Gravenhage | 16 jaar | Dream Motors BV | [https://www\.marktplaats\.nl/u/dream\-motors\-bv/15052744/](<https://www.marktplaats.nl/u/dream-motors-bv/15052744/>) | business |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| active\_listing\_count | integer |
| category | text |
| collected\_at | text |
| location | text |
| member\_since | text |
| seller\_name | text |
| seller\_profile\_url | text |
| seller\_type | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["discover"]
  n1["seller"]
  n2["sample"]
  n3["sellers"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **discover**: Find distinct sellers in the business\-filtered Auto's category, following category result pages\.
- **seller**: Verify professional dealer status on a car listing, then read the seller's unfiltered active stock total\.
- **sample**: Keep one row per seller, select the requested sample size, and sort by active listing total\.
- **sellers**: Professional car dealers discovered in Marktplaats Auto's, with each seller's total active listings\.

## Version history

- 2026-11-14T18:15:15.389950Z: v1: Add a weekly\-refresh sample of professional Marktplaats car dealers with current active listing totals\.
- 2026-11-14T18:16:54.245510Z: v2: Restrict the demo to professional dealerships, excluding personal accounts even if their advertisements are business\-labelled\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/marktplaats-car-dealers-16546ec450b2?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
