# Allegro Poland LEGO Seller Prices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Allegro Poland LEGO seller offers: 681 offer rows in the published table\. The table includes set details, seller names, condition, and prices in PLN\.

[Get the full dataset for free](https://www.jsonify.com/datasets/allegro-poland-lego-seller-prices-111dc8b854b2?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 2
- Last published: 2026-11-12T11:38:22.240043Z

## The brief

> I need this data: Allegro Poland LEGO seller offers: 681 offer rows in the published table\. The table includes set details, seller names, condition, and prices in PLN\.

Summary from the public dataset description.

## Allegro LEGO seller prices / offers

681 total rows · 50 sampled · Output revision 2
Published: 2026-11-12T11:38:22.240043Z · Producing pipeline version: Unknown

[CSV sample](outputs/cb80154e1305/offers-92ab364e8f43/sample.csv) · [JSON sample](outputs/cb80154e1305/offers-92ab364e8f43/sample.json) · [Schema](outputs/cb80154e1305/offers-92ab364e8f43/schema.json)

| condition | currency | listed\_total\_with\_delivery\_pln | observed\_at\_utc | offer\_id | offer\_title | offer\_url | price\_pln |
| --- | --- | --- | --- | --- | --- | --- | --- |
| New | PLN | 88\.34 | 2026\-11\-12T11:15:21\.485558\+00:00 | 18064455445 | LEGO Creator 3 w 1 31146 Ciężarówka z platformą i helikopterem | [https://allegro\.pl/produkt/lego\-creator\-3\-w\-1\-31146\-ciezarowka\-z\-platforma\-i\-helikopterem\-c94f4167\-e391\-44cb\-85dc\-0ad7bf04ac77?offerId=18064455445](<https://allegro.pl/produkt/lego-creator-3-w-1-31146-ciezarowka-z-platforma-i-helikopterem-c94f4167-e391-44cb-85dc-0ad7bf04ac77?offerId=18064455445>) | 77\.85 |
| New | PLN | 88\.38 | 2026\-11\-12T11:15:21\.485558\+00:00 | 12339099726 | LEGO KLOCKI CREATOR 31146 \- LAWETA CIĘŻARÓWKA TIR Z HELIKOPTEREM 3w1 | [https://allegro\.pl/produkt/lego\-creator\-3\-w\-1\-31146\-ciezarowka\-z\-platforma\-i\-helikopterem\-c94f4167\-e391\-44cb\-85dc\-0ad7bf04ac77?offerId=12339099726](<https://allegro.pl/produkt/lego-creator-3-w-1-31146-ciezarowka-z-platforma-i-helikopterem-c94f4167-e391-44cb-85dc-0ad7bf04ac77?offerId=12339099726>) | 77\.89 |
| New | PLN | 89\.48 | 2026\-11\-12T11:15:21\.485558\+00:00 | 15030775303 | LEGO Creator 3w1 Samochód Ciężarówka helikopter Cysterna Samolot Auto | [https://allegro\.pl/produkt/lego\-creator\-3\-w\-1\-31146\-ciezarowka\-z\-platforma\-i\-helikopterem\-c94f4167\-e391\-44cb\-85dc\-0ad7bf04ac77?offerId=15030775303](<https://allegro.pl/produkt/lego-creator-3-w-1-31146-ciezarowka-z-platforma-i-helikopterem-c94f4167-e391-44cb-85dc-0ad7bf04ac77?offerId=15030775303>) | 78\.99 |
| New | PLN | 90\.39 | 2026\-11\-12T11:15:21\.485558\+00:00 | 15050443848 | LEGO CREATOR 3w1 31146 CIĘŻARÓWKA Z PLATFORMĄ I HELIKOPTEREM zestaw \+7 lat | [https://allegro\.pl/produkt/lego\-creator\-3\-w\-1\-31146\-ciezarowka\-z\-platforma\-i\-helikopterem\-c94f4167\-e391\-44cb\-85dc\-0ad7bf04ac77?offerId=15050443848](<https://allegro.pl/produkt/lego-creator-3-w-1-31146-ciezarowka-z-platforma-i-helikopterem-c94f4167-e391-44cb-85dc-0ad7bf04ac77?offerId=15050443848>) | 79\.9 |
| New | PLN | 90\.39 | 2026\-11\-12T11:15:21\.485558\+00:00 | 19110744588 | LEGO 31146 Creator 3w1 Pojazdy Ciężarówka Helikopter Samolot Na Prezent | [https://allegro\.pl/produkt/lego\-creator\-3\-w\-1\-31146\-ciezarowka\-z\-platforma\-i\-helikopterem\-c94f4167\-e391\-44cb\-85dc\-0ad7bf04ac77?offerId=19110744588](<https://allegro.pl/produkt/lego-creator-3-w-1-31146-ciezarowka-z-platforma-i-helikopterem-c94f4167-e391-44cb-85dc-0ad7bf04ac77?offerId=19110744588>) | 79\.9 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| condition | text |
| currency | text |
| listed\_total\_with\_delivery\_pln | double precision |
| observed\_at\_utc | text |
| offer\_id | text |
| offer\_title | text |
| offer\_url | text |
| price\_pln | double precision |
| seller | text |
| set\_name | text |
| set\_number | text |
| source\_page | text |
| third\_party\_seller | boolean |

## How the pipeline works

```mermaid
flowchart LR
  n0["sets"]
  n1["seller#95;offers"]
  n2["deduplicate"]
  n3["offers"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **sets**: Select the LEGO sets from the saved twelve\-set panel\.
- **seller\_offers**: Read the first seller\-offer page for each LEGO set and exclude Allegro's own retail offers\.
- **deduplicate**: Keep one row for each exact seller offer in the latest snapshot\.
- **offers**: Current third\-party LEGO set offers in PLN, excluding Allegro retail\.

## Version history

- 2026-11-12T11:13:37.137797Z: v1: Saved the Allegro LEGO seller\-price snapshot as an on\-demand pipeline, with selectable sets and an option to include non\-new offers\.
- 2026-11-12T11:38:08.771614Z: v2: Corrected seller names beginning with hyphens so future refreshes no longer save Markdown escape characters\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/allegro-poland-lego-seller-prices-111dc8b854b2?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
