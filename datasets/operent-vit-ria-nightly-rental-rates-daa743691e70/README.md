# Vitória Short\-Term Rental Rates

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Vitória rental listings with displayed nightly quotes and availability for specific stay dates\. The published dataset contains 960 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/operent-vit-ria-nightly-rental-rates-daa743691e70?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 10
- Last published: 2026-11-09T10:37:15.874612Z

## The brief

> I need this data: Vitória rental listings with displayed nightly quotes and availability for specific stay dates\. The published dataset contains 960 rows\.

Summary from the public dataset description.

## Vitória nightly rental rates / nightly\_rates

960 total rows · 50 sampled · Output revision 4
Published: 2026-11-09T10:37:15.874612Z · Producing pipeline version: 10

[CSV sample](outputs/de4b65c24d43/nightly-rates-115ea5b7fd74/sample.csv) · [JSON sample](outputs/de4b65c24d43/nightly-rates-115ea5b7fd74/sample.json) · [Schema](outputs/de4b65c24d43/nightly-rates-115ea5b7fd74/schema.json)

| available | bedrooms | collected\_at | currency | date | listing\_id | listing\_url | max\_guests |
| --- | --- | --- | --- | --- | --- | --- | --- |
| False | 1 | 2026\-11\-09T09:22:18\.056810\+00:00 | BRL | 2026\-11\-10 | 53531609 | [https://www\.airbnb\.com/rooms/53531609](<https://www.airbnb.com/rooms/53531609>) | 2 |
| False | 1 | 2026\-11\-09T10:19:15\.711621\+00:00 | BRL | 2026\-12\-02 | 15035911 | [https://www\.booking\.com/hotel/br/flat\-praia\-comfort\-camburi\.html](<https://www.booking.com/hotel/br/flat-praia-comfort-camburi.html>) | 4 |
| False | 1 | 2026\-11\-09T09:32:51\.082204\+00:00 | BRL | 2026\-11\-14 | 1694320411842196266 | [https://www\.airbnb\.com/rooms/1694320411842196266](<https://www.airbnb.com/rooms/1694320411842196266>) | 4 |
| False | 1 | 2026\-11\-09T10:01:29\.312448\+00:00 | BRL | 2026\-11\-23 | 1216800404584520733 | [https://www\.airbnb\.com/rooms/1216800404584520733](<https://www.airbnb.com/rooms/1216800404584520733>) | 2 |
| False | 1 | 2026\-11\-09T09:34:48\.613465\+00:00 | BRL | 2026\-11\-15 | 1728577633890495345 | [https://www\.airbnb\.com/rooms/1728577633890495345](<https://www.airbnb.com/rooms/1728577633890495345>) | 4 |

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

- **properties**: The fixed sample panel of Airbnb and Booking\.com apartments and entire homes in Vitória\. Both sources are retained independently\.
- **panel**: Load the fixed Vitória property panel and set the next consecutive stay nights using local time\.
- **metadata**: Read Airbnb whole\-home metadata and its calendar\. Retain the Booking\.com property links for exact dated apartment checks\.
- **stay\_nights**: Create one exact one\-night, two\-adult check per property for every requested stay night\.
- **nightly\_quotes**: Check each exact overnight stay for two adults in BRL\. Require a source offer or an explicit unavailable response, never infer sold out from absence\.
- **verify\_coverage**: Require all property\-night checks, both platforms, unique listing\-night records and valid source\-confirmed prices before replacing saved results\.
- **nightly\_rates**: Latest daily snapshot of source\-displayed one\-night apartment quotes in BRL for two adults\. Includes cleaning fees where included in the offer; additional excluded taxes are not added\. Airbnb ratings are out of 5, Booking\.com ratings out of 10\. False means no offer for the exact one\-night search, not proof of occupancy\. Minimum stay restrictions can make a night unavailable\. Unknown or blocked checks fail without replacing saved data\.

## Version history

- 2026-11-06T18:57:51.580757Z: v1: Adds the daily Vitória sample of Airbnb and Booking\.com apartments and whole homes, with nightly BRL rates and availability for one\-night stays by two adults across the next thirty days\.
- 2026-11-06T19:48:34.003663Z: v2: Fixed discounted Airbnb offers so their current BRL totals can be collected alongside regular prices\.
- 2026-11-06T20:02:24.530196Z: v3: Added one retry for temporary Booking\.com page\-loading failures while preserving complete daily coverage\.
- 2026-11-06T20:36:25.938903Z: v4: Improved recovery from incomplete Booking\.com availability pages without treating unresolved checks as unavailable\.
- 2026-11-06T20:51:13.837996Z: v5: Improved the alternative page read for Booking\.com stays whose rendered availability is incomplete\.
- 2026-11-06T21:48:00.980405Z: v6: Recognizes an additional Booking\.com offer format when the listing explicitly confirms two adults\.
- 2026-11-06T22:27:51.478293Z: v7: Fixed the final completeness check so interrupted collections can save their verified results after recovery\.
- 2026-11-08T09:37:47.987878Z: v8: Added a final fallback for Booking\.com pages that remain blocked or incomplete, preserving exact stay checks and existing results\.
- 2026-11-08T10:16:36.478563Z: v9: Recover incomplete Booking\.com pages with a fresh browser while retaining strict stay validation\.
- 2026-11-09T09:51:55.678435Z: v10: Confirm Vitória from the property's own address when Booking\.com city links are missing\.

## Recorded repairs

- 2026-11-07T09:16:19.969928Z: no change
- 2026-11-07T09:17:13.686705Z: repaired
- 2026-11-08T09:34:43.129053Z: no change
- 2026-11-08T09:37:55.192548Z: repaired
- 2026-11-09T09:45:51.528294Z: no change
- 2026-11-09T09:49:53.516901Z: no change
- 2026-11-09T09:52:05.944888Z: repaired
- 2026-11-09T09:52:14.375658Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/operent-vit-ria-nightly-rental-rates-daa743691e70?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
