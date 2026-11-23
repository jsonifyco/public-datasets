# Marktplaats Car Dealers

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Marktplaats car dealer dataset with seller profiles, locations, membership tenure and active listing counts\. The published dataset contains 50 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/marktplaats-car-dealers-16546ec450b2?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 2
- Last published: 2026-11-23T07:02:30.734293Z

## The brief

> I need this data: Marktplaats car dealer dataset with seller profiles, locations, membership tenure and active listing counts\. The published dataset contains 50 rows\.

Summary from the public dataset description.

## Marktplaats car dealers / sellers

50 total rows · 10 sampled · Output revision 3
Published: 2026-11-23T07:02:30.734293Z · Producing pipeline version: 2

[CSV sample](outputs/1aa6bc551c5b/sellers-02dc9cc87f93/sample.csv) · [JSON sample](outputs/1aa6bc551c5b/sellers-02dc9cc87f93/sample.json) · [Schema](outputs/1aa6bc551c5b/sellers-02dc9cc87f93/schema.json)

| active\_listing\_count | category | collected\_at | location | member\_since | seller\_name | seller\_profile\_url | seller\_type |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 8 | Auto's | 2026\-11\-23T07:01:45\.982179\+00:00 | Dordrecht | 8 jaar | Autobedrijf S\.A\.E\. | [https://www\.marktplaats\.nl/u/autobedrijf\-s\-a\-e/26341241/](<https://www.marktplaats.nl/u/autobedrijf-s-a-e/26341241/>) | business |
| 3 | Auto's | 2026\-11\-23T07:01:42\.568830\+00:00 | Borne | 1 jaar | Ten Broeke Auto's | [https://www\.marktplaats\.nl/u/ten\-broeke\-auto\-s/56866112/](<https://www.marktplaats.nl/u/ten-broeke-auto-s/56866112/>) | business |
| 37 | Auto's | 2026\-11\-23T07:01:30\.140018\+00:00 | Veen | 21 jaar | MvB auto's | [https://www\.marktplaats\.nl/u/mvb\-auto\-s/1757740/](<https://www.marktplaats.nl/u/mvb-auto-s/1757740/>) | business |
| 8 | Auto's | 2026\-11\-23T07:01:18\.046752\+00:00 | Heerlen | 17 jaar | Autobedrijf John Koullen | [https://www\.marktplaats\.nl/u/autobedrijf\-john\-koullen/13833586/](<https://www.marktplaats.nl/u/autobedrijf-john-koullen/13833586/>) | business |
| 4 | Auto's | 2026\-11\-23T07:01:14\.404251\+00:00 | Langbroek | 1 jaar | Budget\-Auto's | [https://www\.marktplaats\.nl/u/budget\-auto\-s/56135109/](<https://www.marktplaats.nl/u/budget-auto-s/56135109/>) | business |

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
