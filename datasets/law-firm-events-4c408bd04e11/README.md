# Law Firm Events

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Event records associated with Abreu Advogados, PLMJ, VdA, Morais Leitão, Cuatrecasas, Garrigues and Uría Menéndez, with event details and source links\.

[Get the full dataset for free](https://www.jsonify.com/datasets/law-firm-events-4c408bd04e11?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 5
- Last published: 2026-11-26T09:11:31.346723Z

## The brief

> I need this data: Event records associated with Abreu Advogados, PLMJ, VdA, Morais Leitão, Cuatrecasas, Garrigues and Uría Menéndez, with event details and source links\.

Summary from the public dataset description.

## Law firm events / events

22 total rows · 10 sampled · Output revision 18
Published: 2026-11-26T09:11:31.346723Z · Producing pipeline version: 5

[CSV sample](outputs/b08d9aab8e59/events-862417b9e7c3/sample.csv) · [JSON sample](outputs/b08d9aab8e59/events-862417b9e7c3/sample.json) · [Schema](outputs/b08d9aab8e59/events-862417b9e7c3/schema.json)

| date\_note | description | end\_date | event\_date | event\_name | event\_time | event\_url | firm |
| --- | --- | --- | --- | --- | --- | --- | --- |
| O programa indica 21 de abril; a data de 21\.04\.2026 na ficha oficial do evento confirma o ano\. | Conferência sobre cibersegurança no setor industrial português, com enfoque nas obrigações da Diretiva NIS2 relativas à gestão de risco, ao reporte de incidentes e à responsabilidade dos órgãos de gestão\. | 2026\-04\-21 | 2026\-04\-21 | O Futuro da Cibersegurança no Setor Industrial | 9h30 – 13h | [https://abreuadvogados\.com/conhecimento/eventos/abreu/o\-futuro\-da\-ciberseguranca\-no\-setor\-industrial/](<https://abreuadvogados.com/conhecimento/eventos/abreu/o-futuro-da-ciberseguranca-no-setor-industrial/>) | Abreu Advogados |
| None | Terceira sessão do ciclo sobre privacidade no trabalho, dedicada aos limites do acesso do empregador ao conteúdo dos dispositivos empresariais em investigações internas e à proteção da privacidade dos trabalhadores\. | 2026\-11\-26 | 2026\-11\-26 | Entre a Investigação e a Privacidade: o acesso ao conteúdo dos dispositivos empresariais | 9:00 – 10:30 | [https://www\.cuatrecasas\.com/pt/global/events/investigacao\-privacidade\-acesso\-ao\-conteudo\-dispositivos\-empresariais](<https://www.cuatrecasas.com/pt/global/events/investigacao-privacidade-acesso-ao-conteudo-dispositivos-empresariais>) | Cuatrecasas |
| The session is scheduled for 26 November; the publication date establishes the year as 2026\. | An online session in the Fundações 360º Programme examining recent changes to the tax framework for patronage and practical tax issues for foundations and their supporters\. | 2026\-11\-26 | 2026\-11\-26 | Tax Framework for the Foundation Sector | 3:00 pm to 4:00 pm | [https://www\.vda\.pt/en/media/events/vda\-participates\-in\-the\-foundation\-capacity\-building\-sessions/28967/](<https://www.vda.pt/en/media/events/vda-participates-in-the-foundation-capacity-building-sessions/28967/>) | VdA |
| The announcement is dated November 26, 2026, but does not state when the session took place\. | VdA hosted a panel and roundtable in Porto on amendments to the Legal Framework for Urban Development and Construction \(RJUE\) and their impact on urban development and real estate\. | None | None | VdA hosts session in Porto on amendments to the RJUE | None | [https://www\.vda\.pt/en/media/events/vda\-hosts\-session\-in\-porto\-on\-amendments\-to\-the\-rjue/28966/](<https://www.vda.pt/en/media/events/vda-hosts-session-in-porto-on-amendments-to-the-rjue/28966/>) | VdA |
| None | Sessão com mesa\-redonda sobre o impacto da revisão da Diretiva\-Quadro dos Resíduos e do Regulamento de Ecodesign para Produtos Sustentáveis no setor têxtil português\. | None | 2026\-11\-20 | Business Breakfast \| Sustentabilidade e Regulação no Setor Têxtil | 09:00 | [https://www\.plmj\.com/pt/conhecimento/eventos/Business\-Breakfast\-Sustentabilidade\-e\-Regulacao\-no\-Setor\-Textil/34719/](<https://www.plmj.com/pt/conhecimento/eventos/Business-Breakfast-Sustentabilidade-e-Regulacao-no-Setor-Textil/34719/>) | PLMJ |

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
