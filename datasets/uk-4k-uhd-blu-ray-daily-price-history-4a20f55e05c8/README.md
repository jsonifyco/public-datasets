# HMV and Rarewaves data: UK 4K Blu\-ray price dataset

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

UK 4K UHD Blu\-ray prices from HMV and Rarewaves, including prices in GBP, displayed was/RRP prices, advertised offers and stock status\. Export the price data to CSV, Excel or Google Sheets\.

[Get the full dataset for free](https://www.jsonify.com/datasets/uk-4k-uhd-blu-ray-daily-price-history-4a20f55e05c8?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 1
- Last published: 2026-11-28T09:03:24.527219Z

## The brief

> I need this data: UK 4K UHD Blu\-ray prices from HMV and Rarewaves, including prices in GBP, displayed was/RRP prices, advertised offers and stock status\. Export the price data to CSV, Excel or Google Sheets\.

Summary from the public dataset description.

## UK 4K UHD Blu\-ray Price History / price\_history

1,020 total rows · 50 sampled · Output revision 10
Published: 2026-11-28T09:03:24.527219Z · Producing pipeline version: 1

[CSV sample](outputs/1468933064cd/price-history-3b9b0d17ff6d/sample.csv) · [JSON sample](outputs/1468933064cd/price-history-3b9b0d17ff6d/sample.json) · [Schema](outputs/1468933064cd/price-history-3b9b0d17ff6d/schema.json)

| advertised\_discount\_pct | advertised\_offer | capture\_date | captured\_at | edition\_note | format | in\_stock | observation\_key |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 20 | 20% Off \- Use Code HIDEF20 | 2026\-11\-25 | 2026\-11\-25T09:00:28\.192798\+00:00 | Gremlins | 4K Ultra HD Blu\-ray | False | 2026\-11\-25T09:00:28\.192798\+00:00\|HMV\|591297 |
| 20 | 20% Off \- Use Code HIDEF20 | 2026\-11\-26 | 2026\-11\-26T09:01:06\.939648\+00:00 | House of the Dragon: Season 2 \(hmv Exclusive\) | 4K Ultra HD Blu\-ray | False | 2026\-11\-26T09:01:06\.939648\+00:00\|HMV\|453130 |
| None | 3 For £50 4K Ultra HD | 2026\-11\-26 | 2026\-11\-26T09:01:06\.939648\+00:00 | Blade Runner 2049 | 4K Ultra HD Blu\-ray | True | 2026\-11\-26T09:01:06\.939648\+00:00\|HMV\|693691 |
| None | Limited Edition SteelBook | 2026\-11\-21 | 2026\-11\-21T09:00:23\.730736\+00:00 | Clayface \(hmv Exclusive\) Limited Edition 4K Ultra HD SteelBook | 4K Ultra HD Blu\-ray | False | 2026\-11\-21T09:00:23\.730736\+00:00\|HMV\|849047 |
| None | 3 For £50 4K Ultra HD | 2026\-11\-20 | 2026\-11\-20T09:00:18\.517247\+00:00 | Oppenheimer | 4K Ultra HD Blu\-ray | True | 2026\-11\-20T09:00:18\.517247\+00:00\|HMV\|109233 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| advertised\_discount\_pct | double precision |
| advertised\_offer | text |
| capture\_date | text |
| captured\_at | text |
| edition\_note | text |
| format | text |
| in\_stock | boolean |
| observation\_key | text |
| price\_gbp | double precision |
| product\_url | text |
| rank | integer |
| store | text |
| store\_product\_id | text |
| title | text |
| was\_rrp\_gbp | double precision |

## How the pipeline works

```mermaid
flowchart LR
  n0["prior#95;captures"]
  n1["stores"]
  n2["ranked#95;titles"]
  n3["refresh#95;retained"]
  n4["price#95;history"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n0 --> n1
  n0 --> n2
```

- **prior\_captures**: Previously captured product identities to retain when importing an earlier capture; empty for a new tracker\.
- **stores**: Start a fresh UTC capture for HMV and Rarewaves\.
- **ranked\_titles**: Read each store’s bestselling 4K selection and retain every title seen on earlier days\.
- **refresh\_retained**: Reuse today’s ranked prices and revisit product pages for titles that dropped out of the chart\.
- **price\_history**: Daily GBP price observations, preserving earlier captures and separately recording retailer reference prices\.

## Version history

- 2026-11-19T11:19:41.748123Z: v1: Adds daily HMV and Rarewaves 4K UHD price history and keeps refreshing previously captured titles\.

## Recorded repairs

- 2026-11-21T09:01:25.276218Z: no change
- 2026-11-21T09:01:54.639560Z: repaired
- 2026-11-21T09:03:15.088066Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/uk-4k-uhd-blu-ray-daily-price-history-4a20f55e05c8?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
