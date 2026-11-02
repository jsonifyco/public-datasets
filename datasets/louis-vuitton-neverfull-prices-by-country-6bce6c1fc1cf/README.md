# Louis Vuitton Neverfull Prices by Country

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Published Louis Vuitton Neverfull price records in local currencies\. The current published table contains 24 rows; its publication timestamp does not establish when prices were observed\.

[Get the full dataset for free](https://www.jsonify.com/datasets/louis-vuitton-neverfull-prices-by-country-6bce6c1fc1cf?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 1
- Last published: 2026-11-02T10:26:23.565459Z

## The brief

> I need this data: Published Louis Vuitton Neverfull price records in local currencies\. The current published table contains 24 rows; its publication timestamp does not establish when prices were observed\.

Summary from the public dataset description.

## Louis Vuitton Neverfull prices by country / prices

24 total rows · 10 sampled · Output revision 1
Published: 2026-11-02T10:26:23.565459Z · Producing pipeline version: 1

[CSV sample](outputs/d5355b3abc2b/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/d5355b3abc2b/prices-fe81f9390ffe/sample.json) · [Schema](outputs/d5355b3abc2b/prices-fe81f9390ffe/schema.json)

| currency | fetched\_at\_utc | item | notes | price | source | url | variant\_qty |
| --- | --- | --- | --- | --- | --- | --- | --- |
| GBP | 2026\-11\-02T10:26:16\.106966Z | Neverfull GM Monogram \(M46978\) | UK displayed price includes VAT\. stock\_flag=in\_stock; purchase button: Add to Shopping Bag\. | 1500 | Louis Vuitton United Kingdom | [https://uk\.louisvuitton\.com/eng\-gb/products/neverfull\-gm\-tote\-bag\-monogram\-nvprod5350104v/M46978](<https://uk.louisvuitton.com/eng-gb/products/neverfull-gm-tote-bag-monogram-nvprod5350104v/M46978>) | 1 |
| EUR | 2026\-11\-02T10:25:46\.905768Z | Neverfull MM Damier Ebene \(N40599\) | France displayed price includes VAT \(TTC\)\. stock\_flag=in\_stock; purchase button: Ajouter au panier\. | 1550 | Louis Vuitton France | [https://fr\.louisvuitton\.com/fra\-fr/produits/sac\-neverfull\-mm\-damier\-ebene\-nvprod5350102v/N40599](<https://fr.louisvuitton.com/fra-fr/produits/sac-neverfull-mm-damier-ebene-nvprod5350102v/N40599>) | 1 |
| EUR | 2026\-11\-02T10:26:06\.257035Z | Neverfull MM Damier Azur \(N40604\) | Germany displayed price includes VAT \(Mehrwertsteuer\)\. stock\_flag=in\_stock; purchase button: In den Warenkorb\. | 1550 | Louis Vuitton Germany | [https://de\.louisvuitton\.com/deu\-de/produkte/neverfull\-mm\-damier\-azur\-canvas\-nvprod5350103v/N40604](<https://de.louisvuitton.com/deu-de/produkte/neverfull-mm-damier-azur-canvas-nvprod5350103v/N40604>) | 1 |
| EUR | 2026\-11\-02T10:25:35\.584392Z | Neverfull MM Monogram cherry \(M46987\) | France displayed price includes VAT \(TTC\)\. stock\_flag=in\_stock; purchase button: Ajouter au panier\. | 1550 | Louis Vuitton France | [https://fr\.louisvuitton\.com/fra\-fr/produits/sac\-neverfull\-mm\-monogram\-nvprod5350101v/M46987](<https://fr.louisvuitton.com/fra-fr/produits/sac-neverfull-mm-monogram-nvprod5350101v/M46987>) | 1 |
| EUR | 2026\-11\-02T10:25:46\.469081Z | Neverfull MM Damier Ebene \(N40599\) | Germany displayed price includes VAT \(Mehrwertsteuer\)\. stock\_flag=in\_stock; purchase button: In den Warenkorb\. | 1550 | Louis Vuitton Germany | [https://de\.louisvuitton\.com/deu\-de/produkte/neverfull\-mm\-damier\-ebene\-nvprod5350102v/N40599](<https://de.louisvuitton.com/deu-de/produkte/neverfull-mm-damier-ebene-nvprod5350102v/N40599>) | 1 |

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
