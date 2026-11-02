# French Supermarket Prices and Product Catalogue

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

French supermarket product listings and prices from Carrefour, E\.Leclerc, Auchan, Intermarché, Super U, Monoprix and other retailers\. The published dataset contains 171,865 rows across product and category tables; observation dates are recorded where available\.

[Get the full dataset for free](https://www.jsonify.com/datasets/supermarket-products-in-france-6bb96540e5f9?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 46
- Last published: 2026-11-02T14:53:40.285101Z

## The brief

> I need this data: French supermarket product listings and prices from Carrefour, E\.Leclerc, Auchan, Intermarché, Super U, Monoprix and other retailers\. The published dataset contains 171,865 rows across product and category tables; observation dates are recorded where available\.

Summary from the public dataset description.

## Supermarket Products in France / products

169,176 total rows · 50 sampled · Output revision 5
Published: 2026-11-02T14:53:40.285101Z · Producing pipeline version: 46

[CSV sample](outputs/5bba15b41143/products-0a3e27b8ca81/sample.csv) · [JSON sample](outputs/5bba15b41143/products-0a3e27b8ca81/sample.json) · [Schema](outputs/5bba15b41143/products-0a3e27b8ca81/schema.json)

| availability | brand | category | category\_url | currency | image\_url | location\_scope | observed\_at |
| --- | --- | --- | --- | --- | --- | --- | --- |
| True | Nature Valley | Epicerie Sucrée | [https://courses\.monoprix\.fr/categories/epicerie\-sucr%C3%A9e/bd800ae5\-5dde\-488d\-b187\-0d9578581d61](<https://courses.monoprix.fr/categories/epicerie-sucr%C3%A9e/bd800ae5-5dde-488d-b187-0d9578581d61>) | EUR | [https://courses\.monoprix\.fr/images\-v3/0c44253f\-c4a3\-4340\-9d37\-d41e42b9d14a/6b8d11b1\-73f4\-49ab\-b855\-7d014eaf400a/300x300\.jpg](<https://courses.monoprix.fr/images-v3/0c44253f-c4a3-4340-9d37-d41e42b9d14a/6b8d11b1-73f4-49ab-b855-7d014eaf400a/300x300.jpg>) | national\_online | 2026\-11\-01T22:12:02\.515476\+00:00 |
| True | Persil | Entretien | [https://www\.houra\.fr/catalogue/entretien/voir\-tous\-les\-produits\-B1559594\-1\.html](<https://www.houra.fr/catalogue/entretien/voir-tous-les-produits-B1559594-1.html>) | EUR | None | paris\_delivery\_area | 2026\-11\-02T01:10:27\.638518\+00:00 |
| True | Roger &amp; Gallet | Parapharmacie | [https://courses\.monoprix\.fr/categories/parapharmacie/396ea71e\-a37c\-4890\-aa3f\-63734378dc6a](<https://courses.monoprix.fr/categories/parapharmacie/396ea71e-a37c-4890-aa3f-63734378dc6a>) | EUR | [https://courses\.monoprix\.fr/images\-v3/0c44253f\-c4a3\-4340\-9d37\-d41e42b9d14a/0e401fb0\-05ea\-411e\-adfa\-a102011516a3/300x300\.jpg](<https://courses.monoprix.fr/images-v3/0c44253f-c4a3-4340-9d37-d41e42b9d14a/0e401fb0-05ea-411e-adfa-a102011516a3/300x300.jpg>) | national\_online | 2026\-11\-01T22:16:50\.563266\+00:00 |
| True | VIEILLE FERME | Bière, Cave et Spiritueux | [https://courses\.monoprix\.fr/categories/bi%C3%A8re\-cave\-et\-spiritueux/1c32cbad\-6e7e\-437a\-91b4\-923d2c9fd6af](<https://courses.monoprix.fr/categories/bi%C3%A8re-cave-et-spiritueux/1c32cbad-6e7e-437a-91b4-923d2c9fd6af>) | EUR | [https://courses\.monoprix\.fr/images\-v3/0c44253f\-c4a3\-4340\-9d37\-d41e42b9d14a/7a69238b\-090b\-4d5f\-bf1a\-80ec62e52fda/300x300\.jpg](<https://courses.monoprix.fr/images-v3/0c44253f-c4a3-4340-9d37-d41e42b9d14a/7a69238b-090b-4d5f-bf1a-80ec62e52fda/300x300.jpg>) | national\_online | 2026\-11\-01T22:14:55\.869161\+00:00 |
| True | Le petit Olivier | Hygiène, Beauté | [https://www\.houra\.fr/catalogue/hygiene\-beaute/voir\-tous\-les\-produits\-B1559598\-1\.html](<https://www.houra.fr/catalogue/hygiene-beaute/voir-tous-les-produits-B1559598-1.html>) | EUR | None | paris\_delivery\_area | 2026\-11\-02T01:02:07\.158073\+00:00 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| availability | boolean |
| brand | text |
| category | text |
| category\_url | text |
| currency | text |
| image\_url | text |
| location\_scope | text |
| observed\_at | text |
| offer\_id | text |
| pack\_size | text |
| price | double precision |
| price\_per\_unit | double precision |
| product\_id | text |
| product\_name | text |
| product\_url | text |
| promotion | text |
| retailer | text |
| seller\_id | text |
| seller\_name | text |
| source\_brand | text |
| source\_name | text |
| store\_address | text |
| store\_id | text |
| store\_name | text |
| unit\_price\_label | text |

## Supermarket Products in France / categories

2,689 total rows · 50 sampled · Output revision 5
Published: 2026-11-02T14:53:40.285101Z · Producing pipeline version: 46

[CSV sample](outputs/5bba15b41143/categories-a6216ea03e57/sample.csv) · [JSON sample](outputs/5bba15b41143/categories-a6216ea03e57/sample.json) · [Schema](outputs/5bba15b41143/categories-a6216ea03e57/schema.json)

| category | category\_url | complete | completed\_at | notes | pages | products | reported\_total |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Pizzas | [https://www\.carrefour\.fr/r/charcuterie\-traiteur/pizzas\-tartes\-pates\-fraiches/pizzas](<https://www.carrefour.fr/r/charcuterie-traiteur/pizzas-tartes-pates-fraiches/pizzas>) | True | 2026\-11\-01T15:07:27\.123912\+00:00 | final\-page metadata currentPage==totalPage \(2\) with null next link after 48 exact Carrefour API entities The supplied Carrefour category URL redirected to the current first\-party product leaf [https://www\.carrefour\.fr/r/charcuterie\-traiteur/pizzas\-tartes\-pates\-fraiches/pizzas](<https://www.carrefour.fr/r/charcuterie-traiteur/pizzas-tartes-pates-fraiches/pizzas>)\. The exact Paris Auteuil cart remained stable before and after sequential first\-party JSON catalogue pagination; sponsored DOM placements were not counted as additional products\. | 2 | 48 | 48 |
| Brosses et Peignes | [https://www\.carrefour\.fr/r/hygiene\-et\-beaute/les\-cheveux/accessoires\-cheveux/brosse\-peigne](<https://www.carrefour.fr/r/hygiene-et-beaute/les-cheveux/accessoires-cheveux/brosse-peigne>) | True | 2026\-11\-01T18:28:56\.578818\+00:00 | final\-page metadata currentPage==totalPage \(1\) with null next link after 13 exact Carrefour API entities The supplied Carrefour category URL redirected to the current first\-party product leaf [https://www\.carrefour\.fr/r/hygiene\-et\-beaute/les\-cheveux/accessoires\-cheveux/brosse\-peigne](<https://www.carrefour.fr/r/hygiene-et-beaute/les-cheveux/accessoires-cheveux/brosse-peigne>)\. The exact Paris Auteuil cart remained stable before and after sequential first\-party JSON catalogue pagination; sponsored DOM placements were not counted as additional products\. | 1 | 13 | 13 |
| Gels lavants et Eaux nettoyantes | [https://www\.carrefour\.fr/r/parapharmacie/bebe/toilette\-bebe/gels\-lavants\-et\-eaux\-nettoyantes](<https://www.carrefour.fr/r/parapharmacie/bebe/toilette-bebe/gels-lavants-et-eaux-nettoyantes>) | True | 2026\-11\-01T18:44:45\.272589\+00:00 | final\-page metadata currentPage==totalPage \(1\) with null next link after 30 exact Carrefour API entities The supplied Carrefour category URL redirected to the current first\-party product leaf [https://www\.carrefour\.fr/r/parapharmacie/bebe/toilette\-bebe/gels\-lavants\-et\-eaux\-nettoyantes](<https://www.carrefour.fr/r/parapharmacie/bebe/toilette-bebe/gels-lavants-et-eaux-nettoyantes>)\. The exact Paris Auteuil cart remained stable before and after sequential first\-party JSON catalogue pagination; sponsored DOM placements were not counted as additional products\. | 1 | 30 | 30 |
| Calendrier de l'avent | [https://www\.carrefour\.fr/r/epicerie\-sucree/chocolats/calendrier\-lavent](<https://www.carrefour.fr/r/epicerie-sucree/chocolats/calendrier-lavent>) | True | 2026\-11\-01T16:27:42\.560137\+00:00 | final\-page metadata currentPage==totalPage \(2\) with null next link after 32 exact Carrefour API entities The supplied Carrefour category URL redirected to the current first\-party product leaf [https://www\.carrefour\.fr/r/epicerie\-sucree/chocolats/calendrier\-lavent](<https://www.carrefour.fr/r/epicerie-sucree/chocolats/calendrier-lavent>)\. The exact Paris Auteuil cart remained stable before and after sequential first\-party JSON catalogue pagination; sponsored DOM placements were not counted as additional products\. | 2 | 32 | 32 |
| Fruits, pâtes de fruits | [https://www\.coursesu\.com/c/chocolats\-de\-noel/chocolats\-et\-specialites\-a\-offrir/fruits\-pates\-de\-fruits](<https://www.coursesu.com/c/chocolats-de-noel/chocolats-et-specialites-a-offrir/fruits-pates-de-fruits>) | True | 2026\-11\-02T12:19:03\.730416\+00:00 |  | 1 | 1 | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| category | text |
| category\_url | text |
| complete | boolean |
| completed\_at | text |
| notes | text |
| pages | integer |
| products | integer |
| reported\_total | integer |
| source\_name | text |
| started\_at | text |
| store\_name | text |
| terminal | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["categories#95;input"]
  n1["collected#95;categories#95;input"]
  n2["departments#95;input"]
  n3["sources"]
  n4["load#95;sources"]
  n5["discover#95;departments"]
  n6["root#95;categories"]
  n7["expand#95;departments"]
  n8["plan#95;categories"]
  n9["collect#95;categories"]
  n10["refresh#95;legacy#95;categories"]
  n11["label#95;marketplace#95;offers"]
  n12["prepare#95;output"]
  n13["output#95;kind"]
  n14["shape#95;products"]
  n15["products"]
  n16["shape#95;categories"]
  n17["categories"]
  n4 --> n5
  n5 --> n6
  n6 --> n7
  n7 --> n8
  n8 --> n9
  n9 --> n10
  n10 --> n11
  n11 --> n12
  n12 --> n13
  n14 --> n15
  n16 --> n17
  n0 --> n4
  n1 --> n4
  n2 --> n4
  n3 --> n4
  n13 --> n16
  n13 --> n14
  n3 --> n4
  n2 --> n6
  n0 --> n8
  n1 --> n10
```

- **categories\_input**: Optional saved category inventory for a targeted or resumed catalogue refresh\. Leave empty to discover every configured retailer category\.
- **collected\_categories\_input**: Optional saved collected categories for reprocessing offers without recollecting retailer catalogues\.
- **departments\_input**: Optional saved department inventory for resuming category discovery\.
- **sources**: French retailer storefronts and selected Paris contexts\.
- **load\_sources**: Load the selected French retailer storefronts and Paris store contexts\.
- **discover\_departments**: Read the current grocery and everyday household departments from each French retailer\.
- **root\_categories**: Split retailer navigation into independent category discovery tasks\.
- **expand\_departments**: Resolve department landing pages to their live product\-list categories\.
- **plan\_categories**: Create a reusable inventory of all discovered retailer product categories\.
- **collect\_categories**: Traverse complete category catalogues and retain source\-backed product offers with their store context\.
- **refresh\_legacy\_categories**: Recheck older category observations when their parser evidence requires refresh, saving each completed category independently\.
- **label\_marketplace\_offers**: Resolve explicit Auchan marketplace listings into source\-confirmed seller offers, without Paris store attribution\.
- **prepare\_output**: Deduplicate offers within each retailer context and retain category completion evidence\.
- **output\_kind**: Separate current product offers from category coverage evidence\.
- **shape\_products**: Publish the current retailer product catalogue with prices, links and Paris context\.
- **products**: sink
- **shape\_categories**: Publish category traversal counts and source completion evidence\.
- **categories**: sink

## Version history

- 2026-11-01T13:14:37.191882Z: v1: Adds nine French supermarket catalogues with Paris store context\. Intermarché products are retained with explicit category coverage warnings when source totals cannot be reconciled\.
- 2026-11-01T13:41:31.510877Z: v2: Fixes Carrefour category links shared across departments so catalogue discovery can continue\.
- 2026-11-01T13:49:51.410991Z: v3: Fixes Carrefour categories that appear twice in its menu by matching the category identity on the page\. Collection can retain those categories and continue from saved progress\.
- 2026-11-01T14:16:46.066570Z: v4: Fixed Carrefour food listings that use a product identifier instead of a barcode\. Categories whose counts change during collection are retried before accepting their results\.
- 2026-11-01T14:31:08.312292Z: v5: Fixed Carrefour store selection when a hidden Drive button appears on the page\. Temporary store\-selection timeouts now use the existing retry process\.
- 2026-11-01T15:02:01.320561Z: v6: Added recovery when a Carrefour browsing session loses its response, restarting the affected category with the correct Paris store selected\.
- 2026-11-01T15:20:34.693957Z: v7: Fixed missing Carrefour products caused by repeated listings between pages\. A verified price\-order fallback now recovers the complete category\.
- 2026-11-01T15:42:06.360451Z: v8: Corrected Carrefour’s baby\-category scope to exclude toys, furniture, clothing and travel equipment while retaining everyday baby\-care products\.
- 2026-11-01T15:58:49.461544Z: v9: Completed the supermarket\-only filter for baby feeding furniture and kitchen appliances, while retaining baby food and everyday feeding accessories\.
- 2026-11-01T16:07:33.983796Z: v10: Separate Carrefour delivery\-only household offers from Paris store offers, preserving products without attributing national prices to a local store\.
- 2026-11-01T17:58:39.055021Z: v11: Recover transient Carrefour catalogue request rejections through the existing bounded fresh\-store retry\.
- 2026-11-01T19:26:32.134147Z: v12: Carrefour categories now retain every returned product when the displayed total is too low, with the discrepancy recorded in coverage notes\. Missing products and conflicting listings still stop the update\.
- 2026-11-01T20:07:27.884878Z: v13: E\.Leclerc department counts now account for products listed in multiple subcategories\. When counts differ, every subcategory is checked before the collection can continue\.
- 2026-11-01T20:13:26.625337Z: v14: E\.Leclerc subcategory collection now keeps the verified Convention store selection instead of repeating it for each page\. Temporary navigation failures get a bounded fresh\-session recovery attempt\.
- 2026-11-01T21:06:13.794864Z: v15: E\.Leclerc offer changes are now checked with one fresh category reading\. Collection continues only when the current prices and product identities agree\.
- 2026-11-01T21:46:05.329026Z: v16: Recovers Intermarché catalogue access after temporary failures and handles its updated cookie\-consent control\.
- 2026-11-01T21:52:10.081113Z: v17: Recovers temporary Intermarché page failures without immediately restarting the whole category, and spaces out page requests\.
- 2026-11-01T22:09:27.554268Z: v18: Fixes Monoprix and Courses U request sessions and handles identical sponsored Monoprix products without counting them twice\.
- 2026-11-01T22:14:09.966838Z: v19: Restarts Monoprix pagination safely when switching to a fresh browser visit\.
- 2026-11-01T22:20:45.606323Z: v20: Retries Auchan collection with a fresh verified Tolbiac visit when the selected\-store confirmation is missing\.
- 2026-11-01T22:34:44.294379Z: v21: Fixes Auchan shelf prices where conditional multi\-buy savings appear before the actual price, and refreshes affected older results\.
- 2026-11-01T22:42:56.509813Z: v22: Uses Auchan’s labelled pickup price instead of signed promotional savings, and safely restarts categories whose totals change during collection\.
- 2026-11-01T22:48:35.526601Z: v23: Auchan can now recover when its store\-selection form stalls, while still checking the exact Paris pickup store before saving prices\.
- 2026-11-01T23:05:54.816940Z: v24: Auchan categories with inconsistent displayed totals are now verified through two complete matching reads, with the discrepancy recorded alongside the products\.
- 2026-11-01T23:11:32.853614Z: v25: Auchan offer verification now ignores changing review\-count badges while continuing to check product details and prices\.
- 2026-11-01T23:40:18.729405Z: v26: Auchan collection now follows category pages that open subcategories and correctly recognizes explicitly empty store categories\.
- 2026-11-01T23:54:12.954952Z: v27: Auchan’s off\-season wine\-fair page is recorded as closed while the regular wine range continues to be collected\.
- 2026-11-02T00:00:00.684250Z: v28: Courses U categories explicitly unavailable at the selected store now produce clear coverage notes instead of stopping the collection\.
- 2026-11-02T00:10:36.905196Z: v29: Courses U image\-only campaign advertisements no longer become nameless products\. Actual product cards remain eligible, with names recovered from matching structured card data where needed\.
- 2026-11-02T00:24:55.560106Z: v30: Courses U editorial links no longer become duplicate product offers\. Previously collected categories with suspect URL identities are rechecked before publication\.
- 2026-11-02T00:38:42.468149Z: v31: Courses U recommendation carousels no longer duplicate the same products collected from category pages\.
- 2026-11-02T00:52:33.676814Z: v32: Houra categories whose totals change mid\-collection now get one fresh complete pass, which must still reconcile fully\.
- 2026-11-02T01:08:54.305579Z: v33: Houra can recover once from an identical offer repeating during pagination, without relaxing product or coverage checks\.
- 2026-11-02T01:17:29.269472Z: v34: Mon Marché recipe content is recognized separately from supermarket products and recorded in category coverage\.
- 2026-11-02T01:40:16.376775Z: v35: H2O now follows its visible links to more products, collecting the full category instead of stopping after the first page\.
- 2026-11-02T01:57:52.427429Z: v36: Final category rechecks now save progress individually\. Temporary Courses U store\-opening refusals receive two bounded retries before failing\.
- 2026-11-02T02:12:48.235626Z: v37: Courses U per\-piece unit prices no longer obscure shelf prices\. Older affected categories are rechecked before the next publication\.
- 2026-11-02T02:40:46.247437Z: v38: Removes specialist animal structures outside the requested supermarket ranges and fills source\-backed Auchan unit prices and Mon Marché pack sizes and unit prices\.
- 2026-11-02T03:17:16.433568Z: v39: Rechecks Auchan category shortfalls and only marks categories complete when collected products reconcile with their displayed totals\.
- 2026-11-02T08:56:03.517434Z: v40: Fully traversed Auchan categories now save all returned products with an explicit incomplete\-coverage warning when displayed totals differ\. Retained category results receive the same warning before publication\.
- 2026-11-02T10:20:15.141033Z: v41: Restores Courses U unit prices and explicit pack descriptions for Courses U and Auchan products\.
- 2026-11-02T12:06:29.431695Z: v42: Auchan categories with changing product lists now retain observed offers and clearly report incomplete coverage\. Timed\-out store searches are retried before stopping an update\.
- 2026-11-02T12:26:50.553693Z: v43: Courses U now distinguishes current single\-item prices from former prices and multi\-buy offers, keeping promotional products in the catalogue with the correct shelf and unit prices\.
- 2026-11-02T13:23:47.887899Z: v44: Mon Marché refreshes now record explicitly removed categories without stopping the catalogue update, while continuing to collect current categories for the selected Paris delivery address\.
- 2026-11-02T14:44:19.956852Z: v45: Auchan marketplace listings now produce separate seller\-labelled offers with their own prices, without Paris\-store attribution\.
- 2026-11-02T14:50:19.287869Z: v46: Auchan products sold by Auchan itself now retain their collected store offers, while third\-party sellers remain separate marketplace offers\.

## Recorded repairs

- 2026-11-02T03:32:29.338093Z: no change
- 2026-11-02T03:39:06.490363Z: temporary blocker

[Get the full dataset for free](https://www.jsonify.com/datasets/supermarket-products-in-france-6bb96540e5f9?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
