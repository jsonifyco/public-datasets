# Yacht Charter Fleet Listings and Prices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Yacht charter fleet sample with listing details and dated weekly search prices for Croatia, Greece and the Balearics\.

[Get the full dataset for free](https://www.jsonify.com/datasets/yacht-charter-fleet-sample-55a14b2e14c3?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 2
- Last published: 2026-11-10T11:15:01.714669Z

## The brief

> I need this data: Yacht charter fleet sample with listing details and dated weekly search prices for Croatia, Greece and the Balearics\.

Summary from the public dataset description.

## Yacht charter fleet sample / yachts

270 total rows · 50 sampled · Output revision 1
Published: 2026-11-10T11:15:01.714669Z · Producing pipeline version: 2

[CSV sample](outputs/c1ae98410c29/yachts-f81c639720fe/sample.csv) · [JSON sample](outputs/c1ae98410c29/yachts-f81c639720fe/sample.json) · [Schema](outputs/c1ae98410c29/yachts-f81c639720fe/schema.json)

| area | base\_marina | cabins | captured\_date | charter\_company | check\_in | check\_out | city |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Greece | Lefkas Marina | 6 | 2026\-11\-10 | AF Yachting | 2027\-07\-10 | 2027\-07\-17 | Lefkada town |
| Greece | Lefkas Marina | 3 | 2026\-11\-10 | AF Yachting | 2027\-07\-10 | 2027\-07\-17 | Lefkada town |
| Greece | Olympic Marina | 5 | 2026\-11\-10 | Hellenic Yachting | 2027\-07\-10 | 2027\-07\-17 | Lávrion |
| Balearics | Marina Naviera Balear | 3 | 2026\-11\-10 | First Class Sailing Spain | 2027\-07\-10 | 2027\-07\-17 | Palma de Mallorca |
| Greece | Lefkas Marina | 6 | 2026\-11\-10 | AF Yachting | 2027\-07\-10 | 2027\-07\-17 | Lefkada town |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| area | text |
| base\_marina | text |
| cabins | integer |
| captured\_date | text |
| charter\_company | text |
| check\_in | text |
| check\_out | text |
| city | text |
| country | text |
| island\_or\_region | text |
| length\_m | double precision |
| marketplace | text |
| price\_notes | text |
| source\_price\_basis | text |
| source\_yacht\_type | text |
| url | text |
| vat\_excluded | boolean |
| weekly\_price\_high\_season\_eur | text |
| weekly\_price\_low\_season\_eur | text |
| weekly\_search\_price\_eur | text |
| yacht\_model | text |
| yacht\_name | text |
| yacht\_type | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["plan"]
  n1["collect"]
  n2["validate"]
  n3["yachts"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **plan**: Select the same Croatia, Greece, Mallorca and Ibiza searches used for the sample\.
- **collect**: Open a fresh public marketplace search and read its bounded result pages with current rental prices\.
- **validate**: Check distinct listings and preserve the sample's fields and pricing caveats before saving\.
- **yachts**: Public yacht charter fleet sample and dated rental search prices\.

## Version history

- 2026-11-10T11:11:27.642465Z: v1: Added a saved collector for the yacht charter sample with the same fields and dated rental prices\.
- 2026-11-10T11:14:15.921577Z: v2: Improved access to later result pages so the full one\-off sample can be saved\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/yacht-charter-fleet-sample-55a14b2e14c3?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
