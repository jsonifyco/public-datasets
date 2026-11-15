# Online Businesses for Sale

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Online businesses for sale: listing details include asking prices, revenue, profit, traffic, business type, and marketplace\. The published dataset contains 214 listing rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/online-businesses-for-sale-058b5903d847?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 1
- Last published: 2026-11-15T08:19:47.393668Z

## The brief

> I need this data: Online businesses for sale: listing details include asking prices, revenue, profit, traffic, business type, and marketplace\. The published dataset contains 214 listing rows\.

Summary from the public dataset description.

## Online businesses for sale / listings

214 total rows · 50 sampled · Output revision 1
Published: 2026-11-15T08:19:47.393668Z · Producing pipeline version: 1

[CSV sample](outputs/519131a8bf0c/listings-8a836f245cd6/sample.csv) · [JSON sample](outputs/519131a8bf0c/listings-8a836f245cd6/sample.json) · [Schema](outputs/519131a8bf0c/listings-8a836f245cd6/schema.json)

| annual\_net\_profit\_usd | annual\_revenue\_usd | asking\_price\_usd | business\_type | captured\_at | displayed\_multiple | listed\_date | listing\_id |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 57759 | 164583 | 132844 | Amazon FBA | 2026\-11\-15T08:19:41\.334519\+00:00 | 2\.3x annual SDE; 28x monthly SDE | 2026\-02\-20T20:00:00\.282Z | 91175 |
| 112627 | 752017 | 281567 | Amazon FBA | 2026\-11\-15T08:19:41\.334519\+00:00 | 2\.5x annual SDE; 30x monthly SDE | 2026\-06\-25T19:00:03\.397Z | 95477 |
| 449999 | 1660289 | 809998 | Amazon FBA | 2026\-11\-15T08:19:41\.334519\+00:00 | 1\.8x annual SDE; 22x monthly SDE | 2026\-04\-15T04:00:00\.321Z | 92512 |
| 156 | 168 | None | Content | 2026\-11\-15T08:19:41\.334519\+00:00 | None | None | 14807551 |
| 49308 | 113338 | 69031 | eCommerce, DropShipping | 2026\-11\-15T08:19:41\.334519\+00:00 | 1\.4x annual SDE; 17x monthly SDE | 2026\-09\-15T16:00:00\.302Z | 97467 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| annual\_net\_profit\_usd | double precision |
| annual\_revenue\_usd | double precision |
| asking\_price\_usd | double precision |
| business\_type | text |
| captured\_at | text |
| displayed\_multiple | text |
| listed\_date | text |
| listing\_id | text |
| listing\_url | text |
| marketplace | text |
| monetization | jsonb |
| monthly\_traffic | double precision |
| monthly\_traffic\_metric | text |
| monthly\_traffic\_period | text |
| multiple\_period | text |
| net\_profit\_period | text |
| revenue\_period | text |
| site\_age | text |
| status | text |
| title | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["sources"]
  n1["collect"]
  n2["validate"]
  n3["listings"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **sources**: Select the two public marketplaces for the current business\-for\-sale snapshot\.
- **collect**: Read all For Sale Empire Flippers listings and up to fifty newest operating Flippa businesses from public cards, skipping Flippa if access is blocked\.
- **validate**: Verify one row per marketplace listing and reject zero asking prices before saving the current snapshot\.
- **listings**: Current public business\-for\-sale listings with source periods and honest missing values\.

## Version history

- 2026-11-15T08:19:21.448953Z: v1: Add a weekly public snapshot of businesses for sale on Empire Flippers and Flippa, preserving source periods and meaningful missing values\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/online-businesses-for-sale-058b5903d847?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
