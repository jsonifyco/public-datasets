# Louis Vuitton Neverfull Prices by Country

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Published Louis Vuitton Neverfull price records in local currencies\. The published dataset contains 24 rows; its publication timestamp does not establish when prices were observed\.

[Get the full dataset for free](https://www.jsonify.com/datasets/louis-vuitton-neverfull-prices-by-country-6bce6c1fc1cf?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-11-09T09:25:41.805200Z

## The brief

> I need this data: Published Louis Vuitton Neverfull price records in local currencies\. The published dataset contains 24 rows; its publication timestamp does not establish when prices were observed\.

Summary from the public dataset description.

## Louis Vuitton Neverfull prices by country / prices

24 total rows · 10 sampled · Output revision 2
Published: 2026-11-09T09:25:41.805200Z · Producing pipeline version: 1

[CSV sample](outputs/d5355b3abc2b/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/d5355b3abc2b/prices-fe81f9390ffe/sample.json) · [Schema](outputs/d5355b3abc2b/prices-fe81f9390ffe/schema.json)

| currency | fetched\_at\_utc | item | notes | price | source | url | variant\_qty |
| --- | --- | --- | --- | --- | --- | --- | --- |
| GBP | 2026\-11\-09T09:21:59\.281507Z | Neverfull MM Monogram cherry \(M46987\) | UK displayed price includes VAT\. stock\_flag=in\_stock; purchase button: Add to Shopping Bag\. | 1460 | Louis Vuitton United Kingdom | [https://uk\.louisvuitton\.com/eng\-gb/products/neverfull\-mm\-tote\-bag\-monogram\-nvprod5350101v/M46987](<https://uk.louisvuitton.com/eng-gb/products/neverfull-mm-tote-bag-monogram-nvprod5350101v/M46987>) | 1 |
| USD | 2026\-11\-09T09:24:57\.486708Z | Neverfull PM Monogram \(M46979\) | Displayed US price; applicable sales tax may be added at checkout\. stock\_flag=unknown; live purchase button unavailable; online stock not verified\. | 2160 | Louis Vuitton United States | [https://us\.louisvuitton\.com/eng\-us/products/neverfull\-pm\-monogram\-nvprod5350107v/M46979](<https://us.louisvuitton.com/eng-us/products/neverfull-pm-monogram-nvprod5350107v/M46979>) | 1 |
| USD | 2026\-11\-09T09:24:15\.296717Z | Neverfull MM Damier Ebene \(N40599\) | Displayed US price; applicable sales tax may be added at checkout\. stock\_flag=unknown; live purchase button unavailable; online stock not verified\. | 2240 | Louis Vuitton United States | [https://us\.louisvuitton\.com/eng\-us/products/neverfull\-mm\-damier\-ebene\-nvprod5350102v/N40599](<https://us.louisvuitton.com/eng-us/products/neverfull-mm-damier-ebene-nvprod5350102v/N40599>) | 1 |
| EUR | 2026\-11\-09T09:24:44\.763734Z | Neverfull MM Damier Ebene \(N40599\) | Germany displayed price includes VAT \(Mehrwertsteuer\)\. stock\_flag=in\_stock; purchase button: In den Warenkorb\. | 1550 | Louis Vuitton Germany | [https://de\.louisvuitton\.com/deu\-de/produkte/neverfull\-mm\-damier\-ebene\-nvprod5350102v/N40599](<https://de.louisvuitton.com/deu-de/produkte/neverfull-mm-damier-ebene-nvprod5350102v/N40599>) | 1 |
| USD | 2026\-11\-09T09:25:32\.671592Z | Neverfull GM Monogram \(M46978\) | Displayed US price; applicable sales tax may be added at checkout\. stock\_flag=unknown; live purchase button unavailable; online stock not verified\. | 2310 | Louis Vuitton United States | [https://us\.louisvuitton\.com/eng\-us/products/neverfull\-gm\-monogram\-nvprod5350104v/M46978](<https://us.louisvuitton.com/eng-us/products/neverfull-gm-monogram-nvprod5350104v/M46978>) | 1 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| currency | text |
| fetched\_at\_utc | text |
| item | text |
| notes | text |
| price | double precision |
| source | text |
| url | text |
| variant\_qty | integer |

## How the pipeline works

```mermaid
flowchart LR
  n0["offers"]
  n1["prices"]
  n2["validate"]
  n3["prices"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **offers**: Prepare the six specified Neverfull variants across the four official country storefronts\.
- **prices**: Read each exact product page, select its first price after the heading, and mark stock unknown unless its purchase button is visible\.
- **validate**: Check that every selected product\-country pair has one price in its local currency and all requested columns\.
- **prices**: One current official price per specified Neverfull variant and country; variant\_qty counts one specified variant, not inventory units\.

## Version history

- 2026-11-02T10:15:23.160627Z: v1: Adds official prices for the six specified Neverfull variants across four countries, with tax notes and clearly marked unknown stock when purchase buttons are unavailable\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/louis-vuitton-neverfull-prices-by-country-6bce6c1fc1cf?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
