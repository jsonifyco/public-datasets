# HMV and Rarewaves data: UK 4K UHD Blu\-ray price dataset, refreshed daily

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Daily UK 4K UHD Blu\-ray prices from HMV and Rarewaves: price in GBP, was/RRP price, advertised discount and stock for bestsellers and every title seen before\. Export to CSV, Excel or Google Sheets\.

[Get the full dataset for free](https://www.jsonify.com/datasets/uk-4k-uhd-blu-ray-daily-price-history-4a20f55e05c8?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 1
- Last published: 2026-11-19T11:29:27.800550Z

## The brief

> I need this data: Daily UK 4K UHD Blu\-ray prices from HMV and Rarewaves: price in GBP, was/RRP price, advertised discount and stock for bestsellers and every title seen before\. Export to CSV, Excel or Google Sheets\.

Summary from the public dataset description.

## UK 4K UHD Blu\-ray Price History / price\_history

80 total rows · 10 sampled · Output revision 1
Published: 2026-11-19T11:29:27.800550Z · Producing pipeline version: 1

[CSV sample](outputs/1468933064cd/price-history-3b9b0d17ff6d/sample.csv) · [JSON sample](outputs/1468933064cd/price-history-3b9b0d17ff6d/sample.json) · [Schema](outputs/1468933064cd/price-history-3b9b0d17ff6d/schema.json)

| advertised\_discount\_pct | advertised\_offer | capture\_date | captured\_at | edition\_note | format | in\_stock | observation\_key |
| --- | --- | --- | --- | --- | --- | --- | --- |
| None | 3 For £50 4K Ultra HD | 2026\-11\-19 | 2026\-11\-19T11:28:51\.387963\+00:00 | Aliens | 4K Ultra HD Blu\-ray | True | 2026\-11\-19T11:28:51\.387963\+00:00\|HMV\|106535 |
| None | None | 2026\-11\-19 | 2026\-11\-19T11:28:51\.387963\+00:00 | Troy Limited Edition | 4K Ultra HD Blu\-ray | True | 2026\-11\-19T11:28:51\.387963\+00:00\|HMV\|784120 |
| 6 | Save 6% | 2026\-11\-19 | 2026\-11\-19T11:28:51\.387963\+00:00 | Limited Edition | 4K Ultra HD | True | 2026\-11\-19T11:28:51\.387963\+00:00\|Rarewaves\|5027035029863 |
| None | None | 2026\-11\-19 | 2026\-11\-19T11:28:51\.387963\+00:00 | Pulp: What Do You Do for an Encore? | 4K Ultra HD | False | 2026\-11\-19T11:28:51\.387963\+00:00\|Rarewaves\|5060696221429 |
| None | None | 2026\-11\-19 | 2026\-11\-19T11:28:51\.387963\+00:00 | Steelbook | 4K Ultra HD | True | 2026\-11\-19T11:28:51\.387963\+00:00\|Rarewaves\|5056719202476 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| advertised\_discount\_pct | integer |
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

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/uk-4k-uhd-blu-ray-daily-price-history-4a20f55e05c8?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
