# Portugal Insolvency Notices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Public Citius insolvency notices with process, debtor, court, publication date and published deadline details\. The published dataset contains 680 rows across all tables\.

[Get the full dataset for free](https://www.jsonify.com/datasets/insolvency-notices-pt-5cf39e22f64e?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 7
- Last published: 2026-11-14T06:35:20.365413Z

## The brief

> I need this data: Public Citius insolvency notices with process, debtor, court, publication date and published deadline details\. The published dataset contains 680 rows across all tables\.

Summary from the public dataset description.

## Avisos de insolvência / avisos

340 total rows · 50 sampled · Output revision 14
Published: 2026-11-14T06:35:20.365413Z · Producing pipeline version: 7

[CSV sample](outputs/43cb4b753508/avisos-354cde498655/sample.csv) · [JSON sample](outputs/43cb4b753508/avisos-354cde498655/sample.json) · [Schema](outputs/43cb4b753508/avisos-354cde498655/schema.json)

| Distrito | Estado do prazo | NIF ou NIPC | Natureza do devedor | Prazo publicado | Processo | Publicado em | Tipo de anúncio |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Porto | Prazo identificado no documento | 271570725 | Pessoa singular | 30 dias; os prazos para reclamação de créditos começam a correr finda a dilação, que se conta da data da publicação do anúncio eletrónico na Área de Serviços Digitais dos Tribunais\. | 8856/26\.0T8VNG | 2026\-11\-10 | declaração de insolvência |
| Porto | Prazo não identificado no documento | 150974876 | Pessoa singular | None | 2565/26\.8T8STS | 2026\-11\-13 | Outro |
| Lisboa | Prazo identificado no documento | 242913695 | Pessoa singular | 30 dias, a contar do fim da dilação, que se conta da data da publicação do anúncio eletrónico na Área de Serviços Digitais dos Tribunais\. | 18407/26\.1T8SNT | 2026\-11\-12 | declaração de insolvência |
| Porto | Prazo não identificado no documento | 515721441 | Empresa | None | 1092/26\.8T8AMT\-D | 2026\-11\-10 | Outro |
| Porto | Prazo identificado no documento | 514564130 | Empresa | No prazo de trinta dias, findos os cinco dias dos éditos contados da publicação deste edital\. | 6437/26\.8T8VNG\-B | 2026\-11\-13 | Outro |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| Distrito | text |
| Estado do prazo | text |
| NIF ou NIPC | text |
| Natureza do devedor | text |
| Prazo publicado | text |
| Processo | text |
| Publicado em | text |
| Tipo de anúncio | text |
| Tribunal | text |
| Ver anúncio no Citius | text |
| name | text |

## Avisos de insolvência / insolvency\_notices\_pt

340 total rows · 50 sampled · Output revision 14
Published: 2026-11-14T06:35:20.365413Z · Producing pipeline version: 7

[CSV sample](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/sample.csv) · [JSON sample](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/sample.json) · [Schema](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/schema.json)

| claims\_deadline | court | debtor\_name | debtor\_nif | debtor\_type | district | insolvency\_administrator | notice\_type |
| --- | --- | --- | --- | --- | --- | --- | --- |
| None | Vila Franca de Xira \- Tribunal Judicial da Comarca de Lisboa Norte / Juízo de Comércio de Vila Franca de Xira \- Juiz 3 | Márcio Casimiro Lopes Vaz | 212913689 | individual | Lisboa | Martinho Fernandes Luís | other |
| None | Comarca do Porto \- Santo Tirso / Juízo de Comércio de Santo Tirso \- Juiz 7 | Elisabete Maria Monteiro da Silva | 215071808 | individual | Porto | Andreia Sofia Lopes da Silva Penetra Gonçalves | other |
| None | Lisboa \- Tribunal Judicial da Comarca de Lisboa / Juízo de Comércio de Lisboa \- Juiz 3 | Pmp Consultores de Engenharia Lda | 510017762 | company | Lisboa | Patrícia Sofia Marques Navalho | encerramento |
| None | Comarca de Lisboa Oeste \- Sintra / Juízo de Comércio de Sintra \- Juiz 2 | Nelson Manuel Monte Salazar | 217320066 | individual | Lisboa | Maria José Ramos Peres dos Reis | other |
| 30 dias, a contar do fim da dilação, que se conta da data da publicação do anúncio eletrónico na Área de Serviços Digitais dos Tribunais\. | Comarca de Lisboa Oeste \- Sintra / Juízo de Comércio de Sintra \- Juiz 6 | Roger Duarte Simões de Oliveira Medeiros | 230586945 | individual | Lisboa | Fernando Marinho Vaz | declaração de insolvência |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| claims\_deadline | text |
| court | text |
| debtor\_name | text |
| debtor\_nif | text |
| debtor\_type | text |
| district | text |
| insolvency\_administrator | text |
| notice\_type | text |
| process\_number | text |
| published\_date | text |
| source | text |
| summary | text |
| url | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["verified#95;notices"]
  n1["courts"]
  n2["search#95;notices"]
  n3["deduplicate"]
  n4["read#95;document"]
  n5["sort"]
  n6["insolvency#95;notices#95;pt"]
  n7["presentation"]
  n8["avisos"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n6 --> n7
  n7 --> n8
  n0 --> n1
  n0 --> n5
```

- **verified\_notices**: Optional saved notice snapshot for presentation\-only rebuilding; leave unset for live collection\.
- **courts**: Find all listed court locations serving the districts of Lisboa and Porto\.
- **search\_notices**: Search each district court for recent notices and follow every results page\.
- **deduplicate**: Keep the newest notice for each process and notice category, as requested\.
- **read\_document**: Read each public notice document for the published credit\-claim deadline and confirm debtor type\.
- **sort**: Sort the final notice dataset by publication date, newest first\.
- **insolvency\_notices\_pt**: Public Citius insolvency notices for Lisboa and Porto in the last seven days\.
- **presentation**: Present debtor\-first Portuguese fields and distinguish published deadlines from unavailable or unverified documents\.
- **avisos**: Vista de leitura dos anúncios, com prazos publicados e lacunas explícitas\.

## Version history

- 2026-11-03T20:18:40.030465Z: v1: Create a daily\-ready Citius collection of recent public insolvency notices for Lisboa and Porto, with debtor details and published claims deadlines\.
- 2026-11-03T20:30:12.769767Z: v2: Recover missing debtor details for ancillary notices from their exact main court process so those notices no longer stop publication\.
- 2026-11-03T21:28:29.970874Z: v3: Added a Portuguese notice reading worksheet with explicit deadline uncertainty and a debtor\-first, newest\-first download\. Preserved the complete original notice records separately\.
- 2026-11-03T22:29:41.581366Z: v4: Rows now use the exact debtor name as their native heading\. The dataset display name is Avisos de insolvência, with original notice data and Portuguese download preserved\.
- 2026-11-10T08:44:28.365557Z: v5: Retain the approved notice when its document is missing, keeping its deadline null and clearly marked unverified\. Read the document normally if Citius restores it\.
- 2026-11-13T06:10:20.221989Z: v6: Fixed updates stopping when Citius lists the same reference twice on one page\. Debtor lookups still stop if an entire results page repeats\.
- 2026-11-14T06:18:51.091945Z: v7: Fixed updates stopping on different name spellings in related court records\. Conflicting names are left unused while the exact notice document supplies missing details\.

## Recorded repairs

- 2026-11-10T06:19:09.875431Z: no change
- 2026-11-10T06:23:14.143851Z: temporary blocker
- 2026-11-13T06:04:29.364410Z: no change
- 2026-11-13T06:05:37.531429Z: no change
- 2026-11-13T06:10:27.344481Z: repaired
- 2026-11-14T06:11:47.627162Z: no change
- 2026-11-14T06:12:40.675800Z: no change
- 2026-11-14T06:19:00.669024Z: repaired
- 2026-11-14T06:35:50.871073Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/insolvency-notices-pt-5cf39e22f64e?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
