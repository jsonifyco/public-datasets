# Brazil Cleaning Appliance Prices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Compare payment\-specific prices for cleaning appliances from Kärcher, Mondial, Philco, Britânia and Electrolux in Brazil\. The published prices table contains 25 product price observations\.

[Get the full dataset for free](https://www.jsonify.com/datasets/wap-competitor-cleaning-appliance-prices-c12b17da7758?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 2
- Last published: 2026-11-12T09:31:50.891447Z

## The brief

> I need this data: Compare payment\-specific prices for cleaning appliances from Kärcher, Mondial, Philco, Britânia and Electrolux in Brazil\. The published prices table contains 25 product price observations\.

Summary from the public dataset description.

## WAP competitor cleaning appliance prices / prices

25 total rows · 10 sampled · Output revision 2
Published: 2026-11-12T09:31:50.891447Z · Producing pipeline version: 2

[CSV sample](outputs/35ef0c0660a0/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/35ef0c0660a0/prices-fe81f9390ffe/sample.json) · [Schema](outputs/35ef0c0660a0/prices-fe81f9390ffe/schema.json)

| brand | product | model | category | price\_brl | currency | payment\_basis | retail\_price\_brl |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Mondial | Robô Aspirador de Pó Pratic Clean Mondial Preto Bivolt RB\-12\-ST\-BL | RB\-12\-ST\-BL | Robot vacuum | 492\.21 | BRL | Upfront | 546\.9 |
| Britânia | Aspirador de Pó Britânia 2 tubos prolongadores 1250W Bas1430 | BAS1430 | Vacuum cleaner | 209\.9 | BRL | Retail/card total | 209\.9 |
| Britânia | Aspirador de Pó Vertical Britânia 2 em 1 1250W BAS1290V | BAS1290V | Vacuum cleaner | 179\.9 | BRL | Retail/card total | 179\.9 |
| Kärcher | Lavadora de Alta pressão Kärcher Compacta 1500 PSI 1400W | Compacta | Pressure washer | 319\.9 | BRL | Pix, paid in full | None |
| Philco | Aspirador de Pó Vertical Philco Deep Cleaning 2 em 1 1600W PAS31 | PAS31 | Vacuum cleaner | 319\.9 | BRL | Retail/card total | 319\.9 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| brand | text |
| product | text |
| model | text |
| category | text |
| price\_brl | double precision |
| currency | text |
| payment\_basis | text |
| retail\_price\_brl | double precision |
| additional\_verified\_pix\_price\_brl | double precision |
| upfront\_price\_brl | double precision |
| availability | text |
| product\_url | text |
| price\_source\_url | text |
| observed\_at\_utc | text |
| price\_evidence | text |
| payment\_terms | text |
| notes | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["products"]
  n1["load#95;products"]
  n2["collect#95;prices"]
  n3["validate#95;coverage"]
  n4["prices"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n0 --> n1
  n0 --> n1
```

- **products**: Five cleaning appliance products from each of five WAP competitor brands, with official product links\.
- **load\_products**: Load the selected 25\-product comparison panel from the saved official product links\.
- **collect\_prices**: Read each official Brazilian product page and capture its current retail and payment\-specific prices\.
- **validate\_coverage**: Confirm every selected product is represented before replacing the saved price snapshot\.
- **prices**: Current official\-store prices for the WAP competitor comparison panel\.

## Version history

- 2026-11-12T09:23:01.503125Z: v1: Created an on\-demand comparison of the same 25 cleaning appliances from five WAP competitor brands, with official\-store prices and payment terms\.
- 2026-11-12T09:31:25.529263Z: v2: Corrected Electrolux sale\-price selection and separated Mondial's unnamed upfront prices from verified Pix offers\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/wap-competitor-cleaning-appliance-prices-c12b17da7758?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
