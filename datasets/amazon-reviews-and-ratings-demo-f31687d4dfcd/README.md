# Amazon Product Reviews and Ratings Sample Dataset

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Sample Amazon\.com product\-page reviews and ratings for a user\-supplied ASIN list, with review text, dates, star ratings, and variant context\.

[Get the full dataset for free](https://www.jsonify.com/datasets/amazon-reviews-and-ratings-demo-f31687d4dfcd?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 2
- Last published: 2026-10-22T14:05:00.788201Z

## The brief

> I need this data: Sample Amazon\.com product\-page reviews and ratings for a user\-supplied ASIN list, with review text, dates, star ratings, and variant context\.

Summary from the public dataset description.

## Amazon reviews demo / reviews

12 total rows · 12 sampled · Output revision 1
Published: 2026-10-22T14:05:00.788201Z · Producing pipeline version: 2

[CSV sample](outputs/5e58b787efdb/reviews-546410512038/sample.csv) · [JSON sample](outputs/5e58b787efdb/reviews-546410512038/sample.json) · [Schema](outputs/5e58b787efdb/reviews-546410512038/schema.json)

| asin | body | collected\_at | country | overall\_rating | product\_title | product\_url | rating |
| --- | --- | --- | --- | --- | --- | --- | --- |
| B00T0C9XRK | I do not wear mascara very often, so this one works really… | 2026\-10\-22T14:03:30\.505573\+00:00 | United States | 4\.3 | essence Lash Princess False Lash Effect Mascara, Black \(Pack of 1\) | [https://www\.amazon\.com/dp/B00T0C9XRK](<https://www.amazon.com/dp/B00T0C9XRK>) | 5 |
| B00FLYWNYQ | I love my Instant Pot\! It’s been such a time saver in my k… | 2026\-10\-22T14:04:57\.459256\+00:00 | United States | 4\.7 | Instant Pot Duo 6 Qt 7\-in\-1 Electric Pressure Cooker, Stainless Steel | [https://www\.amazon\.com/dp/B00FLYWNYQ](<https://www.amazon.com/dp/B00FLYWNYQ>) | 5 |
| B00T0C9XRK | This mascara is awesome\. I love the brown color\. Makes my … | 2026\-10\-22T14:03:30\.505601\+00:00 | United States | 4\.3 | essence Lash Princess False Lash Effect Mascara, Black \(Pack of 1\) | [https://www\.amazon\.com/dp/B00T0C9XRK](<https://www.amazon.com/dp/B00T0C9XRK>) | 4 |
| B0014C0LUC | I have been a nurse for 20 years\. I have very wide feet an… | 2026\-10\-22T14:03:07\.752749\+00:00 | United States | 4\.8 | Crocs Unisex\-Adult Classic Clog, Clogs for Women and Men | [https://www\.amazon\.com/dp/B0014C0LUC](<https://www.amazon.com/dp/B0014C0LUC>) | 5 |
| B00T0C9XRK | Lengthens, stays on\. Doesnt smudge\. Doesnt irratiate eyes … | 2026\-10\-22T14:03:30\.505594\+00:00 | United States | 4\.3 | essence Lash Princess False Lash Effect Mascara, Black \(Pack of 1\) | [https://www\.amazon\.com/dp/B00T0C9XRK](<https://www.amazon.com/dp/B00T0C9XRK>) | 5 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| asin | text |
| body | text |
| collected\_at | text |
| country | text |
| overall\_rating | double precision |
| product\_title | text |
| product\_url | text |
| rating | double precision |
| review\_date | text |
| review\_id | text |
| review\_url | text |
| reviewed\_variant | text |
| reviewed\_variant\_asin | text |
| reviewer\_email | text |
| reviewer\_name | text |
| shopify\_product\_handle | text |
| shopify\_product\_id | text |
| source | text |
| title | text |
| total\_ratings | integer |
| variant\_match\_status | text |
| verified\_purchase | boolean |

## How the pipeline works

```mermaid
flowchart LR
  n0["asins"]
  n1["prepare"]
  n2["collect"]
  n3["validate"]
  n4["reviews"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n0 --> n1
  n0 --> n1
```

- **asins**: Amazon\.com ASINs to sample, one ASIN per row\.
- **prepare**: Validate and deduplicate the supplied Amazon\.com product identifiers\.
- **collect**: Read displayed Amazon product ratings and review cards, preserving related\-variant identity and original review dates\.
- **validate**: Remove duplicate review identifiers and validate that every saved review has text, stars, date and source link\.
- **reviews**: Selected Amazon reviews and product ratings for later Shopify product mapping\.

## Version history

- 2026-10-22T13:50:53.878857Z: v1: Added a refreshable Amazon ratings and review sample with a general staging CSV and product variant flags\.
- 2026-10-22T14:02:45.565064Z: v2: Improved collection when Amazon returns incomplete review pages, preserving the same sample and CSV fields\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/amazon-reviews-and-ratings-demo-f31687d4dfcd?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
