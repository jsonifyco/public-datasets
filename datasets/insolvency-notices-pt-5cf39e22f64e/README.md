# Portugal Insolvency Notices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Public Citius insolvency notices with process, debtor, court, publication date and claims deadline details\. The published dataset contains 428 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/insolvency-notices-pt-5cf39e22f64e?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 2
- Last published: 2026-11-03T20:56:31.375712Z

## The brief

> I need this data: Public Citius insolvency notices with process, debtor, court, publication date and claims deadline details\. The published dataset contains 428 rows\.

Summary from the public dataset description.

## insolvency\_notices\_pt / insolvency\_notices\_pt

428 total rows · 50 sampled · Output revision 1
Published: 2026-11-03T20:56:31.375712Z · Producing pipeline version: 2

[CSV sample](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/sample.csv) · [JSON sample](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/sample.json) · [Schema](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/schema.json)

| claims\_deadline | court | debtor\_name | debtor\_nif | debtor\_type | district | insolvency\_administrator | notice\_type |
| --- | --- | --- | --- | --- | --- | --- | --- |
| None | Comarca de Lisboa \- Lisboa / Juízo de Comércio de Lisboa \- Juiz 3 | Ricardo Emanuel Henriques de Évora | 217613535 | individual | Lisboa | Vera Lúcia Ladeira Rodrigues | other |
| None | Comarca de Lisboa Norte \- Vila Franca de Xira / Juízo de Comércio de Vila Franca de Xira \- Juiz 2 | Visão de Lisboa \- Equipamentos Profissionais Cinematográficos Lda | 504389963 | company | Lisboa | António Pedro Ferreira Semblano Galhardo | declaração de insolvência |
| None | Sintra \- Tribunal Judicial da Comarca de Lisboa Oeste / Juízo de Comércio de Sintra \- Juiz 3 | Paulo Jorge Lisbão Rodrigues Arede | 105401315 | individual | Lisboa | António Joaquim Oliveira Vieira | encerramento |
| 30 dias, a contar do fim da dilação, que se conta da data da publicação do anúncio eletrónico na Área de Serviços Digitais dos Tribunais\. | Comarca de Lisboa Oeste \- Sintra / Juízo de Comércio de Sintra \- Juiz 1 | Mafalda Sofia Arnaud Rosa | 272645885 | individual | Lisboa | Inácio Ramos Peres | declaração de insolvência |
| None | Comarca de Lisboa Norte \- Vila Franca de Xira / Juízo de Comércio de Vila Franca de Xira \- Juiz 1 | Raúl António Luamba | 209742062 | individual | Lisboa | António Joaquim Oliveira Vieira | other |

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
  n0["courts"]
  n1["search#95;notices"]
  n2["deduplicate"]
  n3["read#95;document"]
  n4["sort"]
  n5["insolvency#95;notices#95;pt"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
```

- **courts**: Find all listed court locations serving the districts of Lisboa and Porto\.
- **search\_notices**: Search each district court for recent notices and follow every results page\.
- **deduplicate**: Keep the newest notice for each process and notice category, as requested\.
- **read\_document**: Read each public notice document for the published credit\-claim deadline and confirm debtor type\.
- **sort**: Sort the final notice dataset by publication date, newest first\.
- **insolvency\_notices\_pt**: Public Citius insolvency notices for Lisboa and Porto in the last seven days\.

## Version history

- 2026-11-03T20:18:40.030465Z: v1: Create a daily\-ready Citius collection of recent public insolvency notices for Lisboa and Porto, with debtor details and published claims deadlines\.
- 2026-11-03T20:30:12.769767Z: v2: Recover missing debtor details for ancillary notices from their exact main court process so those notices no longer stop publication\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/insolvency-notices-pt-5cf39e22f64e?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
