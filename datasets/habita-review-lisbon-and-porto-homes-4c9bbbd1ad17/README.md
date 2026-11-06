# Lisbon and Porto Home Listings and Prices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Residential listings for rent and sale in Lisbon and Porto, with prices, property details, address text and observation timestamps\. The published dataset contains 394 listing observations\.

[Get the full dataset for free](https://www.jsonify.com/datasets/habita-review-lisbon-and-porto-homes-4c9bbbd1ad17?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 3
- Last published: 2026-11-06T21:02:38.294938Z

## The brief

> I need this data: Residential listings for rent and sale in Lisbon and Porto, with prices, property details, address text and observation timestamps\. The published dataset contains 394 listing observations\.

Summary from the public dataset description.

## Habita Review residential listings / observations

394 total rows · 50 sampled · Output revision 2
Published: 2026-11-06T21:02:38.294938Z · Producing pipeline version: 3

[CSV sample](outputs/945895408abe/observations-bfc5a6b45b6a/sample.csv) · [JSON sample](outputs/945895408abe/observations-bfc5a6b45b6a/sample.json) · [Schema](outputs/945895408abe/observations-bfc5a6b45b6a/schema.json)

| address\_evidence | address\_precision | area\_m2 | bathrooms | bedrooms | building\_id | building\_listing\_count | building\_number |
| --- | --- | --- | --- | --- | --- | --- | --- |
| None | None | 35 | 1 | 1 | None | None | None |
| None | None | 98 | 1 | 2 | None | None | None |
| None | None | 30 | 1 | 0 | None | None | None |
| None | None | 87 | 1 | 2 | None | None | None |
| None | None | 113\.98 | 2 | 3 | None | None | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| address\_evidence | text |
| address\_precision | text |
| area\_m2 | double precision |
| bathrooms | integer |
| bedrooms | integer |
| building\_id | text |
| building\_listing\_count | integer |
| building\_number | text |
| building\_portal\_count | integer |
| building\_unit\_hints | text |
| collected\_at | text |
| data\_quality\_notes | jsonb |
| description\_address\_text | text |
| description\_gross\_area\_m2 | double precision |
| description\_typology | text |
| energy\_rating | text |
| first\_seen | text |
| floor | text |
| last\_seen | text |
| latitude | double precision |
| listing\_id | text |
| listing\_url | text |
| longitude | double precision |
| municipality | text |
| operation | text |
| parish\_freguesia | text |
| price\_eur | double precision |
| price\_per\_m2 | double precision |
| selected\_parish | text |
| snapshot\_at | text |
| source | text |
| source\_address\_text | text |
| street\_address\_text | text |
| street\_id | text |
| street\_listing\_count | integer |
| street\_name | text |
| street\_portal\_count | integer |
| typology | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["search#95;plan"]
  n1["discover"]
  n2["expand#95;listings"]
  n3["property#95;details"]
  n4["validate#95;coverage"]
  n5["observations"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
```

- **search\_plan**: Prepare Lisbon and Porto rent and sale searches on Idealista and Imovirtual, covering apartments and houses\.
- **discover**: Read ranked residential search results and select a bounded T0 to T4 sample, verifying source, municipality and operation\.
- **expand\_listings**: Flatten the selected listings and remove repeated source identities before reading each property page\.
- **property\_details**: Read each listing’s current EUR price, residential features and most precise published address without inferring a hidden location\.
- **validate\_coverage**: Verify that both portals, both cities and both operations have useful rows, then append timestamped observations for price history\.
- **observations**: Daily source listing observations\. Compare prices by source and listing identity over collected\_at; map pins may be approximate\.

## Version history

- 2026-11-06T19:13:46.174758Z: v1: Added daily residential listing samples with exposed addresses and retained price observations\.
- 2026-11-06T20:37:25.708116Z: v2: Expanded the daily address demo to nine parishes and a target of 360 listings, with precise address recovery, source\-conflict flags and conservative street/building groups\.
- 2026-11-06T20:52:03.942181Z: v3: Fixed duplicate Imovirtual search entries so one property keeps one verified identity and does not interrupt the daily update\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/habita-review-lisbon-and-porto-homes-4c9bbbd1ad17?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
