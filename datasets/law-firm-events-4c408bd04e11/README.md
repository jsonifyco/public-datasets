# Law Firm Events

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Event records associated with Abreu Advogados, PLMJ, VdA, Morais Leitão, Cuatrecasas, Garrigues and Uría Menéndez, with event details and source links\. The published dataset contains 19 event records\.

[Get the full dataset for free](https://www.jsonify.com/datasets/law-firm-events-4c408bd04e11?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 5
- Last published: 2026-11-19T09:06:52.406893Z

## The brief

> I need this data: Event records associated with Abreu Advogados, PLMJ, VdA, Morais Leitão, Cuatrecasas, Garrigues and Uría Menéndez, with event details and source links\. The published dataset contains 19 event records\.

Summary from the public dataset description.

## Law firm events / events

19 total rows · 10 sampled · Output revision 13
Published: 2026-11-19T09:06:52.406893Z · Producing pipeline version: 5

[CSV sample](outputs/b08d9aab8e59/events-862417b9e7c3/sample.csv) · [JSON sample](outputs/b08d9aab8e59/events-862417b9e7c3/sample.json) · [Schema](outputs/b08d9aab8e59/events-862417b9e7c3/schema.json)

| date\_note | description | end\_date | event\_date | event\_name | event\_time | event\_url | firm |
| --- | --- | --- | --- | --- | --- | --- | --- |
| O programa indica 15 a 24 de abril; o ano de 2026 é confirmado pela data da listagem oficial\. | Curso de 19 horas sobre o papel estratégico do advogado in\-house, incluindo compliance, M&amp;A, ESG, tecnologia e resolução de litígios\. As aulas são online, com uma última sessão presencial para entrega de certificados\. | 2026\-04\-24 | 2026\-04\-15 | 5\.ª edição Curso In\-House: Advocacia de empresa para o futuro \| Instituto de Conhecimento &amp; Future Law | 15h – 18h | [https://abreuadvogados\.com/conhecimento/eventos/abreu/5\-a\-edicao\-curso\-in\-house\-advocacia\-de\-empresa\-para\-o\-futuro\-instituto\-de\-conhecimento\-future\-law/](<https://abreuadvogados.com/conhecimento/eventos/abreu/5-a-edicao-curso-in-house-advocacia-de-empresa-para-o-futuro-instituto-de-conhecimento-future-law/>) | Abreu Advogados |
| O anúncio indica 02 de outubro sem ano\. O ano não pode ser confirmado apenas pelo nome do ficheiro do programa\. | Conferência da PLMJ sobre transparência salarial, diversidade e desafios para as áreas de Recursos Humanos à luz das alterações ao Código do Trabalho\. | None | None | Transparência salarial e diversidade: novos desafios RH | 09h30 | [https://www\.plmj\.com/pt/conhecimento/eventos/Transparencia\-salarial\-e\-diversidade\-novos\-desafios\-RH/34022/](<https://www.plmj.com/pt/conhecimento/eventos/Transparencia-salarial-e-diversidade-novos-desafios-RH/34022/>) | PLMJ |
| The announcement gives 26 May without a year; the dated official listing establishes 2026\. | An event in Lisbon on digital sovereignty, financial infrastructure and distributed governance, including a session on the taxation and regulation of cryptoassets in Portugal\. | 2026\-05\-26 | 2026\-05\-26 | Digital Self\-Sovereign State of Portugal | 16h00–19h30 | [https://abreuadvogados\.com/conhecimento/eventos/abreu/digital\-self\-sovereign\-state\-of\-portugal/](<https://abreuadvogados.com/conhecimento/eventos/abreu/digital-self-sovereign-state-of-portugal/>) | Abreu Advogados |
| None | Encontro sobre os desafios e oportunidades do Open Insurance para o setor segurador português e europeu, incluindo proteção do consumidor e o impacto do quadro regulatório FIDA\. | 2026\-07\-03 | 2026\-07\-03 | Open Insurance, Primado do Cliente: Oportunidades, Desafios e Testemunhos Internacionais | 09h15–12h45 | [https://abreuadvogados\.com/conhecimento/eventos/abreu/open\-insurance\-primado\-do\-cliente\-oportunidades\-desafios\-e\-testemunhos\-internacionai/](<https://abreuadvogados.com/conhecimento/eventos/abreu/open-insurance-primado-do-cliente-oportunidades-desafios-e-testemunhos-internacionai/>) | Abreu Advogados |
| O ano de 2026 é determinado pela data de publicação de 22\.10\.2026; o anúncio indica 29 de outubro para a sessão\. | Apresentação da obra de Isabel Valente Dias sobre a retribuição no ordenamento juslaboral português, seguida de uma mesa\-redonda sobre temas centrais do livro\. | None | 2026\-10\-29 | Apresentação da obra "A Retribuição no Ordenamento Juslaboral Português" | 17h30 | [https://www\.mlgts\.pt/pt/conhecimento/noticias/Apresentacao\-da\-obra\-A\-Retribuicao\-no\-Ordenamento\-Juslaboral\-Portugues/27178/](<https://www.mlgts.pt/pt/conhecimento/noticias/Apresentacao-da-obra-A-Retribuicao-no-Ordenamento-Juslaboral-Portugues/27178/>) | Morais Leitão |

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
