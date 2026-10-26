# TMview Class 36 Trademarks and Publicly Evidenced Company Websites

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

A refreshable, bounded sample of TMview registered Class 36 logo and combined trademarks, with applicant details and publicly evidenced company websites where matches are available\. Logo\-only names and unresolved website matches are retained\.

[Get the full dataset for free](https://www.jsonify.com/datasets/tmview-class-36-brands-and-websites-cabdb479e298?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-10-26T17:23:00.087271Z

## The brief

> I need this data: A refreshable, bounded sample of TMview registered Class 36 logo and combined trademarks, with applicant details and publicly evidenced company websites where matches are available\. Logo\-only names and unresolved website matches are retained\.

Summary from the public dataset description.

## TMview trademark sample / trademarks

10 total rows · 10 sampled · Output revision 1
Published: 2026-10-26T17:23:00.087271Z · Producing pipeline version: 1

[CSV sample](outputs/a092267a8904/trademarks-9cca72a552e8/sample.csv) · [JSON sample](outputs/a092267a8904/trademarks-9cca72a552e8/sample.json) · [Schema](outputs/a092267a8904/trademarks-9cca72a552e8/schema.json)

| trademark\_id | trademark\_name | applicant\_name | office | application\_number | application\_date | status | nice\_classes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| CO500020190057487 | CREDITLÓN LA MARATÓN DE CRÉDITOS FINANCIERA COMULTRASAN\. | COOPERATIVA DE AHORRO Y CREDITO DE SANTANDER LIMITADA, FINANCIERA COMULTRASAN O COMULTRASAN | CO | SD2019/0057487 | 2019\-07\-08 | Registered | 36 |
| CR500002023003390 | AFIANZADORA CAJA DE ANDE | CAJA DE AHORRO Y PRÉSTAMOS DE LA ASOCIACIÓN NACIONAL DE EDUCADORES | CR | 2023\-003390 | 2023\-05\-15 | Registered | 35, 36, 42 |
| CR500002023008366 | CREDI TODOS, EL CREDITO PARA TODOS | ALMACEN MOZEL SOCIEDAD ANONIMA, CJ | CR | 2023\-008366 | 2023\-08\-24 | Registered | 36 |
| CR500002021001224 | CAMBIAGRO | DISAGRO DE GUATEMALA S\.A\. | CR | 2021\-001224 | 2021\-02\-10 | Registered | 36 |
| CN500000514882936 | 图形 | 福建标致矿泉水有限公司 | CN | 5148829 | 2006\-02\-05 | Registered | 36 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| trademark\_id | text |
| trademark\_name | text |
| applicant\_name | text |
| office | text |
| application\_number | text |
| application\_date | text |
| status | text |
| nice\_classes | text |
| trademark\_url | text |
| logo\_url | text |
| search\_url | text |
| collected\_at | text |
| company\_website | text |
| website\_evidence\_url | text |
| website\_match\_note | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["matching#95;marks"]
  n1["company#95;websites"]
  n2["trademarks"]
  n0 --> n1
  n1 --> n2
```

- **matching\_marks**: Read a bounded page of registered class 36 combined and figurative trademarks from the supplied TMview search\.
- **company\_websites**: Find public company or brand websites for the trademark applicants, keeping uncertain identities unresolved\.
- **trademarks**: Matching trademark records with evidence\-backed company website matches where available\.

## Version history

- 2026-10-26T17:21:24.578621Z: v1: Added a TMview trademark sample with applicant details, source links and evidence\-backed company website matches\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/tmview-class-36-brands-and-websites-cabdb479e298?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
