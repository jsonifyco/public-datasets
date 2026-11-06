# Irish Wine and Spirits Price Tracker

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Irish wine and spirits catalogue price observations from O'Briens Wine, Tesco Ireland, Dunnes Stores and SuperValu, including listed prices and promotion details\. The published dataset contains 945 rows; its publication timestamp does not establish when the observations were collected\.

[Get the full dataset for free](https://www.jsonify.com/datasets/clinks-irish-wine-and-spirits-price-tracker-ece8b068e56b?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 5
- Last published: 2026-11-06T21:44:39.961676Z

## The brief

> I need this data: Irish wine and spirits catalogue price observations from O'Briens Wine, Tesco Ireland, Dunnes Stores and SuperValu, including listed prices and promotion details\. The published dataset contains 945 rows; its publication timestamp does not establish when the observations were collected\.

Summary from the public dataset description.

## Clinks Irish drinks prices / prices

944 total rows · 50 sampled · Output revision 4
Published: 2026-11-06T21:44:39.961676Z · Producing pipeline version: Unknown

[CSV sample](outputs/bb7e3522209b/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/bb7e3522209b/prices-fe81f9390ffe/sample.json) · [Schema](outputs/bb7e3522209b/prices-fe81f9390ffe/schema.json)

| retailer | product\_name | brand | category | volume\_ml | abv | price\_eur | promo\_price\_eur |
| --- | --- | --- | --- | --- | --- | --- | --- |
| O'Briens Wine | Monte Real Rioja Reserva | Monte Real | wine red | 750 | 14 | 23\.99 | 14\.99 |
| Dunnes Stores | Monastier Cabernet Sauvignon 75cl | Monastier | wine red | 750 | 13\.5 | 10\.5 | 8 |
| SuperValu | Vina Albali Verdejo Rueda  \(75 cl\) | Viña Albali | wine white | 750 | 13 | 12\.99 | None |
| Molloy's | Valderivero Rueda Verdejo | Valderivero | wine white | 750 | 13 | 12\.99 | 11\.99 |
| Tesco Ireland | Mcguigan Signature Cabernet Sauvignon Red Wine 75Cl | McGuigan | wine red | 750 | 13 | 17 | 8\.5 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| retailer | text |
| product\_name | text |
| brand | text |
| category | text |
| volume\_ml | double precision |
| abv | double precision |
| price\_eur | double precision |
| promo\_price\_eur | double precision |
| promo\_text | text |
| in\_stock | boolean |
| product\_url | text |
| collected\_at | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["plan"]
  n1["listings"]
  n2["deduplicate"]
  n3["details"]
  n4["validate"]
  n5["prices"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
```

- **plan**: Select the first wine and spirit listings from the four required retailers, plus a small optional Tesco check\.
- **listings**: Read each public category and retain its listing order, prices, promotions and product links\.
- **deduplicate**: Keep distinct retailer products and interleave retailers before reading product details\.
- **details**: Fill bottle size, alcohol content and brand from the selected products' own detail pages where needed\.
- **validate**: Check retailer coverage, product identity and euro price fields before saving the daily observation sample\.
- **prices**: Daily Irish retailer product\-price observations, preserving loyalty\-offer terms\.

## Version history

- 2026-11-06T20:24:05.714850Z: v1: Added the Clinks Irish wine and spirits price sample, including Tesco Ireland, with separate regular and loyalty prices and timestamped history\.
- 2026-11-06T20:48:54.840192Z: v2: Recover O’Briens catalogue collection using a verified rendered feed route after raw requests were rate\-limited\.
- 2026-11-06T21:16:22.306045Z: v3: Make the four accessible retailers required, keep Tesco optional and bounded, and correct sale\-pack volume parsing\.
- 2026-11-06T21:19:09.417378Z: v4: Preserve wine bottle sizes while using explicit can volumes ahead of unit\-price comparisons\.
- 2026-11-06T21:44:20.057917Z: v5: Exclude cocktail tools and distinguish alcohol strength from ingredient percentages\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/clinks-irish-wine-and-spirits-price-tracker-ece8b068e56b?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
