# Companies Hiring at Scale in Poland

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

A published dataset of 96 companies advertising at least 50 jobs on one public source, with counts from Pracuj\.pl, Indeed Poland, and accessible company careers pages\. The publication timestamp does not establish when the job listings were observed\.

[Get the full dataset for free](https://www.jsonify.com/datasets/companies-hiring-at-scale-in-poland-50-open-roles-1be11bee1c95?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-11-13T18:22:40.358613Z

## The brief

> I need this data: A published dataset of 96 companies advertising at least 50 jobs on one public source, with counts from Pracuj\.pl, Indeed Poland, and accessible company careers pages\. The publication timestamp does not establish when the job listings were observed\.

Summary from the public dataset description.

## Companies Hiring at Scale in Poland: 50\+ Open Roles / companies

96 total rows · 10 sampled · Output revision 2
Published: 2026-11-13T18:22:40.358613Z · Producing pipeline version: Unknown

[CSV sample](outputs/bf9089355748/companies-1701cfb023a1/sample.csv) · [JSON sample](outputs/bf9089355748/companies-1701cfb023a1/sample.json) · [Schema](outputs/bf9089355748/companies-1701cfb023a1/schema.json)

| careers\_count\_note | careers\_page\_count | careers\_page\_url | company\_domain | company\_name | example\_job\_titles | hybrid\_share | indeed\_count |
| --- | --- | --- | --- | --- | --- | --- | --- |
| No explicit current Poland\-only job total exposed on the easy careers page\. | None | [https://sii\.pl/oferty\-pracy/](<https://sii.pl/oferty-pracy/>) | sii\.pl | Sii Sp\. z o\.o\. | \["Associate Business Manager – sektor Public &amp; Utilities \(f/m/x\)", "Senior ServiceNow Developer \(f/m/x\)", "Python Test Automation Engineer with AWS \(f/m/x\)"\] | 0\.9053 | None |
| Wyniki 1 – 20 z 1288 | 1288 | [https://careers\.jeronimomartins\.com/Biedronka/search/?locale=pl\_PL](<https://careers.jeronimomartins.com/Biedronka/search/?locale=pl_PL>) | biedronka\.pl | Biedronka \(Jeronimo Martins Polska S\.A\.\) | \["Sprzedawca\-kasjer \(m/k\) \| Mile widziane osoby z niepełnosprawnością", "Sprzedawca \- Lada Tradycyjna \(m/k\) \| Mile widziane osoby z niepełnosprawnością", "Kierownik sklepu \(m/k\)"\] | 0 | None |
| No easy public careers link found on the employer profile\. | None | None | capgemini\.com | Capgemini Polska | \["Project Manager \(Custom Application Development, with German\)", "Business Analyst \(with German\)", "Senior Consultant \(Workday Integration\)"\] | 1 | None |
| No explicit current Poland\-only job total exposed on the easy careers page\. | None | [https://kariera\.stokrotka\.pl/oferty\-pracy/](<https://kariera.stokrotka.pl/oferty-pracy/>) | stokrotka\.pl | Stokrotka Sp\. z o\.o\. | \["Magazynier / Magazynierka – Kompletacja Towaru", "Kierowca kat\. C / Kierowczyni kat\. C", "Pracownik / Pracownica Sklepu \- również dla osób z orzeczeniem o niepełnosprawności"\] | 0 | None |
| No explicit current Poland\-only job total exposed on the easy careers page\. | None | [https://www\.nn\.pl/kariera/lista\-ofert](<https://www.nn.pl/kariera/lista-ofert>) | nn\.pl | Nationale\-Nederlanden | \["Młodszy Menadżer / Młodsza Menadżerka Zespołu Sprzedaży \(nowy zespół\)", "Analityko\-Tester Systemowy / Analityko\-Testerka Systemowa", "Doradca / Doradczyni Klienta"\] | 0\.8121 | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| careers\_count\_note | text |
| careers\_page\_count | bigint |
| careers\_page\_url | text |
| company\_domain | text |
| company\_name | text |
| example\_job\_titles | jsonb |
| hybrid\_share | double precision |
| indeed\_count | bigint |
| indeed\_count\_note | text |
| indeed\_source\_url | text |
| industry | jsonb |
| metrics\_basis | text |
| most\_recent\_posting\_date | text |
| open\_roles\_total | bigint |
| pracuj\_count | bigint |
| pracuj\_distinct\_job\_groups | bigint |
| pracuj\_source\_url | text |
| profile\_url | text |
| remote\_share | double precision |
| scraped\_at | text |
| top\_3\_job\_functions | jsonb |
| top\_locations | jsonb |
| website | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["employers"]
  n1["candidates"]
  n2["company"]
  n3["deduplicate"]
  n4["companies"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n0 --> n1
  n0 --> n1
```

- **employers**: Public employer\-profile candidates discovered from Pracuj, with observed directory counts\.
- **candidates**: Use the saved public employer directory candidates for this one\-off Poland sample\.
- **company**: Read each employer profile and every Poland\-filtered Pracuj results page, then check public Indeed and easy careers links\.
- **deduplicate**: Deduplicate exact normalized company names and official domains, then rank by highest source count\.
- **companies**: Companies with at least 50 Poland\-only public job postings on one available source\.

## Version history

- 2026-11-13T17:55:21.686527Z: v1: Build a one\-off Poland hiring snapshot with separate source counts, job examples and locations\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/companies-hiring-at-scale-in-poland-50-open-roles-1be11bee1c95?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
