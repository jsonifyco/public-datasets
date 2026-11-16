# EU and National Legal Acts

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

EU and national legal acts: a published dataset of 300 records with act dates, identifiers and links to official sources\.

[Get the full dataset for free](https://www.jsonify.com/datasets/eu-and-national-legal-acts-a0597b835d9f?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-11-16T10:32:46.914250Z

## The brief

> I need this data: EU and national legal acts: a published dataset of 300 records with act dates, identifiers and links to official sources\.

Summary from the public dataset description.

## EU and national legal acts / main

300 total rows · 50 sampled · Output revision 1
Published: 2026-11-16T10:32:46.914250Z · Producing pipeline version: 1

[CSV sample](outputs/0f4423c42df2/main-0d6e4079e367/sample.csv) · [JSON sample](outputs/0f4423c42df2/main-0d6e4079e367/sample.json) · [Schema](outputs/0f4423c42df2/main-0d6e4079e367/schema.json)

| act\_number | act\_type | celex | document\_date | document\_date\_basis | eli | gazette\_reference | issuing\_body |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 2026/2466 | Implementing regulation | 32026R2466 | 2026\-10\-28 | Cellar document date | [http://data\.europa\.eu/eli/reg\_impl/2026/2466/oj](<http://data.europa.eu/eli/reg_impl/2026/2466/oj>) | OJ L, 2026/2466, 2026\-10\-29 | European Commission; Directorate\-General for Health and Food Safety |
| 2026/2395 | Implementing decision | 32026D2395 | 2026\-10\-22 | Cellar document date | [http://data\.europa\.eu/eli/dec\_impl/2026/2395/oj](<http://data.europa.eu/eli/dec_impl/2026/2395/oj>) | OJ L, 2026/2395, 2026\-10\-26 | European Commission; Directorate\-General for Health and Food Safety |
|  | Arrêté |  | 2026\-11\-03 | Date in official act title | [https://www\.legifrance\.gouv\.fr/eli/arrete/2026/11/3/JUSF2629462A/jo/texte](<https://www.legifrance.gouv.fr/eli/arrete/2026/11/3/JUSF2629462A/jo/texte>) | JORF n° 0260 du 6 novembre 2026; texte n° 10 | Ministère de la justice |
| 2026/2370 | Implementing decision | 32026D2370 | 2026\-10\-28 | Cellar document date | [http://data\.europa\.eu/eli/dec\_impl/2026/2370/oj](<http://data.europa.eu/eli/dec_impl/2026/2370/oj>) | OJ L, 2026/2370, 2026\-10\-29 | European Commission; Directorate\-General for Energy |
| 2023\-715 | Arrêté |  | 2026\-11\-03 | Date in official act title | [https://www\.legifrance\.gouv\.fr/eli/arrete/2026/11/3/MICB2624362A/jo/texte](<https://www.legifrance.gouv.fr/eli/arrete/2026/11/3/MICB2624362A/jo/texte>) | JORF n° 0260 du 6 novembre 2026; texte n° 36 | Ministère de la culture |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| act\_number | text |
| act\_type | text |
| celex | text |
| document\_date | text |
| document\_date\_basis | text |
| eli | text |
| gazette\_reference | text |
| issuing\_body | text |
| jurisdiction | text |
| language | text |
| metadata\_url | text |
| missing\_fields | text |
| nor | text |
| publication\_date | text |
| source | text |
| source\_id | text |
| title | text |
| url | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["saved"]
  n1["prepare"]
  n2["main"]
  n1 --> n2
  n0 --> n1
  n0 --> n1
```

- **saved**: Read the existing saved snapshot without contacting sources\.
- **prepare**: Preserve the saved fields, correct documented QA issues where applicable, and sort for public reading\.
- **main**: Saved sample records with original observation dates\.

## Version history

- 2026-11-16T10:32:14.134054Z: v1: Publish the existing saved sample with a neutral title and overview\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/eu-and-national-legal-acts-a0597b835d9f?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
