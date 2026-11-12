# Iberian Endurance Events

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Iberian endurance events in Portugal and Spain, with event dates, locations, distances, entry prices and source details\.

[Get the full dataset for free](https://www.jsonify.com/datasets/aurea77-iberian-endurance-events-15c76f799e90?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 2
- Last published: 2026-11-11T20:40:20.829684Z

## The brief

> I need this data: Iberian endurance events in Portugal and Spain, with event dates, locations, distances, entry prices and source details\.

Summary from the public dataset description.

## Aurea77 endurance events / events

394 total rows · 50 sampled · Output revision 1
Published: 2026-11-11T20:40:20.829684Z · Producing pipeline version: 2

[CSV sample](outputs/ce3fa5a87445/events-862417b9e7c3/sample.csv) · [JSON sample](outputs/ce3fa5a87445/events-862417b9e7c3/sample.json) · [Schema](outputs/ce3fa5a87445/events-862417b9e7c3/schema.json)

| city | country | currency | distances | entry\_price | event\_name | organiser | region |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Vila Nova de Cerveira | Portugal | EUR | \["25 km", "45 km"\] | 10 € | MTB – "ROTA DA GÁVEA" | None | Viana do Castelo |
| Plano de la Feria | Spain | EUR | \["14 km", "23 km"\] | 19\.0–23\.0 | Epora Trail | Club Mar Alegre y la Compañía de Romanos SPQR de Montoro | Córdoba |
| León | Spain | EUR | \["7 km"\] | 13\.0 | San Silvestre Popular Ciudad de Leon | Concejalía de Deportes del Ayuntamiento de León, Delegación Leonesa de Atletismo y Sprint Atletismo León | León |
| Figueira da Foz | Portugal | None | \["10 km"\] | None | Campeonatos Nacionais de 10km em Estrada \(Sub\-20, Absolutos e Veteranos\) | None | None |
| Via de l'Imperi Romà | Spain | EUR | \["5 km", "10 km"\] | 12\.0–16\.0 | Tarraco Health Race | Col·legi Oficial de Metges de Tarragona | Tarragona |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| city | text |
| country | text |
| currency | text |
| distances | jsonb |
| entry\_price | text |
| event\_name | text |
| organiser | text |
| region | text |
| registration\_url | text |
| scraped\_at | text |
| source\_name | text |
| source\_url | text |
| sources | jsonb |
| sport | text |
| start\_date | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["plan"]
  n1["discover#95;pages"]
  n2["balance#95;pages"]
  n3["read#95;pages"]
  n4["balance#95;details"]
  n5["event#95;details"]
  n6["deduplicate"]
  n7["events"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n6 --> n7
```

- **plan**: Select public federation calendars and race listings for the requested three\-month sample\.
- **discover\_pages**: Read each public calendar and expand only its relevant month pages\.
- **balance\_pages**: Keep federation and listing sources represented while avoiding duplicate calendar pages\.
- **read\_pages**: Read event cards and official calendar entries, rejecting unconfirmed dates and unrelated disciplines\.
- **balance\_details**: Deduplicate event\-page requests and balance the sample across countries and sources\.
- **event\_details**: Read each event’s public details for dates, distances, location, organiser and displayed entry fees\.
- **deduplicate**: Merge matching event names, dates and cities while retaining every source occurrence and calculating sample quality\.
- **events**: Upcoming endurance events with all contributing source observations\.

## Version history

- 2026-11-11T20:20:37.406454Z: v1: Created the private Iberian endurance event collector with public federation and race\-listing sources, cross\-source deduplication and a coverage report\.
- 2026-11-11T20:25:39.472753Z: v2: Repairs the Spanish athletics calendar read so pages without the event list are retried through supported public access methods\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/aurea77-iberian-endurance-events-15c76f799e90?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
