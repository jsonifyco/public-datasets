# Turo Classic and Exotic Car Rentals

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Saved Turo listings for classic, exotic and sports cars, with daily prices and trip context\. Snapshot: 60 listings\.

[Get the full dataset for free](https://www.jsonify.com/datasets/turo-classic-and-exotic-car-rentals-9f51f87bf45b?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-11-13T15:58:41.083512Z

## The brief

> I need this data: Saved Turo listings for classic, exotic and sports cars, with daily prices and trip context\. Snapshot: 60 listings\.

Summary from the public dataset description.

## Turo classic and exotic car rentals / Listings

60 total rows · 10 sampled · Output revision 1
Published: 2026-11-13T15:58:41.083512Z · Producing pipeline version: 1

[CSV sample](outputs/4aeb93a90938/listings-5009238dba6b/sample.csv) · [JSON sample](outputs/4aeb93a90938/listings-5009238dba6b/sample.json) · [Schema](outputs/4aeb93a90938/listings-5009238dba6b/schema.json)

| captured\_at | city | currency | daily\_price | host\_name | host\_type | listing\_url | make |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 2026\-11\-10T18:13:34\.680730\+00:00 | Miami | USD | 368 | Thomas | Unconfirmed | [https://turo\.com/us/en/car\-rental/united\-states/miami\-fl/porsche/911/1840420](<https://turo.com/us/en/car-rental/united-states/miami-fl/porsche/911/1840420>) | Porsche |
| 2026\-11\-10T18:13:34\.680730\+00:00 | Miami | USD | 367 | Valeria | Unconfirmed | [https://turo\.com/us/en/car\-rental/united\-states/miami\-fl/porsche/911/3258853](<https://turo.com/us/en/car-rental/united-states/miami-fl/porsche/911/3258853>) | Porsche |
| 2026\-11\-10T18:13:49\.723114\+00:00 | New York | USD | 970 | Simran | Unconfirmed | [https://turo\.com/us/en/car\-rental/united\-states/jersey\-city\-nj/porsche/911/3710855](<https://turo.com/us/en/car-rental/united-states/jersey-city-nj/porsche/911/3710855>) | Porsche |
| 2026\-11\-10T18:13:32\.133400\+00:00 | Los Angeles | USD | 1518 | UniqueRideLA | Unconfirmed | [https://turo\.com/us/en/car\-rental/united\-states/beverly\-hills\-ca/lamborghini/huracan\-evo/2016276](<https://turo.com/us/en/car-rental/united-states/beverly-hills-ca/lamborghini/huracan-evo/2016276>) | Lamborghini |
| 2026\-11\-10T18:13:32\.133400\+00:00 | Los Angeles | USD | 1439 | Rent FYV Car Rental Marketplace | Unconfirmed | [https://turo\.com/us/en/car\-rental/united\-states/beverly\-hills\-ca/lamborghini/huracan\-evo/2888385](<https://turo.com/us/en/car-rental/united-states/beverly-hills-ca/lamborghini/huracan-evo/2888385>) | Lamborghini |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| captured\_at | text |
| city | text |
| currency | text |
| daily\_price | double precision |
| host\_name | text |
| host\_type | text |
| listing\_url | text |
| make | text |
| model | text |
| pickup\_location | text |
| price\_basis | text |
| rating | double precision |
| trip\_count | integer |
| trip\_end | text |
| trip\_start | text |
| year | integer |

## How the pipeline works

```mermaid
flowchart LR
  n0["saved0"]
  n1["prepare"]
  n2["tables"]
  n3["Listings"]
  n1 --> n2
  n0 --> n1
  n2 --> n3
  n0 --> n1
```

- **saved0**: Read the existing saved worksheet without contacting any sources\.
- **prepare**: Copy the saved sample and sort it for public reading without refreshing sources\.
- **tables**: Keep the saved worksheets separate in the public workbook\.
- **Listings**: Existing saved sample records\.

## Version history

- 2026-11-13T15:58:27.529320Z: v1: Make the saved sample available for a neutral public page without new collection\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/turo-classic-and-exotic-car-rentals-9f51f87bf45b?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
