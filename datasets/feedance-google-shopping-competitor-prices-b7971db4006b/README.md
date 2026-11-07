# Google Shopping Competitor Prices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Google Shopping competitor prices: a published dataset with 2,755 rows across offer and coverage tables\. Offer records include product, seller, price, availability, and collection\-time fields\.

[Get the full dataset for free](https://www.jsonify.com/datasets/feedance-google-shopping-competitor-prices-b7971db4006b?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 9
- Last published: 2026-11-07T11:41:10.124982Z

## The brief

> I need this data: Google Shopping competitor prices: a published dataset with 2,755 rows across offer and coverage tables\. Offer records include product, seller, price, availability, and collection\-time fields\.

Summary from the public dataset description.

## Feedance Shopping price sample / offers

2,452 total rows · 50 sampled · Output revision 2
Published: 2026-11-07T11:41:10.124982Z · Producing pipeline version: Unknown

[CSV sample](outputs/fd6c7b3425ee/offers-92ab364e8f43/sample.csv) · [JSON sample](outputs/fd6c7b3425ee/offers-92ab364e8f43/sample.json) · [Schema](outputs/fd6c7b3425ee/offers-92ab364e8f43/schema.json)

| availability | category | collected\_at | condition | country | currency | google\_product\_id | in\_stock |
| --- | --- | --- | --- | --- | --- | --- | --- |
| In stock online | Consumer electronics | 2026\-11\-07T04:50:38\.090285\+00:00 | None | TR | TRY | 15502392820511403864 | True |
| In stock online | Consumer electronics | 2026\-11\-07T04:49:23\.812051\+00:00 | None | DE | EUR | 13734944200852901261 | True |
| In stock online | Consumer electronics | 2026\-11\-07T04:49:23\.812051\+00:00 | None | DE | EUR | 13734944200852901261 | True |
| Out of stock | Consumer electronics | 2026\-11\-07T04:49:23\.812051\+00:00 | None | DE | EUR | 13734944200852901261 | False |
| In stock online | Consumer electronics | 2026\-11\-07T04:49:23\.812051\+00:00 | None | DE | EUR | 13734944200852901261 | True |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| availability | text |
| category | text |
| collected\_at | text |
| condition | text |
| country | text |
| currency | text |
| google\_product\_id | text |
| in\_stock | boolean |
| offer\_url | text |
| original\_price\_text | text |
| price | double precision |
| product\_title | text |
| query\_gtin\_mpn | text |
| rank\_among\_offers | bigint |
| rating | double precision |
| record\_type | text |
| review\_count | bigint |
| review\_count\_display | text |
| seller\_domain | text |
| seller\_name | text |
| shipping\_cost | double precision |
| sku\_id | text |
| total\_price | double precision |

## Feedance Shopping price sample / coverage

150 total rows · 50 sampled · Output revision 2
Published: 2026-11-07T11:41:10.124982Z · Producing pipeline version: Unknown

[CSV sample](outputs/fd6c7b3425ee/coverage-c3a3091b9d32/sample.csv) · [JSON sample](outputs/fd6c7b3425ee/coverage-c3a3091b9d32/sample.json) · [Schema](outputs/fd6c7b3425ee/coverage-c3a3091b9d32/schema.json)

| canonical\_title | category | collected\_at | country | note | offers\_count | product\_groups\_checked | product\_groups\_unavailable |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Sony WH\-1000XM5 Wireless Headphones, Black | Consumer electronics | 2026\-11\-07T04:49:23\.811647\+00:00 | TR | Matching groups from initial search results, including localized Turkish discovery and keyword\-page recovery; expanded seller rows checked\. Ranking is source panel order before identity filtering\. Unknown shipping, stock or condition stays empty\. Product rating is shared by the Google group, not a seller rating\. Compact review counts retain their display text\. Country is the Google Shopping market; shipping is the displayed estimate without a supplied delivery postcode\. Original foreign\-price text is retained when shown\. | 1 | 5 | 0 |
| Sony WH\-1000XM5 Wireless Headphones, Black | Consumer electronics | 2026\-11\-07T04:49:23\.812051\+00:00 | DE | Google details were unavailable for 4 of 10 inspected product results\. Other available groups were checked; unavailable details do not imply out of stock\. | 32 | 10 | 4 |
| Sony WH\-1000XM5 Wireless Headphones, Black | Consumer electronics | 2026\-11\-07T04:53:45\.913309\+00:00 | GB | Matching groups from initial search results, including localized Turkish discovery and keyword\-page recovery; expanded seller rows checked\. Ranking is source panel order before identity filtering\. Unknown shipping, stock or condition stays empty\. Product rating is shared by the Google group, not a seller rating\. Compact review counts retain their display text\. Country is the Google Shopping market; shipping is the displayed estimate without a supplied delivery postcode\. Original foreign\-price text is retained when shown\. | 30 | 3 | 0 |
| Sony WF\-1000XM5 True Wireless Earbuds, Black | Consumer electronics | 2026\-11\-07T04:53:45\.913457\+00:00 | TR | Matching groups from initial search results, including localized Turkish discovery and keyword\-page recovery; expanded seller rows checked\. Ranking is source panel order before identity filtering\. Unknown shipping, stock or condition stays empty\. Product rating is shared by the Google group, not a seller rating\. Compact review counts retain their display text\. Country is the Google Shopping market; shipping is the displayed estimate without a supplied delivery postcode\. Original foreign\-price text is retained when shown\. | 8 | 3 | 0 |
| Sony WF\-1000XM5 True Wireless Earbuds, Black | Consumer electronics | 2026\-11\-07T04:56:00\.255479\+00:00 | DE | Google details were unavailable for 1 of 3 inspected product results\. Other available groups were checked; unavailable details do not imply out of stock\. | 23 | 3 | 1 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| canonical\_title | text |
| category | text |
| collected\_at | text |
| country | text |
| note | text |
| offers\_count | bigint |
| product\_groups\_checked | bigint |
| product\_groups\_unavailable | bigint |
| query | text |
| query\_gtin\_mpn | text |
| record\_type | text |
| sku\_id | text |
| status | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["sku#95;roster"]
  n1["markets"]
  n2["discover"]
  n3["product#95;panels"]
  n4["offers"]
  n5["reconcile"]
  n6["split"]
  n7["offers"]
  n8["coverage"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n0 --> n1
  n6 --> n8
  n6 --> n7
  n0 --> n1
```

- **sku\_roster**: Exact sample SKUs, identifiers, variants and supporting public references\. Edit this panel to track another product\.
- **markets**: Pair each selected sample SKU with Turkey, Germany and the United Kingdom\.
- **discover**: Find matching product groups in each market and resolve headline\-only results through the live keyword search page\.
- **product\_panels**: Keep matching product groups together so each SKU and country reuses one Shopping session\.
- **offers**: Read every matching product group in a shared SKU\-country session and check exact seller variants\.
- **reconcile**: Deduplicate Google offer identities and identical links and combine product\-group coverage into one SKU\-country check\.
- **split**: Keep comparable seller offers and SKU\-market coverage checks in separate worksheets\.
- **offers**: Exact\-variant seller offer observations from Google Shopping\.
- **coverage**: One check per SKU and country, including searches without verified matching offers\.

## Version history

- 2026-11-07T00:34:51.940797Z: v1: Build a fifty\-product Google Shopping price sample across Turkey, Germany and the UK, with exact\-variant checks, offer details and daily observation history\.
- 2026-11-07T01:08:07.866577Z: v2: Recover matching Shopping results that omit their product identifier through the existing country\-specific product lookup\.
- 2026-11-07T02:06:13.922642Z: v3: Confirm the selected Shopping market from its settled country label on every browser connection, avoiding inconsistent reads while pages load\.
- 2026-11-07T02:36:09.267487Z: v4: Read Google's country label when its footer is collapsed, and use the verified Shopping entry redirect for product searches\.
- 2026-11-07T04:49:15.975446Z: v5: Complete longer seller lists and exclude accessory bundles, generic JBL listings and explicit regional\-code mismatches\.
- 2026-11-07T06:04:54.582587Z: v6: Reads sale prices beneath Google's popularity badge and recognizes an explicit end to additional matching shops without discarding existing offers\.
- 2026-11-07T09:32:30.893770Z: v7: Reads Best price sale quotes, separates exact black NutriBullet offers, and correctly reports when no exact offers remain\.
- 2026-11-07T11:40:34.136702Z: v8: Exclude replacement vacuum parts and separate ambiguous regional product configurations using verified identifiers\. Expand same\-market discovery and retain explicit coverage gaps\.
- 2026-11-07T15:08:19.590978Z: v9: Keep streaming\-device generations and distinct beauty packaging separate when matching seller offers and reconciling saved observations\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/feedance-google-shopping-competitor-prices-b7971db4006b?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
