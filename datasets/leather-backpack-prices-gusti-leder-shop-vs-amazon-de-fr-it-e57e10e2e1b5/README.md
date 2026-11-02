# Leather Backpack Prices: Gusti Leder and Amazon

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

A published dataset of leather backpack listings from Gusti Leder Germany and Amazon Germany, France and Italy\. Prices are displayed in euros; shipping and conditional coupons are excluded\.

[Get the full dataset for free](https://www.jsonify.com/datasets/leather-backpack-prices-gusti-leder-shop-vs-amazon-de-fr-it-e57e10e2e1b5?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 1
- Last published: 2026-11-02T10:35:13.486479Z

## The brief

> I need this data: A published dataset of leather backpack listings from Gusti Leder Germany and Amazon Germany, France and Italy\. Prices are displayed in euros; shipping and conditional coupons are excluded\.

Summary from the public dataset description.

## Leather backpack prices: Gusti Leder shop vs Amazon DE/FR/IT / backpacks

52 total rows · 10 sampled · Output revision 1
Published: 2026-11-02T10:35:13.486479Z · Producing pipeline version: 1

[CSV sample](outputs/2a8b5246fae2/backpacks-3ad734d4decb/sample.csv) · [JSON sample](outputs/2a8b5246fae2/backpacks-3ad734d4decb/sample.json) · [Schema](outputs/2a8b5246fae2/backpacks-3ad734d4decb/schema.json)

| source | url | item | variant\_qty | price | currency | fetched\_at\_utc | notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| amazon\.fr | [https://www\.amazon\.fr/dp/B074DZPJQ2](<https://www.amazon.fr/dp/B074DZPJQ2>) | Gusti Sac à dos en cuir \- Sac à dos Sac de jour Sac d'extérieur Cuir véritable Homme/Femme | 2 | 124\.95 | EUR | 2026\-11\-02T10:31:28\.223980\+00:00 | \{"ASIN": "B074DZPJQ2", "strike\_through\_RRP": null, "outlet": null, "stock": "in\_stock", "variant\_qty\_basis": "Distinct reported selectable ASINs including current listing; minimum observed count when no siblings reported", "outlet\_basis": "Not provided by Amazon; null is unknown", "price\_basis": "Regional product displayed offer; shipping and conditional coupons excluded", "brand": "Gusti"} |
| gusti\-leder\.de | [https://gusti\-leder\.de/products/outlet\-rucksack\-10](<https://gusti-leder.de/products/outlet-rucksack-10>) | Gusti Leder Outlet Rucksack \(SO7\_M120\-1\-1\_17441\) | 1 | 64\.95 | EUR | 2026\-11\-02T10:27:52\.605668\+00:00 | \{"ASIN": null, "strike\_through\_RRP": 94\.95, "outlet": true, "stock": "in\_stock", "variant\_qty\_basis": "Shopify selectable variants on this listing", "price\_basis": "German storefront displayed price; shipping excluded"} |
| amazon\.de | [https://www\.amazon\.de/dp/B0DSJFZHYL](<https://www.amazon.de/dp/B0DSJFZHYL>) | Gusti Leder Milo New Rolltop Rucksack aus Leder für Damen und Herren, 15\-Zoll\-Laptopfach, 13 L, mit verstecktem AirTag\-Fach, Flaschenhalter, 3 Reißverschlussfächern und abnehmbarer Tasche, Braun | 1 | 114\.95 | EUR | 2026\-11\-02T10:28:08\.305497\+00:00 | \{"ASIN": "B0DSJFZHYL", "strike\_through\_RRP": null, "outlet": null, "stock": "in\_stock", "variant\_qty\_basis": "Distinct reported selectable ASINs including current listing; minimum observed count when no siblings reported", "outlet\_basis": "Not provided by Amazon; null is unknown", "price\_basis": "Regional product displayed offer; shipping and conditional coupons excluded", "brand": "Gusti"} |
| amazon\.de | [https://www\.amazon\.de/dp/B0728HSB8K](<https://www.amazon.de/dp/B0728HSB8K>) | Berliner Bags Rolltop Rucksack Utrecht Vintage, Lederrucksack \- Braun | 6 | 159\.99 | EUR | 2026\-11\-02T10:30:36\.991664\+00:00 | \{"ASIN": "B0728HSB8K", "strike\_through\_RRP": null, "outlet": null, "stock": "in\_stock", "variant\_qty\_basis": "Distinct reported selectable ASINs including current listing; minimum observed count when no siblings reported", "outlet\_basis": "Not provided by Amazon; null is unknown", "price\_basis": "Regional product displayed offer; shipping and conditional coupons excluded", "brand": "BerlinerBags"} |
| amazon\.fr | [https://www\.amazon\.fr/dp/B0CS37733F](<https://www.amazon.fr/dp/B0CS37733F>) | Gusti Leder Sac à dos « Gitta » Rolltop \- Sac à dos en cuir de chèvre marron \- Vintage \- Avec fermeture éclair et fermeture magnétique \- 8\-10 l \- Pour le quotidien et l'université | 1 | 89\.95 | EUR | 2026\-11\-02T10:32:23\.176574\+00:00 | \{"ASIN": "B0CS37733F", "strike\_through\_RRP": null, "outlet": null, "stock": "in\_stock", "variant\_qty\_basis": "Distinct reported selectable ASINs including current listing; minimum observed count when no siblings reported", "outlet\_basis": "Not provided by Amazon; null is unknown", "price\_basis": "Regional product displayed offer; shipping and conditional coupons excluded", "brand": "Gusti"} |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| source | text |
| url | text |
| item | text |
| variant\_qty | integer |
| price | double precision |
| currency | text |
| fetched\_at\_utc | text |
| notes | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["sources"]
  n1["search"]
  n2["candidates"]
  n3["details"]
  n4["snapshot"]
  n5["backpacks"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
```

- **sources**: Set up the four requested leather backpack searches in Germany, France and Italy\.
- **search**: Read Gusti Germany search cards and Amazon market results, retaining the requested brands and original search membership\.
- **candidates**: Deduplicate search listings and balance the candidate pool across all four sources before checking each product\.
- **details**: Verify backpack material and category on each product, then read its regional price, selectable variant count and availability\.
- **snapshot**: Keep a balanced snapshot of 40\-60 distinct verified leather backpack listings, requiring all four markets and German competitor coverage\.
- **backpacks**: Current verified leather backpack prices from Gusti Germany and Amazon Germany, France and Italy\.

## Version history

- 2026-11-02T10:26:23.865795Z: v1: Created the weekly leather backpack price comparison across Gusti Germany and Amazon DE, FR and IT, including named German competitors and material exclusions\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/leather-backpack-prices-gusti-leder-shop-vs-amazon-de-fr-it-e57e10e2e1b5?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
