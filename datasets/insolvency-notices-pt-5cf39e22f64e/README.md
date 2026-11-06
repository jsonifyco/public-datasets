# Portugal Insolvency Notices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Public Citius insolvency notices with process, debtor, court, publication date and published deadline details\. The published dataset contains 634 rows across all tables\.

[Get the full dataset for free](https://www.jsonify.com/datasets/insolvency-notices-pt-5cf39e22f64e?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 4
- Last published: 2026-11-06T06:19:34.481960Z

## The brief

> I need this data: Public Citius insolvency notices with process, debtor, court, publication date and published deadline details\. The published dataset contains 634 rows across all tables\.

Summary from the public dataset description.

## Avisos de insolvência / avisos

317 total rows · 50 sampled · Output revision 6
Published: 2026-11-06T06:19:34.481960Z · Producing pipeline version: 4

[CSV sample](outputs/43cb4b753508/avisos-354cde498655/sample.csv) · [JSON sample](outputs/43cb4b753508/avisos-354cde498655/sample.json) · [Schema](outputs/43cb4b753508/avisos-354cde498655/schema.json)

| Distrito | Estado do prazo | NIF ou NIPC | Natureza do devedor | Prazo publicado | Processo | Publicado em | Tipo de anúncio |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Porto | Prazo não identificado no documento | 178691836 | Pessoa singular | None | 10495/22\.6T8VNG | 2026\-11\-04 | Outro |
| Lisboa | Não verificado: documento indisponível | 232104034 | Pessoa singular | None | 12953/26\.4T8SNT | 2026\-11\-05 | encerramento |
| Lisboa | Prazo não identificado no documento | 215595319 | Pessoa singular | None | 12235/23\.3T8SNT | 2026\-11\-03 | Outro |
| Porto | Prazo não identificado no documento | 245838317 | Pessoa singular | None | 6553/26\.6T8VNG | 2026\-11\-04 | Outro |
| Porto | Prazo não identificado no documento | 205456332 | Pessoa singular | None | 1253/26\.0T8AMT | 2026\-11\-02 | encerramento |

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

317 total rows · 50 sampled · Output revision 6
Published: 2026-11-06T06:19:34.481960Z · Producing pipeline version: 4

[CSV sample](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/sample.csv) · [JSON sample](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/sample.json) · [Schema](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/schema.json)

| claims\_deadline | court | debtor\_name | debtor\_nif | debtor\_type | district | insolvency\_administrator | notice\_type |
| --- | --- | --- | --- | --- | --- | --- | --- |
| None | Amarante \- Tribunal Judicial da Comarca do Porto Este / Juízo de Comércio de Amarante \- Juiz 1 | Armando Teixeira Soares; Marilia da Conceição dos Santos Vieira | 199641854; 206722265 | individual | Porto | Andreia Sofia Lopes da Silva Penetra Gonçalves | declaração de insolvência |
| None | Comarca de Lisboa Norte \- Vila Franca de Xira / Juízo de Comércio de Vila Franca de Xira \- Juiz 4 | Antonio Fernando Pereira Lopes Pinto | 162697643 | individual | Lisboa | João Manuel Cortes Pirra Salvado Martinho | other |
| None | Vila Franca de Xira \- Tribunal Judicial da Comarca de Lisboa Norte / Juízo de Comércio de Vila Franca de Xira \- Juiz 1 | CARLOS MANUEL VAZ RODRIGUES; Marina Rute Pires da Costa Rodrigues | 174964935; 225334267 | individual | Lisboa | Carlos Alberto Vecino Vieira | other |
| None | Comarca do Porto \- Santo Tirso / Juízo de Comércio de Santo Tirso \- Juiz 7 | Natália Sofia Mota Pinto | 192669796 | individual | Porto | Isidro da Purificação Correia | other |
| None | Comarca do Porto Este \- Amarante / Juízo de Comércio de Amarante \- Juiz 4 | Francisco Ferreira Veloso | 136358705 | individual | Porto | Miguel Augusto Rodrigues Matos Torres | other |

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

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/insolvency-notices-pt-5cf39e22f64e?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
