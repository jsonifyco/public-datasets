# Law Firm Events

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Event records associated with Abreu Advogados, PLMJ, VdA, Morais Leitão, Cuatrecasas, Garrigues and Uría Menéndez, with event details and source links\. The published dataset contains 20 event records\.

[Get the full dataset for free](https://www.jsonify.com/datasets/law-firm-events-4c408bd04e11?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 5
- Last published: 2026-11-17T09:05:51.491779Z

## The brief

> I need this data: Event records associated with Abreu Advogados, PLMJ, VdA, Morais Leitão, Cuatrecasas, Garrigues and Uría Menéndez, with event details and source links\. The published dataset contains 20 event records\.

Summary from the public dataset description.

## Law firm events / events

20 total rows · 10 sampled · Output revision 11
Published: 2026-11-17T09:05:51.491779Z · Producing pipeline version: 5

[CSV sample](outputs/b08d9aab8e59/events-862417b9e7c3/sample.csv) · [JSON sample](outputs/b08d9aab8e59/events-862417b9e7c3/sample.json) · [Schema](outputs/b08d9aab8e59/events-862417b9e7c3/schema.json)

| date\_note | description | end\_date | event\_date | event\_name | event\_time | event\_url | firm |
| --- | --- | --- | --- | --- | --- | --- | --- |
| None | Congresso sobre os desafios e o enquadramento jurídico do setor bancário e financeiro, reunindo juristas de bancos, da academia e da advocacia\. | None | 2026\-02\-25 | I Congresso de Direito Bancário e Financeiro | 09:00 | [https://www\.plmj\.com/pt/conhecimento/eventos/I\-Congresso\-de\-Direito\-Bancario\-e\-Financeiro/34295/](<https://www.plmj.com/pt/conhecimento/eventos/I-Congresso-de-Direito-Bancario-e-Financeiro/34295/>) | PLMJ |
| O anúncio indica 25 de novembro; o ano de 2026 é determinado pela data de publicação\. | Conferência sobre a evolução do direito civil português e os desafios para o futuro do Código Civil, por ocasião dos seus 60 anos\. | 2026\-11\-25 | 2026\-11\-25 | Conferência “Ler os Sinais do Tempo: do Mundo para o Direito” | None | [https://www\.mlgts\.pt/pt/conhecimento/noticias/Conferencia\-Ler\-os\-Sinais\-do\-Tempo\-do\-Mundo\-para\-o\-Direito/27186/](<https://www.mlgts.pt/pt/conhecimento/noticias/Conferencia-Ler-os-Sinais-do-Tempo-do-Mundo-para-o-Direito/27186/>) | Morais Leitão |
| As datas referem\-se às duas sessões anunciadas; o período completo da Semana da Reabilitação Urbana não é indicado\. | A Morais Leitão coorganiza duas sessões sobre alterações ao licenciamento urbanístico e a sua aplicação no setor imobiliário e da habitação, em 2 e 3 de novembro\. | 2026\-11\-03 | 2026\-11\-02 | 14\.ª edição da Semana da Reabilitação Urbana do Porto | None | [https://www\.mlgts\.pt/pt/conhecimento/noticias/Morais\-Leitao\-participa\-na\-14\-edicao\-da\-Semana\-da\-Reabilitacao\-Urbana\-do\-Porto/27161/](<https://www.mlgts.pt/pt/conhecimento/noticias/Morais-Leitao-participa-na-14-edicao-da-Semana-da-Reabilitacao-Urbana-do-Porto/27161/>) | Morais Leitão |
| O anúncio indica que o congresso decorre ao longo de dois dias, mas não identifica expressamente a data do segundo dia\. | Congresso de dois dias sobre o direito e a regulação das infraestruturas digitais, incluindo cabos submarinos, centros de dados, cloud e identidade digital\. | None | 2026\-10\-27 | I Congresso de Direito das Infraestruturas Digitais: Regulação e Poder | 09:00 | [https://www\.plmj\.com/pt/conhecimento/eventos/I\-Congresso\-de\-Direito\-das\-Infraestruturas\-Digitais\-Regulacao\-e\-Poder/34662/](<https://www.plmj.com/pt/conhecimento/eventos/I-Congresso-de-Direito-das-Infraestruturas-Digitais-Regulacao-e-Poder/34662/>) | PLMJ |
| O programa indica 21 de abril; o ano de 2026 consta da listagem oficial do evento\. | Conferência sobre os desafios estratégicos e regulatórios da cibersegurança no setor industrial português, com destaque para a Diretiva NIS2\. | 2026\-04\-21 | 2026\-04\-21 | O Futuro da Cibersegurança no Setor Industrial | 9h30 – 13h | [https://abreuadvogados\.com/conhecimento/eventos/abreu/o\-futuro\-da\-ciberseguranca\-no\-setor\-industrial/](<https://abreuadvogados.com/conhecimento/eventos/abreu/o-futuro-da-ciberseguranca-no-setor-industrial/>) | Abreu Advogados |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| date\_note | text |
| description | text |
| end\_date | text |
| event\_date | text |
| event\_name | text |
| event\_time | text |
| event\_url | text |
| firm | text |
| format | text |
| last\_checked | text |
| legal\_evidence | text |
| listing\_url | text |
| location | text |
| organizer | text |
| organizer\_evidence | text |
| portugal\_evidence | text |
| publication\_date | text |
| registration\_url | text |
| timezone | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["event#95;pages"]
  n1["previous#95;events"]
  n2["historical#95;events"]
  n3["sources"]
  n4["discover"]
  n5["pages#95;ready"]
  n6["details"]
  n7["normalize"]
  n8["events"]
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n6 --> n7
  n7 --> n8
  n0 --> n3
  n1 --> n3
  n2 --> n3
  n0 --> n5
  n2 --> n5
  n1 --> n5
```

- **event\_pages**: Optional reusable discovered event\-page inventory\. Leave unbound to discover fresh listings\.
- **previous\_events**: Previously saved events to recheck against the current inclusion criteria\.
- **historical\_events**: Earlier published discoveries retained for requalification after a filtering correction\.
- **sources**: Choose the seven official event feeds and news sections that publish event announcements\.
- **discover**: Read the latest listing pages from each firm, following observed pagination and collecting official detail links\.
- **pages\_ready**: Combine discovered links, remove duplicate URLs and interleave firms for balanced bounded runs\.
- **details**: Read each official announcement, distinguish real events from general news, and extract event dates, venue and registration information\.
- **normalize**: Keep one event per official URL with consistent columns and preserve unknown event dates explicitly\.
- **events**: Portugal\-relevant events organized or co\-organized by the seven requested law firms, with source evidence\.

## Version history

- 2026-11-04T16:45:32.694375Z: v1: Creates a unified collection of published events from the seven law firms, with source links, dates, venues and registration details when available\.
- 2026-11-04T16:56:08.487940Z: v2: Prevents approximate or month\-only event dates from being presented as exact dates\.
- 2026-11-05T09:04:51.136151Z: v3: Recover a missing event title from the announcement headline when the official listing confirms it\.
- 2026-11-12T15:49:50.707785Z: v4: Limit results to Portugal\-relevant legal events organized or co\-organized by the firms\. Remove cultural events and external speaking appearances from earlier saved results, with source excerpts supporting inclusion\.
- 2026-11-12T16:03:16.761265Z: v5: Correct organizing\-role checks so genuine co\-organized legal events are retained and welcome remarks or venue provision alone do not qualify\. Recheck earlier discoveries affected by the filter\.

## Recorded repairs

- 2026-11-05T09:02:34.293772Z: no change
- 2026-11-05T09:03:15.890052Z: no change
- 2026-11-05T09:05:05.108476Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/law-firm-events-4c408bd04e11?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
