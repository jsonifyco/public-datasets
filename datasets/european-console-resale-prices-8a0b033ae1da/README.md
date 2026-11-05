# European Console Resale Prices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Console listing price observations with condition, sale status, model matching and euro\-converted prices\. The published dataset contains 410 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/european-console-resale-prices-8a0b033ae1da?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 2
- Last published: 2026-11-05T15:04:19.911305Z

## The brief

> I need this data: Console listing price observations with condition, sale status, model matching and euro\-converted prices\. The published dataset contains 410 rows\.

Summary from the public dataset description.

## European console resale prices / prices

410 total rows · 50 sampled · Output revision 2
Published: 2026-11-05T15:04:19.911305Z · Producing pipeline version: 2

[CSV sample](outputs/100624b69213/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/100624b69213/prices-fe81f9390ffe/sample.json) · [Schema](outputs/100624b69213/prices-fe81f9390ffe/schema.json)

| observation\_id | model | match\_key | match\_status | title | image\_url | image\_urls | image\_status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| e6e10860fd5216f6ffaf4c2c99c65632385877afd876c2c9d6834cbd6a8afb15 | ps5 original 825 disc | ps5\|original\|825\|disc | matched | Sony Playstation PS5 console disc version CFI\-1215A low firmware sealed new\! | [https://images1\.vinted\.net/t/02\_01b6a\_gXNHbsdecgPYNvv4GXcjTcQf/f800/7ded4980\.webp?s=55a3fa0b7a479f4fe5c60d7211335b86aaedbc39](<https://images1.vinted.net/t/02_01b6a_gXNHbsdecgPYNvv4GXcjTcQf/f800/7ded4980.webp?s=55a3fa0b7a479f4fe5c60d7211335b86aaedbc39>) | \["[https://images1\.vinted\.net/t/02\_01b6a\_…](<https://images1.vinted.net/t/02_01b6a_%E2%80%A6>) | available |
| 6ee79117a12fa180c10fa82e72dc24244026742c1c080e005cdd572253e38054 | ps5 | None | unresolved | PS5\.\. | [https://images1\.vinted\.net/t/03\_00d2d\_EPWLCbZ9Eqy9P2ScTtks5TQQ/f800/f49d5fc4\.webp?s=2bb02b6f408d2974d948d8f55cf4a0645286b3c3](<https://images1.vinted.net/t/03_00d2d_EPWLCbZ9Eqy9P2ScTtks5TQQ/f800/f49d5fc4.webp?s=2bb02b6f408d2974d948d8f55cf4a0645286b3c3>) | \["[https://images1\.vinted\.net/t/03\_00d2d\_…](<https://images1.vinted.net/t/03_00d2d_%E2%80%A6>) | available |
| 1cc5b804dd9218419c85e63ddc10d89dfd3f4c0bc77409e2d275a18ba026b90d | ps5 original 825 disc | ps5\|original\|825\|disc | matched | Sony PlayStation 5 z napędem \(CFI\-1116A\) \+ PS VR2 \+ 2x DualSense \+ 9 Gier | [https://ireland\.apollo\.olxcdn\.com:443/v1/files/pcmhpxe5mf873\-PL/image;s=1200x0](<https://ireland.apollo.olxcdn.com:443/v1/files/pcmhpxe5mf873-PL/image;s=1200x0>) | \["[https://ireland\.apollo\.olxcdn\.com:443/…](<https://ireland.apollo.olxcdn.com:443/%E2%80%A6>) | available |
| db829f11b014c036a557ea443dd4a822e3c7a469f95a20ce3ad7e0e9d05ee93c | ps5 | None | unresolved | Ps5 neu mit 20 monate garantie | [https://images1\.vinted\.net/t/03\_00d24\_SRdjaBHi7q98mAzimjCdzCgW/f800/d0aa9863\.webp?s=4f7ccaa6bb967c7ac1fedd2ac0b15d3c9a486c14](<https://images1.vinted.net/t/03_00d24_SRdjaBHi7q98mAzimjCdzCgW/f800/d0aa9863.webp?s=4f7ccaa6bb967c7ac1fedd2ac0b15d3c9a486c14>) | \["[https://images1\.vinted\.net/t/03\_00d24\_…](<https://images1.vinted.net/t/03_00d24_%E2%80%A6>) | available |
| baa2268eb33839805af99375324510208b0bb79244793aeda707f486297daf1f | ps5 disc | None | unresolved | PS5 \+ FC25 \+1 Controller \(Pretul este NEGOCIABIL\) | [https://frankfurt\.apollo\.olxcdn\.com:443/v1/files/wbygl5rudn2r3\-RO/image;s=1200x0](<https://frankfurt.apollo.olxcdn.com:443/v1/files/wbygl5rudn2r3-RO/image;s=1200x0>) | \["[https://frankfurt\.apollo\.olxcdn\.com:44…](<https://frankfurt.apollo.olxcdn.com:44%E2%80%A6>) | available |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| observation\_id | text |
| model | text |
| match\_key | text |
| match\_status | text |
| title | text |
| image\_url | text |
| image\_urls | jsonb |
| image\_status | text |
| condition | text |
| condition\_original | text |
| price | double precision |
| currency | text |
| price\_eur | double precision |
| listed\_date | text |
| listed\_date\_text | text |
| sold\_or\_removed\_date | text |
| sale\_status | text |
| source | text |
| country | text |
| market\_country | text |
| source\_url | text |
| source\_model\_number | text |
| is\_bundle | boolean |
| best\_offer\_accepted | boolean |
| comparison\_eligible | boolean |
| identity\_evidence | text |
| price\_evidence | text |
| date\_note | text |
| observed\_at | text |
| fx\_date | text |
| fx\_units\_per\_eur | double precision |

## How the pipeline works

```mermaid
flowchart LR
  n0["prepare"]
  n1["discover"]
  n2["expand"]
  n3["read#95;listing"]
  n4["validate"]
  n5["prices"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
```

- **prepare**: Prepare the selected European marketplace searches and read current European Central Bank exchange rates\.
- **discover**: Read each selected marketplace search and find genuine console listings, excluding accessories and wanted ads\.
- **expand**: Keep source identity on each discovered listing so detail reads can be checked and resumed independently\.
- **read\_listing**: Verify the primary console, condition, price and visible dates on each exact listing page\.
- **validate**: Deduplicate listings and require coverage of every selected market before publishing a weekly price observation\.
- **prices**: Weekly exact\-model console asking and sold\-price observations, with source links and EUR conversion\.

## Version history

- 2026-11-05T14:04:45.743497Z: v1: Adds a weekly console\-price demo across European marketplaces, with eBay US sold prices alongside\. Records exact model matches, condition, euro prices and visible dates\.
- 2026-11-05T14:37:30.871629Z: v2: Adds listing photos and standardized condition categories while retaining original condition wording\. Improves larger listing selections so each saved link comes directly from the source\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/european-console-resale-prices-8a0b033ae1da?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
