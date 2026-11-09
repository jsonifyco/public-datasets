# DC Grocery Dairy and Egg Prices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Dairy and egg listings from Streets Market on Uber Eats, Safeway in Georgetown, and Giant in Bethesda on DoorDash\. The published dataset contains 457 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/dc-grocery-dairy-and-egg-prices-feb64fb083cc?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 3
- Last published: 2026-11-02T14:33:32.069897Z

## The brief

> I need this data: Dairy and egg listings from Streets Market on Uber Eats, Safeway in Georgetown, and Giant in Bethesda on DoorDash\. The published dataset contains 457 rows\.

Summary from the public dataset description.

## DC grocery dairy and egg prices / prices

457 total rows · 50 sampled · Output revision 2
Published: 2026-11-02T14:33:32.069897Z · Producing pipeline version: 3

[CSV sample](outputs/53d1f26bd177/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/53d1f26bd177/prices-fe81f9390ffe/sample.json) · [Schema](outputs/53d1f26bd177/prices-fe81f9390ffe/schema.json)

| currency | fetched\_at\_utc | item | notes | price | source | url | variant\_qty |
| --- | --- | --- | --- | --- | --- | --- | --- |
| USD | 2026\-11\-02T14:04:18\.179828\+00:00 | Daisy Brand Light Sour Cream \(14 oz\) | $3\.99; Many in stock; stock\_level: STOCK\_LEVEL\_UNSPECIFIED; public storefront price; delivery fees excluded; duplicate listing: no | 3\.99 | Giant Food \(10400 Old Georgetown Rd, Bethesda MD\) via DoorDash | [https://www\.doordash\.com/convenience/store/27550987/](<https://www.doordash.com/convenience/store/27550987/>) | 14 oz |
| USD | 2026\-11\-02T14:00:20\.431013\+00:00 | Good Culture Cottage Cheese, Whole Milk Classic \(16 oz\) | section: Landing / Fresh Food; isSoldOut: false; isAvailable: true; public storefront price; delivery fees excluded; duplicate listing: no | 3\.99 | Streets Market \(2400 14th St NW, Washington DC\) via Uber Eats | [https://www\.ubereats\.com/store/streets\-market\-2400\-14th\-st\-washington/d6u8kREgUMK1zRJldNBd1w](<https://www.ubereats.com/store/streets-market-2400-14th-st-washington/d6u8kREgUMK1zRJldNBd1w>) | 16 oz |
| USD | 2026\-11\-02T14:33:21\.919662\+00:00 | Daisy Pure &amp; Natural Squeeze Sour Cream \(14 oz\) | $3\.99 on sale from $4\.39; Many in stock; stock\_level: STOCK\_LEVEL\_UNSPECIFIED; public storefront price; delivery fees excluded; duplicate listing: no | 3\.99 | Safeway \(1855 Wisconsin Ave NW, Washington DC\) via DoorDash | [https://www\.doordash\.com/convenience/store/1749048/](<https://www.doordash.com/convenience/store/1749048/>) | 14 oz |
| USD | 2026\-11\-02T14:01:05\.450417\+00:00 | Alderfer Eggs Organic Grade a Medium Brown Eggs \(18 ct\) | section: Fresh Food / Dairy, Cheese &amp; Eggs; isSoldOut: false; isAvailable: true; titleBadge: \{"text": "Alderfer Eggs Organic Grade a Medium Brown Eggs \(18 ct\)", "textFormat": "&lt;span&gt;Alderfer Eggs Organic Grade a Medium Brown Eggs \(18 ct\)&lt;/span&gt;", "accessibilityText": "Alderfer Eggs Organic Grade a Medium Brown Eggs \(18 ct\)"}; public storefront price; delivery fees excluded; duplicate listing: no | 5\.99 | Streets Market \(2400 14th St NW, Washington DC\) via Uber Eats | [https://www\.ubereats\.com/store/streets\-market\-2400\-14th\-st\-washington/d6u8kREgUMK1zRJldNBd1w](<https://www.ubereats.com/store/streets-market-2400-14th-st-washington/d6u8kREgUMK1zRJldNBd1w>) | 18 ct |
| USD | 2026\-11\-02T14:04:14\.868816\+00:00 | Chobani Flip Low\-Fat Boston Cream Pie Greek Yogurt \(4\.5 oz\) | $2\.39; stock\_level: STOCK\_LEVEL\_UNSPECIFIED; public storefront price; delivery fees excluded; duplicate listing: no | 2\.39 | Giant Food \(10400 Old Georgetown Rd, Bethesda MD\) via DoorDash | [https://www\.doordash\.com/convenience/store/27550987/](<https://www.doordash.com/convenience/store/27550987/>) | 4\.5 oz |

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
| variant\_qty | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["stores"]
  n1["prices"]
  n2["coverage"]
  n3["prices"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **stores**: Select the three requested Streets Market, Safeway, and Giant storefronts\.
- **prices**: Read each exact storefront and all pages of the relevant dairy listings, retaining separate source offers and their prices\.
- **coverage**: Require usable dairy and egg prices from all three requested stores before replacing the public dataset\.
- **prices**: Current source listing prices for dairy and eggs at the three requested grocery stores\.

## Version history

- 2026-11-02T10:13:45.104672Z: v1: Collect dairy and egg listings from the three requested stores, preserving separate offers, package sizes, promotions and stock notes\.
- 2026-11-02T11:03:28.143719Z: v2: Restores DoorDash collection by waiting for loaded dairy listings and reading prices within the storefront page\. Preserves all three stores and separately priced duplicate listings\.
- 2026-11-02T14:28:34.815386Z: v3: Wait for DoorDash’s live catalog to initialize and use the public storefront request headers before collecting prices\.

## Recorded repairs

- 2026-11-02T14:04:48.719957Z: no change
- 2026-11-02T14:05:06.973400Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/dc-grocery-dairy-and-egg-prices-feb64fb083cc?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
