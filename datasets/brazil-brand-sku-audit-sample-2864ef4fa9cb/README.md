# Brazil Marketplace Brand and SKU Audit Sample

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Brazil marketplace product listing sample with brand, seller, price, and listing evidence\.

[Get the full dataset for free](https://www.jsonify.com/datasets/brazil-brand-sku-audit-sample-2864ef4fa9cb?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-11-13T16:01:33.398477Z

## The brief

> I need this data: Brazil marketplace product listing sample with brand, seller, price, and listing evidence\.

Summary from the public dataset description.

## Brazil brand SKU audit sample / main

300 total rows · 50 sampled · Output revision 1
Published: 2026-11-13T16:01:33.398477Z · Producing pipeline version: 1

[CSV sample](outputs/bb2ff34b0191/main-0d6e4079e367/sample.csv) · [JSON sample](outputs/bb2ff34b0191/main-0d6e4079e367/sample.json) · [Schema](outputs/bb2ff34b0191/main-0d6e4079e367/schema.json)

| brand | captured\_at | detail\_captured\_at | evidence\_url | image\_url | key\_attributes | list\_was\_price\_brl | listing\_id |
| --- | --- | --- | --- | --- | --- | --- | --- |
| L’Oréal | 2026\-11\-09T13:21:13\.152314\+00:00 | None | [https://www\.magazineluiza\.com\.br/busca/loreal\+paris/](<https://www.magazineluiza.com.br/busca/loreal+paris/>) | [https://a\-static\.mlcdn\.com\.br/800x800/l\-oreal\-paris\-revitalift\-hialuronico\-kit\-creme\-noturno\-serum\-anti\-idade/epocacosmeticos\-integra/61412/76551a31524b9f1af0956e23c59defca\.jpeg](<https://a-static.mlcdn.com.br/800x800/l-oreal-paris-revitalift-hialuronico-kit-creme-noturno-serum-anti-idade/epocacosmeticos-integra/61412/76551a31524b9f1af0956e23c59defca.jpeg>) | \{"Tamanho": "Kit"} | 287\.79 | ck2967c04f |
| L’Oréal | 2026\-11\-09T13:19:49\.841426\+00:00 | None | [https://www\.magazineluiza\.com\.br/busca//](<https://www.magazineluiza.com.br/busca//>) | [https://a\-static\.mlcdn\.com\.br/800x800/protetor\-solar\-facial\-loreal\-paris\-expertise\-fps30\-antioleosidade\-40g\-acido\-salicilico\-matte\-12h\-loreal\-paris\-alta\-protecao/gevstore/lorealantioleosidade40gfps30/f6a0e69b2d9626c5517228d2087fda4d\.jpeg](<https://a-static.mlcdn.com.br/800x800/protetor-solar-facial-loreal-paris-expertise-fps30-antioleosidade-40g-acido-salicilico-matte-12h-loreal-paris-alta-protecao/gevstore/lorealantioleosidade40gfps30/f6a0e69b2d9626c5517228d2087fda4d.jpeg>) | \{"size": \["40g"\], "Volume": "40 g", "Tom de pele": "Sem cor"} | 81\.76 | ag4hf7fgf2 |
| L’Oréal | 2026\-11\-09T13:25:03\.974936\+00:00 | 2026\-11\-09T13:25:03\.974936\+00:00 | [https://www\.amazon\.com\.br/dp/B0DDDKZLJP](<https://www.amazon.com.br/dp/B0DDDKZLJP>) | [https://m\.media\-amazon\.com/images/I/51YbaKlw\-PL\.\_AC\_SX342\_SY445\_QL70\_ML2\_\.jpg](<https://m.media-amazon.com/images/I/51YbaKlw-PL._AC_SX342_SY445_QL70_ML2_.jpg>) | \{} | 74\.9 | B0DDDKZLJP |
| Samsung | 2026\-11\-09T13:25:09\.405927\+00:00 | 2026\-11\-09T13:25:09\.405927\+00:00 | [https://www\.amazon\.com\.br/dp/B0CVCG6S9C](<https://www.amazon.com.br/dp/B0CVCG6S9C>) | [https://m\.media\-amazon\.com/images/I/51It6ch5f7L\.\_AC\_SX300\_SY300\_QL70\_ML2\_\.jpg](<https://m.media-amazon.com/images/I/51It6ch5f7L._AC_SX300_SY300_QL70_ML2_.jpg>) | \{"size": \["1\.6\\""\], "model": \["Galaxy Fit3"\], "colour": \["Prata"\]} | 549 | B0CVCG6S9C |
| Nestlé | 2026\-11\-09T13:24:53\.097956\+00:00 | 2026\-11\-09T13:24:53\.097956\+00:00 | [https://www\.amazon\.com\.br/dp/B0FJDLS2KD](<https://www.amazon.com.br/dp/B0FJDLS2KD>) | [https://m\.media\-amazon\.com/images/I/71ke3HspqxL\.\_AC\_SY300\_SX300\_QL70\_ML2\_\.jpg](<https://m.media-amazon.com/images/I/71ke3HspqxL._AC_SY300_SX300_QL70_ML2_.jpg>) | \{"size": \["160g"\]} | 18\.99 | B0FJDLS2KD |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| brand | text |
| captured\_at | text |
| detail\_captured\_at | text |
| evidence\_url | text |
| image\_url | text |
| key\_attributes | jsonb |
| list\_was\_price\_brl | double precision |
| listing\_id | text |
| listing\_title | text |
| listing\_url | text |
| marketplace | text |
| official\_store\_flag | boolean |
| price\_brl | double precision |
| price\_terms | text |
| rating | double precision |
| review\_count | integer |
| review\_count\_basis | text |
| search\_captured\_at | text |
| seller\_id | text |
| seller\_name | text |
| source\_brand | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["saved0"]
  n1["prepare"]
  n2["tables"]
  n3["main"]
  n1 --> n2
  n2 --> n3
  n0 --> n1
  n0 --> n1
```

- **saved0**: Read the existing saved worksheet without contacting any sources\.
- **prepare**: Copy the saved sample and sort it for public reading without refreshing sources\.
- **tables**: Keep the saved worksheets separate in the public workbook\.
- **main**: Existing saved sample records\.

## Version history

- 2026-11-13T16:01:20.166347Z: v1: Make the saved sample available for a neutral public page without new collection\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/brazil-brand-sku-audit-sample-2864ef4fa9cb?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
