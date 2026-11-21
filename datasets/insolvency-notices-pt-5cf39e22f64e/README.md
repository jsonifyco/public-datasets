# Portugal Insolvency Notices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Public Citius insolvency notices for Lisboa and Porto, with debtor, court, publication date and published deadline details\.

[Get the full dataset for free](https://www.jsonify.com/datasets/insolvency-notices-pt-5cf39e22f64e?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 8
- Last published: 2026-11-21T06:27:12.882734Z

## The brief

> I need this data: Public Citius insolvency notices for Lisboa and Porto, with debtor, court, publication date and published deadline details\.

Summary from the public dataset description.

## Avisos de insolvência / avisos

311 total rows · 50 sampled · Output revision 21
Published: 2026-11-21T06:27:12.882734Z · Producing pipeline version: 8

[CSV sample](outputs/43cb4b753508/avisos-354cde498655/sample.csv) · [JSON sample](outputs/43cb4b753508/avisos-354cde498655/sample.json) · [Schema](outputs/43cb4b753508/avisos-354cde498655/schema.json)

| Distrito | Estado do prazo | NIF ou NIPC | Natureza do devedor | Prazo publicado | Processo | Publicado em | Tipo de anúncio |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Lisboa | Prazo não identificado no documento | 175499608 | Pessoa singular | None | 9672/26\.5T8SNT | 2026\-11\-18 | Outro |
| Porto | Prazo identificado no documento | 264157931 | Pessoa singular | O prazo para a Reclamação de Créditos foi fixado em 30 dias\. Os prazos começam a correr finda a dilação de 5 dias, que se conta da data da publicação do anúncio eletrónico na Área de Serviços Digitais dos Tribunais\. | 9131/26\.6T8VNG | 2026\-11\-20 | declaração de insolvência |
| Lisboa | Prazo não identificado no documento | 513737286 | Empresa | None | 11171/26\.6T8LSB | 2026\-11\-20 | Outro |
| Porto | Prazo não identificado no documento | 513631011 | Empresa | None | 1520/26\.2T8STS\-E | 2026\-11\-19 | Outro |
| Lisboa | Não verificado: documento indisponível | 140150668; 104134828 | Pessoa singular | None | 2010/18\.2T8VFX | 2026\-11\-20 | encerramento |

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

311 total rows · 50 sampled · Output revision 21
Published: 2026-11-21T06:27:12.882734Z · Producing pipeline version: 8

[CSV sample](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/sample.csv) · [JSON sample](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/sample.json) · [Schema](outputs/43cb4b753508/insolvency-notices-pt-0eb817203930/schema.json)

| claims\_deadline | court | debtor\_name | debtor\_nif | debtor\_type | district | insolvency\_administrator | notice\_type |
| --- | --- | --- | --- | --- | --- | --- | --- |
| None | Comarca do Porto \- Vila Nova de Gaia / Juízo de Comércio de Vila Nova de Gaia \- Juiz 4 | João André dos Santos Nunes | 231857004 | individual | Porto | António Coimbra Rodrigues | other |
| None | Vila Nova de Gaia \- Tribunal Judicial da Comarca do Porto / Juízo de Comércio de Vila Nova de Gaia \- Juiz 4 | Cláudia Salomé Machado Areosa | 220072469 | individual | Porto | Graça Isabel Ferreira Lopes da Cunha | other |
| None | Comarca de Lisboa Norte \- Vila Franca de Xira / Juízo de Comércio de Vila Franca de Xira \- Juiz 1 | Body Mix Center \- Gestão de Actividades de Fitness, Unipessoal, Limitada | 508698839 | company | Lisboa | Helena Maria Dias Barata | other |
| None | Comarca do Porto \- Vila Nova de Gaia / Juízo de Comércio de Vila Nova de Gaia \- Juiz 1 | Jonatan Torneri, Unipessoal Lda | 517469022 | company | Porto | Teresa Paula Rodrigues Liberal Alegre da Silva Pidwell Silva | PER |
| None | Comarca de Lisboa Norte \- Vila Franca de Xira / Juízo de Comércio de Vila Franca de Xira \- Juiz 1 | Carlos Alberto da Cruz Maucabelo; Margarida Maria Laranjeiro Relego | 140150668; 104134828 | individual | Lisboa | Luís Manuel Ribeiro de Carvalho | encerramento |

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
- 2026-11-21T06:10:45.424652Z: v8: Recognize limited companies from their published legal names and validated corporate tax numbers when the court category omits debtor type\.

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
- 2026-11-21T06:03:01.889534Z: no change
- 2026-11-21T06:04:41.300276Z: no change
- 2026-11-21T06:14:02.803192Z: repaired
- 2026-11-21T06:27:52.258514Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/insolvency-notices-pt-5cf39e22f64e?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
