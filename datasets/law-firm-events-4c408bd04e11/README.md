# Law Firm Events

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Event records associated with Abreu Advogados, PLMJ, VdA, Morais Leitão, Cuatrecasas, Garrigues and Uría Menéndez, with event details and source links\.

[Get the full dataset for free](https://www.jsonify.com/datasets/law-firm-events-4c408bd04e11?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 5
- Last published: 2026-11-27T09:11:14.638325Z

## The brief

> I need this data: Event records associated with Abreu Advogados, PLMJ, VdA, Morais Leitão, Cuatrecasas, Garrigues and Uría Menéndez, with event details and source links\.

Summary from the public dataset description.

## Law firm events / events

21 total rows · 10 sampled · Output revision 19
Published: 2026-11-27T09:11:14.638325Z · Producing pipeline version: 5

[CSV sample](outputs/b08d9aab8e59/events-862417b9e7c3/sample.csv) · [JSON sample](outputs/b08d9aab8e59/events-862417b9e7c3/sample.json) · [Schema](outputs/b08d9aab8e59/events-862417b9e7c3/schema.json)

| date\_note | description | end\_date | event\_date | event\_name | event\_time | event\_url | firm |
| --- | --- | --- | --- | --- | --- | --- | --- |
| O programa indica 18 de maio; o ano de 2026 consta da data na listagem oficial\. | Conferência sobre as prioridades estratégicas do PTRR, os instrumentos de financiamento, os desafios jurídicos na execução de projetos e a mitigação dos riscos de implementação\. | 2026\-05\-18 | 2026\-05\-18 | PTRR: Um novo ciclo de investimento | 14h30 – 16h30 | [https://abreuadvogados\.com/conhecimento/eventos/abreu/ptrr\-um\-novo\-ciclo\-de\-investimento/](<https://abreuadvogados.com/conhecimento/eventos/abreu/ptrr-um-novo-ciclo-de-investimento/>) | Abreu Advogados |
| None | Sessão com mesa\-redonda sobre o impacto da revisão da Diretiva\-Quadro dos Resíduos e do Regulamento de Ecodesign para Produtos Sustentáveis no setor têxtil português\. | None | 2026\-11\-20 | Business Breakfast \| Sustentabilidade e Regulação no Setor Têxtil | 09:00 | [https://www\.plmj\.com/pt/conhecimento/eventos/Business\-Breakfast\-Sustentabilidade\-e\-Regulacao\-no\-Setor\-Textil/34719/](<https://www.plmj.com/pt/conhecimento/eventos/Business-Breakfast-Sustentabilidade-e-Regulacao-no-Setor-Textil/34719/>) | PLMJ |
| None | Conferência sobre os desafios da transparência salarial e da diversidade para as equipas de recursos humanos, à luz das alterações ao Código do Trabalho\. | None | 2025\-10\-02 | Transparência salarial e diversidade: novos desafios RH | 09:30 | [https://www\.plmj\.com/pt/conhecimento/eventos/Transparencia\-salarial\-e\-diversidade\-novos\-desafios\-RH/34022/](<https://www.plmj.com/pt/conhecimento/eventos/Transparencia-salarial-e-diversidade-novos-desafios-RH/34022/>) | PLMJ |
| O anúncio indica 25 de novembro e descreve um programa de um dia\. O ano de 2026 resulta da data de publicação\. | Conferência que assinala os 60 anos do Código Civil Português, com debates sobre direito dos contratos, reformas do direito civil noutros países, responsabilidade civil, prova e uma possível revisão do Código Civil\. | 2026\-11\-25 | 2026\-11\-25 | Conferência “Ler os Sinais do Tempo: do Mundo para o Direito” | None | [https://www\.mlgts\.pt/pt/conhecimento/noticias/Conferencia\-Ler\-os\-Sinais\-do\-Tempo\-do\-Mundo\-para\-o\-Direito/27186/](<https://www.mlgts.pt/pt/conhecimento/noticias/Conferencia-Ler-os-Sinais-do-Tempo-do-Mundo-para-o-Direito/27186/>) | Morais Leitão |
| None | Evento sobre soberania digital, inteligência artificial e infraestruturas financeiras, com uma sessão dedicada à tributação e à regulação dos criptoativos e das tecnologias de registo distribuído em Portugal\. | 2026\-05\-26 | 2026\-05\-26 | Digital Self\-Sovereign State of Portugal | 16:00–19:30 | [https://abreuadvogados\.com/conhecimento/eventos/abreu/digital\-self\-sovereign\-state\-of\-portugal/](<https://abreuadvogados.com/conhecimento/eventos/abreu/digital-self-sovereign-state-of-portugal/>) | Abreu Advogados |

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
