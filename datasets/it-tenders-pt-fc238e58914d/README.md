# Portugal IT Tender Notices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Portugal IT tender notices from TED, with publication dates, deadlines, contracting entities, CPV codes and published estimated values\. The published dataset contains 156 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/it-tenders-pt-fc238e58914d?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 4
- Last published: 2026-11-09T06:09:22.261148Z

## The brief

> I need this data: Portugal IT tender notices from TED, with publication dates, deadlines, contracting entities, CPV codes and published estimated values\. The published dataset contains 156 rows\.

Summary from the public dataset description.

## Portugal IT tenders / Tenders

78 total rows · 10 sampled · Output revision 9
Published: 2026-11-09T06:09:22.261148Z · Producing pipeline version: 4

[CSV sample](outputs/cebd25590c7c/tenders-7e626c78fe5c/sample.csv) · [JSON sample](outputs/cebd25590c7c/tenders-7e626c78fe5c/sample.json) · [Schema](outputs/cebd25590c7c/tenders-7e626c78fe5c/schema.json)

| Buyer | CPV | Data notes | Deadline Lisbon | Estimated value EUR | Notice type | Procedure | Published date |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Município de Alter do Chão | 30200000 | None | 2026\-12\-01T17:00:59\+00:00 | 225000 | Contract notice | Open procedure | 2026\-11\-02 |
| Autoridade Tributária e Aduaneira | 72200000 | No submission deadline published | None | 168000 | Contract notice | Restricted procedure | 2026\-10\-29 |
| Universidade Nova de Lisboa | 72510000 | No submission deadline published | None | 1975000 | Contract notice | Restricted procedure | 2026\-11\-04 |
| Instituto de Gestão Financeira e Equipamentos da Justiça, IP | 72910000 | None | 2026\-12\-04T23:59:59\+00:00 | 855400 | Contract notice | Open procedure | 2026\-11\-04 |
| SPMS, EPE \- Serviços Partilhados do Ministério da Saúde, EPE | 30230000 | No submission deadline published | None | 92391\.5 | Contract award / result notice | Restricted procedure | 2026\-10\-28 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| Buyer | text |
| CPV | text |
| Data notes | text |
| Deadline Lisbon | text |
| Estimated value EUR | double precision |
| Notice type | text |
| Procedure | text |
| Published date | text |
| Status | text |
| source | text |
| title | text |

## Portugal IT tenders / it\_tenders\_pt

78 total rows · 10 sampled · Output revision 9
Published: 2026-11-09T06:09:22.261148Z · Producing pipeline version: 4

[CSV sample](outputs/cebd25590c7c/it-tenders-pt-d565827789da/sample.csv) · [JSON sample](outputs/cebd25590c7c/it-tenders-pt-d565827789da/sample.json) · [Schema](outputs/cebd25590c7c/it-tenders-pt-d565827789da/schema.json)

| base\_price\_eur | checked\_at | contracting\_entity | cpv | description | form\_type\_code | location | notice\_subtype\_code |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1396240 | 2026\-11\-09T06:09:17\.116353\+00:00 | Instituto dos Registos e do Notariado, IP | \["72000000"\] | Aquisição de serviços de implementação de infraestrutura de plataforma como serviço \(IAAS, PAAS E SAAS\) e serviços de consultoria para a operação e monitorização da plataforma BUPI CLOUD 2027\. | competition | A prestação dos serviços será efetuada em modo híbrido, estando prevista a presença da equipa técnica da entidade adjudicatária nas instalações em Lisboa do IRN, I\.P\. ou IGFEJ | 16 |
| 400930 | 2026\-11\-09T06:09:17\.116353\+00:00 | Serviços Partilhados do Ministério da Saúde, EPE | \["72500000"\] | \(DAG\) Aquisição de serviços de desenvolvimento do novo website do INFARMED, I\.P\. \(PRR\) \(20260267\)\. | competition | Lisboa | 16 |
| 508220 | 2026\-11\-09T06:09:17\.116353\+00:00 | Serviços Partilhados do Ministério da Saúde, EPE | \["72500000"\] | Aquisição de serviços de desenvolvimento de novas funcionalidades no Portal Licenciamento\+, do INFARMED, I\.P\. \(PRR\)\. | competition | Lisboa | 16 |
| 611735 | 2026\-11\-09T06:09:17\.116353\+00:00 | Serviços Partilhados do Ministério da Saúde, EPE | \["72500000"\] | Aquisição de serviços de desenvolvimento de novas funcionalidades no Portal Inspeção\+, do INFARMED, I\.P\. \(PRR\)\. | competition | Lisboa | 16 |
| 168652\.2 | 2026\-11\-09T06:09:17\.116353\+00:00 | Autoridade Nacional de Segurança Rodoviária | \["72260000"\] | Aquisição de licenciamento Microsoft Fabric em ambiente Microsoft Azure \(CSP\) para suporte ao projeto Data &amp; Analytics\. | competition | Freguesia de Barcarena | 16 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| base\_price\_eur | double precision |
| checked\_at | text |
| contracting\_entity | text |
| cpv | jsonb |
| description | text |
| form\_type\_code | text |
| location | text |
| notice\_subtype\_code | text |
| notice\_type\_code | text |
| procedure\_type | text |
| published\_date | text |
| source | text |
| source\_record | jsonb |
| submission\_deadline | text |
| title | text |
| url | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["collect#95;ted"]
  n1["normalize"]
  n2["presentation"]
  n3["Tenders"]
  n4["source#95;evidence"]
  n5["it#95;tenders#95;pt"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
```

- **collect\_ted**: Read Portuguese TED notices in the publication window for the selected technology CPV prefixes\.
- **normalize**: Keep qualifying notices, retain published values, remove duplicate URLs, and order earliest submission deadlines first\.
- **presentation**: Build a readable tender view with honest opportunity status and keep exact source evidence in a separate worksheet\.
- **Tenders**: Readable tender notices\. Status is evaluated at refresh; missing deadlines are not open opportunities\. Euro values are estimates, not awards\.
- **source\_evidence**: Retain original columns, URL joins, full descriptions and exact TED records separately from the customer view\.
- **it\_tenders\_pt**: Original tender fields and exact source evidence for audit and technical joins\.

## Version history

- 2026-11-03T19:54:38.279055Z: v1: Create the daily Portugal technology tenders collection using the working public TED source\.
- 2026-11-03T20:16:22.718967Z: v2: Use the detailed TED lot description when the main description contains only a procurement reference\.
- 2026-11-03T21:29:16.747834Z: v3: Add a readable tender worksheet with meaningful titles and clear opportunity status, preserve full source evidence separately, and provide a formatted Excel export\.
- 2026-11-03T21:30:45.283621Z: v4: Keep workbook coverage notes accurate for the selected publication window and CPV categories\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/it-tenders-pt-fc238e58914d?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
