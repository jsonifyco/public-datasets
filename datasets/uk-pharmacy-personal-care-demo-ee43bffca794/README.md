# UK Toothpaste Prices: Boots, Superdrug and Well Pharmacy

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Compare ordinary single\-item GBP prices for three named 75ml toothpaste variants at Boots UK, Superdrug and Well Pharmacy, with source links and qualified availability\.

[Get the full dataset for free](https://www.jsonify.com/datasets/uk-pharmacy-personal-care-demo-ee43bffca794?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-10-26T12:35:41.997095Z

## The brief

> I need this data: Compare ordinary single\-item GBP prices for three named 75ml toothpaste variants at Boots UK, Superdrug and Well Pharmacy, with source links and qualified availability\.

Summary from the public dataset description.

## UK pharmacy personal care prices / offers

9 total rows · 9 sampled · Output revision 1
Published: 2026-10-26T12:35:41.997095Z · Producing pipeline version: 1

[CSV sample](outputs/c12f0a6b49b4/offers-92ab364e8f43/sample.csv) · [JSON sample](outputs/c12f0a6b49b4/offers-92ab364e8f43/sample.json) · [Schema](outputs/c12f0a6b49b4/offers-92ab364e8f43/schema.json)

| availability | brand | checked\_at | price\_basis | price\_gbp | price\_per\_100ml\_gbp | product | retailer |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Source schema: InStock; stock not verified | Sensodyne | 2026\-10\-26T12:35:13\.312582\+00:00 | Public single\-item price; conditional promotions excluded | 5\.29 | 7\.05 | Sensodyne Rapid Relief Original 75ml | Superdrug |
| Source schema: InStock; stock not verified | Euthymol | 2026\-10\-26T12:34:21\.780477\+00:00 | Public single\-item price; conditional promotions excluded | 3 | 4 | Euthymol Original 75ml | Boots |
| Source schema: InStock; stock not verified | Sensodyne | 2026\-10\-26T12:34:11\.839558\+00:00 | Public single\-item price; conditional promotions excluded | 5\.3 | 7\.07 | Sensodyne Rapid Relief Original 75ml | Boots |
| Source schema: InStock; stock not verified | Sensodyne | 2026\-10\-26T12:34:38\.016907\+00:00 | Public single\-item price; conditional promotions excluded | 5 | 6\.67 | Sensodyne Rapid Relief Original 75ml | Well Pharmacy |
| Source schema: InStock; stock not verified | Sensodyne | 2026\-10\-26T12:33:55\.395784\+00:00 | Public single\-item price; conditional promotions excluded | 5\.49 | 7\.32 | Sensodyne Pronamel Daily Protection 75ml | Superdrug |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| availability | text |
| brand | text |
| checked\_at | text |
| price\_basis | text |
| price\_gbp | double precision |
| price\_per\_100ml\_gbp | double precision |
| product | text |
| retailer | text |
| retailer\_notes | text |
| size\_ml | integer |
| source\_product\_name | text |
| source\_url | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["offers"]
  n1["panel"]
  n2["collect"]
  n3["validate"]
  n4["offers"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n0 --> n1
  n0 --> n1
  n0 --> n2
```

- **offers**: Demo product panel\. One product URL per retailer, named variant, required and excluded title words, brand and single\-tube size in ml\. Edit or extend the panel to change the comparison\.
- **panel**: Prepare the selected toothpaste product pages from Boots, Superdrug and Well Pharmacy\.
- **collect**: Read each exact public product page and validate its named variant, 75 ml single\-tube size and ordinary GBP price\.
- **validate**: Check every selected product page is present before replacing the saved comparison snapshot\.
- **offers**: Public UK personal\-care offer snapshot, matched by named variant and pack size\. Stock is not verified\.

## Version history

- 2026-10-26T12:33:24.604947Z: v1: Added a refreshable nine\-offer toothpaste demo comparing Boots UK, Superdrug and Well Pharmacy, with product links and clearly qualified availability\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/uk-pharmacy-personal-care-demo-ee43bffca794?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
