# Law Firm Events

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Event records associated with Abreu Advogados, PLMJ, VdA, Morais Leitão, Cuatrecasas, Garrigues and Uría Menéndez, with event details and source links\. The published dataset contains 20 event records\.

[Get the full dataset for free](https://www.jsonify.com/datasets/law-firm-events-4c408bd04e11?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 5
- Last published: 2026-11-23T09:20:17.005788Z

## The brief

> I need this data: Event records associated with Abreu Advogados, PLMJ, VdA, Morais Leitão, Cuatrecasas, Garrigues and Uría Menéndez, with event details and source links\. The published dataset contains 20 event records\.

Summary from the public dataset description.

## Law firm events / events

20 total rows · 10 sampled · Output revision 15
Published: 2026-11-23T09:20:17.005788Z · Producing pipeline version: 5

[CSV sample](outputs/b08d9aab8e59/events-862417b9e7c3/sample.csv) · [JSON sample](outputs/b08d9aab8e59/events-862417b9e7c3/sample.json) · [Schema](outputs/b08d9aab8e59/events-862417b9e7c3/schema.json)

| date\_note | description | end\_date | event\_date | event\_name | event\_time | event\_url | firm |
| --- | --- | --- | --- | --- | --- | --- | --- |
| O programa indica 21 de abril e a listagem oficial confirma o ano de 2026\. | Conferência sobre cibersegurança no setor industrial português, com foco nas obrigações da Diretiva NIS2 em matéria de gestão de risco, reporte de incidentes e responsabilização dos órgãos de gestão\. | 2026\-04\-21 | 2026\-04\-21 | O Futuro da Cibersegurança no Setor Industrial | 9h30 – 13h | [https://abreuadvogados\.com/conhecimento/eventos/abreu/o\-futuro\-da\-ciberseguranca\-no\-setor\-industrial/](<https://abreuadvogados.com/conhecimento/eventos/abreu/o-futuro-da-ciberseguranca-no-setor-industrial/>) | Abreu Advogados |
| A listagem oficial indica o início em 27 de outubro de 2026 às 09:00\. O anúncio refere dois dias de congresso, sem indicar a data de encerramento\. | Congresso de dois dias que reúne académicos, reguladores e profissionais da indústria para debater a regulação das infraestruturas digitais, dos cabos submarinos e centros de dados à identidade digital e à inteligência artificial\. | None | 2026\-10\-27 | I Congresso de Direito das Infraestruturas Digitais: Regulação e Poder | 09:00 | [https://www\.plmj\.com/pt/conhecimento/eventos/I\-Congresso\-de\-Direito\-das\-Infraestruturas\-Digitais\-Regulacao\-e\-Poder/34662/](<https://www.plmj.com/pt/conhecimento/eventos/I-Congresso-de-Direito-das-Infraestruturas-Digitais-Regulacao-e-Poder/34662/>) | PLMJ |
| O anúncio, publicado em 5 de junho de 2025, indica que a cerimónia se realizou «ontem» e descreve a abertura e o encerramento na mesma jornada\. | Cerimónia comemorativa da assinatura do Tratado de Adesão de Espanha e Portugal às Comunidades Europeias, com uma conversa sobre a integração europeia dos dois países e um colóquio sobre o impacto do Direito da União nos sistemas jurídicos nacionais\. | 2025\-06\-04 | 2025\-06\-04 | A Uría Menéndez assinala o 40\.º aniversário da assinatura do Tratado de Adesão de Espanha e Portugal à União Europeia | None | [https://www\.uria\.com/pt/prensa/1403\-uria\-menendez\-conmemora\-el\-40\-aniversario\-de\-la\-firma\-del\-tratado\-de\-adhesion\-de\-espana\-y\-portugal\-a\-la\-union\-europea](<https://www.uria.com/pt/prensa/1403-uria-menendez-conmemora-el-40-aniversario-de-la-firma-del-tratado-de-adhesion-de-espana-y-portugal-a-la-union-europea>) | Uría Menéndez |
| O ano de 2026 consta da listagem oficial\. O horário explícito é 14h30 – 16h30, apesar da referência a «Ao longo da manhã» no texto\. | Conferência sobre as prioridades do PTRR, os instrumentos de financiamento, os desafios jurídicos na execução de projetos e a mitigação de riscos\. | 2026\-05\-18 | 2026\-05\-18 | PTRR: Um novo ciclo de investimento | 14h30 – 16h30 | [https://abreuadvogados\.com/conhecimento/eventos/abreu/ptrr\-um\-novo\-ciclo\-de\-investimento/](<https://abreuadvogados.com/conhecimento/eventos/abreu/ptrr-um-novo-ciclo-de-investimento/>) | Abreu Advogados |
| None | Lançamento de um manual de advocacia de empresa, com um painel de debate\. O livro reúne 15 artigos sobre temas como governança corporativa, inteligência artificial no trabalho jurídico, regulação e compliance\. | 2026\-11\-26 | 2026\-11\-26 | Lançamento do livro “Manual do Advogado In\-House” | 16h45 – 18h45 | [https://abreuadvogados\.com/conhecimento/eventos/abreu/lancamento\-do\-livro\-manual\-do\-advogado\-in\-house/](<https://abreuadvogados.com/conhecimento/eventos/abreu/lancamento-do-livro-manual-do-advogado-in-house/>) | Abreu Advogados |

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
