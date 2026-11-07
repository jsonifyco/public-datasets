# Irish Wine and Spirits Price Tracker

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Irish wine and spirits catalogue price observations from O'Briens Wine, Tesco Ireland, Dunnes Stores and SuperValu, including listed prices and promotion details\. The published dataset contains 1,417 rows; its publication timestamp does not establish when the observations were collected\.

[Get the full dataset for free](https://www.jsonify.com/datasets/clinks-irish-wine-and-spirits-price-tracker-ece8b068e56b?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 5
- Last published: 2026-11-07T08:19:05.148849Z

## The brief

> I need this data: Irish wine and spirits catalogue price observations from O'Briens Wine, Tesco Ireland, Dunnes Stores and SuperValu, including listed prices and promotion details\. The published dataset contains 1,417 rows; its publication timestamp does not establish when the observations were collected\.

Summary from the public dataset description.

## Clinks Irish drinks prices / prices

1,417 total rows · 50 sampled · Output revision 5
Published: 2026-11-07T08:19:05.148849Z · Producing pipeline version: 5

[CSV sample](outputs/bb7e3522209b/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/bb7e3522209b/prices-fe81f9390ffe/sample.json) · [Schema](outputs/bb7e3522209b/prices-fe81f9390ffe/schema.json)

| abv | brand | category | collected\_at | in\_stock | price\_eur | product\_name | product\_url |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 16 | Coole Swan | liqueur | 2026\-11\-07T08:13:27\.182337\+00:00 | True | 26 | Coole Swan Superior Irish Cream Liqueur 700ml | [https://www\.dunnesstoresgrocery\.com/sm/delivery/rsid/258/product/coole\-swan\-superior\-irish\-cream\-liqueur\-700ml\-id\-100173115](<https://www.dunnesstoresgrocery.com/sm/delivery/rsid/258/product/coole-swan-superior-irish-cream-liqueur-700ml-id-100173115>) |
| 17\.5 | Baileys | liqueur | 2026\-11\-07T08:12:02\.617319\+00:00 | True | 15\.99 | Baileys Chocolate Cream Liqueur 50cl | [https://www\.obrienswine\.ie/products/baileys\-chocolate\-50cl](<https://www.obrienswine.ie/products/baileys-chocolate-50cl>) |
| None | Conde de Valdemar | wine | 2026\-11\-07T08:13:52\.452923\+00:00 | True | 45 | Conde Valdemar Reserva &amp; Gran Reserva Twin Pack | [https://molloys\.ie/products/conde\-de\-valdemar\-reserva\-gran\-reserva\-twin\-pack](<https://molloys.ie/products/conde-de-valdemar-reserva-gran-reserva-twin-pack>) |
| 15 | Gonzalez Byass | wine fortified | 2026\-11\-07T08:13:27\.161569\+00:00 | True | 16\.5 | Gonzalez Byass Tio Pepe Fino Sherry 750ml | [https://www\.dunnesstoresgrocery\.com/sm/delivery/rsid/258/product/gonzalez\-byass\-tio\-pepe\-fino\-sherry\-750ml\-id\-100512512](<https://www.dunnesstoresgrocery.com/sm/delivery/rsid/258/product/gonzalez-byass-tio-pepe-fino-sherry-750ml-id-100512512>) |
| 12 | Michel Lynch | wine sparkling | 2026\-11\-07T08:13:25\.555854\+00:00 | True | 25 | Michel Lynch Reserve Crémant De Bordeaux Brut 750ml | [https://www\.dunnesstoresgrocery\.com/sm/delivery/rsid/258/product/michel\-lynch\-reserve\-crmant\-de\-bordeaux\-brut\-750ml\-id\-100343170](<https://www.dunnesstoresgrocery.com/sm/delivery/rsid/258/product/michel-lynch-reserve-crmant-de-bordeaux-brut-750ml-id-100343170>) |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| abv | double precision |
| brand | text |
| category | text |
| collected\_at | text |
| in\_stock | boolean |
| price\_eur | double precision |
| product\_name | text |
| product\_url | text |
| promo\_price\_eur | double precision |
| promo\_text | text |
| retailer | text |
| volume\_ml | double precision |

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
