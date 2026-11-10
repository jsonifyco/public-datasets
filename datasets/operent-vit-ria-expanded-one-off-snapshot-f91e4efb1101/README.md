# Vitória Airbnb and Booking\.com Nightly Rates

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Candidate apartment listings in Vitória from Airbnb and Booking\.com, with nightly quotes, availability, listing details and source\-reported ratings\. The published tables contain 2,790 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/operent-vit-ria-expanded-one-off-snapshot-f91e4efb1101?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 5
- Last published: 2026-11-09T21:12:18.908121Z

## The brief

> I need this data: Candidate apartment listings in Vitória from Airbnb and Booking\.com, with nightly quotes, availability, listing details and source\-reported ratings\. The published tables contain 2,790 rows\.

Summary from the public dataset description.

## Vitória expanded one\-off nightly snapshot / nightly\_rates

2,790 total rows · 50 sampled · Output revision 2
Published: 2026-11-09T21:12:18.908121Z · Producing pipeline version: 5

[CSV sample](outputs/98daa1ec20b8/nightly-rates-115ea5b7fd74/sample.csv) · [JSON sample](outputs/98daa1ec20b8/nightly-rates-115ea5b7fd74/sample.json) · [Schema](outputs/98daa1ec20b8/nightly-rates-115ea5b7fd74/schema.json)

| available | bedrooms | collected\_at | currency | date | listing\_id | listing\_url | max\_guests |
| --- | --- | --- | --- | --- | --- | --- | --- |
| True | 2 | 2026\-11\-09T20:57:28\.828480\+00:00 | BRL | 2026\-12\-05 | 575338422308214664 | [https://www\.airbnb\.com/rooms/575338422308214664](<https://www.airbnb.com/rooms/575338422308214664>) | 4 |
| False | 1 | 2026\-11\-09T20:26:18\.472317\+00:00 | BRL | 2026\-11\-20 | 1003570746183939076 | [https://www\.airbnb\.com/rooms/1003570746183939076](<https://www.airbnb.com/rooms/1003570746183939076>) | 3 |
| False | 1 | 2026\-11\-09T20:53:41\.409697\+00:00 | BRL | 2026\-12\-04 | 1605343771835530637 | [https://www\.airbnb\.com/rooms/1605343771835530637](<https://www.airbnb.com/rooms/1605343771835530637>) | 4 |
| False | 1 | 2026\-11\-09T18:03:39\.846568\+00:00 | BRL | 2026\-11\-15 | 1303003515196813014 | [https://www\.airbnb\.com/rooms/1303003515196813014](<https://www.airbnb.com/rooms/1303003515196813014>) | 2 |
| False | 1 | 2026\-11\-09T20:27:53\.986774\+00:00 | BRL | 2026\-11\-21 | 1699204827655414943 | [https://www\.airbnb\.com/rooms/1699204827655414943](<https://www.airbnb.com/rooms/1699204827655414943>) | 3 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| available | boolean |
| bedrooms | integer |
| collected\_at | text |
| currency | text |
| date | text |
| listing\_id | text |
| listing\_url | text |
| max\_guests | integer |
| min\_nights | integer |
| neighbourhood | text |
| nightly\_price | double precision |
| property\_type | text |
| rating | double precision |
| review\_count | integer |
| source | text |
| title | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["properties"]
  n1["panel"]
  n2["metadata"]
  n3["stay#95;nights"]
  n4["nightly#95;quotes"]
  n5["verify#95;coverage"]
  n6["nightly#95;rates"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n0 --> n1
  n0 --> n1
  n0 --> n5
```

- **properties**: Expanded one\-off panel of Airbnb and Booking\.com apartments in Vitória\. Both platforms remain separate listings\.
- **panel**: Load the fixed Vitória property panel and set the next consecutive stay nights using local time\.
- **metadata**: Read Airbnb whole\-home metadata and its calendar\. Retain the Booking\.com property links for exact dated apartment checks\.
- **stay\_nights**: Create one exact one\-night, two\-adult check per property for every requested stay night\.
- **nightly\_quotes**: Check each exact overnight stay for two adults in BRL\. Require a source offer or an explicit unavailable response, never infer sold out from absence\.
- **verify\_coverage**: Require all property\-night checks, both platforms, unique listing\-night records and valid source\-confirmed prices before replacing saved results\.
- **nightly\_rates**: One\-off expanded snapshot of source\-displayed one\-night apartment quotes in BRL for two adults\. Includes cleaning fees where included in the offer; additional excluded taxes are not added\. Airbnb ratings are out of 5, Booking\.com ratings out of 10\. False means no offer for the exact one\-night search, not proof of occupancy\. Minimum stay restrictions can make a night unavailable\. Unknown or blocked checks fail without replacing saved data\.

## Version history

- 2026-11-09T12:58:00.524776Z: v1: Added a separate expanded one\-off Vitória apartment snapshot for the Web Summit meeting, without changing the daily sample\.
- 2026-11-09T12:59:23.969734Z: v2: Corrected source\-based neighbourhood matching in the expanded one\-off snapshot\.
- 2026-11-09T13:56:40.417884Z: v3: Fixed recognition of Booking\.com’s compact price display so the one\-off snapshot can continue without repeating completed checks\.
- 2026-11-09T14:16:08.412605Z: v4: Added a fresh\-page retry when Booking\.com ignores the requested currency or stay dates\.
- 2026-11-09T18:47:14.047025Z: v5: Waits for Booking\.com room details to finish loading and retries incomplete apartment confirmation without weakening source checks\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/operent-vit-ria-expanded-one-off-snapshot-f91e4efb1101?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
