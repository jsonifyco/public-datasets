# Travel eSIM Plans and Prices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Public retail travel eSIM plan and price data for Airalo, Holafly, Nomad and Saily, with destination, data allowance, validity and coverage details\. The published dataset contains 81,050 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/aviso-travel-esim-price-tracker-4a8066232783?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 9
- Last published: 2026-11-09T06:46:39.091556Z

## The brief

> I need this data: Public retail travel eSIM plan and price data for Airalo, Holafly, Nomad and Saily, with destination, data allowance, validity and coverage details\. The published dataset contains 81,050 rows\.

Summary from the public dataset description.

## Travel eSIM plans and prices / plans

81,050 total rows · 50 sampled · Output revision 4
Published: 2026-11-09T06:46:39.091556Z · Producing pipeline version: 9

[CSV sample](outputs/c5ba8f3996ca/plans-c404dc69b55c/sample.csv) · [JSON sample](outputs/c5ba8f3996ca/plans-c404dc69b55c/sample.json) · [Schema](outputs/c5ba8f3996ca/plans-c404dc69b55c/schema.json)

| collected\_at | coverage\_type | currency | data\_gb | destination\_country\_iso2 | destination\_country\_name | network\_speed\_notes | plan\_name |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 2026\-11\-09T06:41:29\.642689\+00:00 | country | USD | None | DK | Denmark | eSIM Details Coverage Unlimited data Fast and reliable internet No more roaming charges Alway… | Copenhagen · unlimited · 1 days |
| 2026\-11\-09T06:38:16\.171411\+00:00 | regional | EUR | 3 | ES | Spain | Speed: 3G/4G/LTE/5G, depending on local network providers\.; Network: Stable and reliable connection from the best local network providers in Europe\. | Europe · 3 GB · 30 days |
| 2026\-11\-09T06:43:32\.141921\+00:00 | country | USD | None | IE | Ireland | eSIM Details Coverage Unlimited data Fast and reliable internet No more roaming charges Alway… | Ireland · unlimited · 23 days |
| 2026\-11\-09T06:38:42\.671951\+00:00 | regional | USD | None | GW | Guinea\-Bissau | eSIM Details Coverage Unlimited data Fast and reliable internet No more roaming charges Alway… | Africa · unlimited · 55 days |
| 2026\-11\-09T06:39:40\.626966\+00:00 | country | EUR | None | ES | Spain | Lower speed rate of 1 Mbps after 3 GB usage per day\.; Orange 5G;  | Mansetel · Unlimited \- 30 days |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| collected\_at | text |
| coverage\_type | text |
| currency | text |
| data\_gb | double precision |
| destination\_country\_iso2 | text |
| destination\_country\_name | text |
| network\_speed\_notes | text |
| plan\_name | text |
| plan\_url | text |
| price | double precision |
| price\_usd | double precision |
| provider | text |
| unlimited | boolean |
| validity\_days | integer |

## How the pipeline works

```mermaid
flowchart LR
  n0["sources"]
  n1["discover"]
  n2["destinations"]
  n3["listing#95;pages"]
  n4["pages"]
  n5["collect"]
  n6["normalize"]
  n7["plans"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n6 --> n7
```

- **sources**: Choose the requested providers and load current currency conversion rates for comparable US dollar prices\.
- **discover**: Read each provider’s complete destination catalog and discover local, regional and global plan pages\.
- **destinations**: Combine destination pages from all providers, retaining every discovered market for collection\.
- **listing\_pages**: Follow every Holafly catalog page so countries and separately marketed city offers are not missed\.
- **pages**: Reconcile the full paginated destination inventory and remove duplicate links before reading plans\.
- **collect**: Read all plan variants from each destination page and expand regional or global coverage into individual destination countries\.
- **normalize**: Validate prices and country identities, remove duplicate representations and publish the latest complete plan catalog\.
- **plans**: Latest travel eSIM retail offers, one plan variant per covered destination country\.

## Version history

- 2026-11-06T19:22:16.717478Z: v1: Build the complete four\-provider destination eSIM tracker with consistent coverage labels, public catalog pagination, prices, currencies and plan\-specific network restrictions\.
- 2026-11-06T19:58:10.009555Z: v2: Handle Nomad's retired Netherlands Antilles code without stopping the catalog\. Preserve the provider's aggregate destination and flag that individual island coverage is unspecified\.
- 2026-11-06T20:10:20.502987Z: v3: Normalize Hawaii's source subdivision code to US while retaining the Hawaii\-specific plan identity\.
- 2026-11-06T20:32:46.170160Z: v4: Recognize Saily's internal Netherlands Antilles destination code and retain its plans with an explicit island\-coverage caveat\.
- 2026-11-06T20:47:02.699342Z: v5: Resolve Puerto Rico plans whose Airalo country\-code field is omitted\.
- 2026-11-06T21:18:27.827080Z: v6: Handle Holafly's standalone Hawaii plans using the existing verified Hawaii\-to\-US identity mapping\.
- 2026-11-06T21:27:05.683102Z: v7: Resolve Holafly's Japan and South Korea bundle into the two covered countries\.
- 2026-11-06T21:52:10.697693Z: v8: Map Holafly's Saint Barthélemy plans to their standard country code\.
- 2026-11-09T06:34:57.509401Z: v9: Saily destination discovery now loads the full page when its initial response is incomplete, and verifies every destination before updating prices\.

## Recorded repairs

- 2026-11-09T06:17:33.128952Z: no change
- 2026-11-09T06:20:35.526602Z: no change
- 2026-11-09T06:35:06.836957Z: repaired
- 2026-11-09T06:35:13.640029Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/aviso-travel-esim-price-tracker-4a8066232783?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
