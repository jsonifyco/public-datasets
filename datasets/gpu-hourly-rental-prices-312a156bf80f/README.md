# GPU Hourly Rental Prices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Listed hourly rental prices for H100 and B200 GPUs, with provider, region, machine, purchase terms, currency and price\-basis details\. The published dataset contains 2,168 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/gpu-hourly-rental-prices-312a156bf80f?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 6
- Last published: 2026-11-06T06:01:36.268359Z

## The brief

> I need this data: Listed hourly rental prices for H100 and B200 GPUs, with provider, region, machine, purchase terms, currency and price\-basis details\. The published dataset contains 2,168 rows\.

Summary from the public dataset description.

## GPU hourly rental prices / rentals

2,168 total rows · 50 sampled · Output revision 15
Published: 2026-11-06T06:01:36.268359Z · Producing pipeline version: 6

[CSV sample](outputs/48259f4a4570/rentals-14788a425070/sample.csv) · [JSON sample](outputs/48259f4a4570/rentals-14788a425070/sample.json) · [Schema](outputs/48259f4a4570/rentals-14788a425070/schema.json)

| gpu\_model | variant | instance | region | country | purchase\_model | commitment | price |
| --- | --- | --- | --- | --- | --- | --- | --- |
| A100 | A100 PCIE | Marketplace offer 32303766 | United Kingdom, GB | UK | on\_demand | No fixed term | 2\.002222222222222 |
| H200 | H200 | p5en\.48xlarge | Europe \(London\) | UK | capacity\_block | Not stated | 63\.158 |
| H100 | H100 SXM | Standard\_ND96is\_H100\_v5 | eastus | US | low\_priority | Interruptible, no fixed term | 17\.698 |
| H200 | NVIDIA HGX H200 | NVIDIA HGX H200 | Europe | Regional | on\_demand | No fixed term | 50\.44 |
| H200 | H200 | p5en\.48xlarge | US West \(Oregon\) | US | capacity\_block | Not stated | 63\.158 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| gpu\_model | text |
| variant | text |
| instance | text |
| region | text |
| country | text |
| purchase\_model | text |
| commitment | text |
| price | double precision |
| currency | text |
| price\_basis | text |
| gpu\_count | integer |
| tax\_note | text |
| offer\_note | text |
| evidence\_quote | text |
| provider | text |
| source\_url | text |
| observed\_at | text |
| observed\_date | text |
| price\_status | text |
| per\_gpu\_hour | double precision |
| instance\_hour | double precision |
| observation\_id | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["history"]
  n1["providers"]
  n2["collect"]
  n3["validate"]
  n4["rentals"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n0 --> n1
  n0 --> n3
```

- **history**: Saved dated GPU observations, reconciled with fresh offers without duplicate daily prices\.
- **providers**: Select the six requested GPU providers and exact H100/B200 model scope\.
- **collect**: Collect official GPU list rates, preserving machine totals, per\-GPU units, regions and purchase commitments\.
- **validate**: Check provider coverage and retain one dated observation per exact GPU offer\.
- **rentals**: Daily official GPU rental prices and scoped non\-listings\.

## Version history

- 2026-10-30T12:34:27.746768Z: v1: Added daily H100/B200 rental data across six providers, including explicit US and UK cloud prices\.
- 2026-10-30T17:10:46.129543Z: v2: Adds six GPU providers and A100, H200, L40S and MI300X coverage\. Completes Azure per\-GPU calculations and standardizes rental commitments while preserving daily price history\.
- 2026-10-30T17:25:49.479475Z: v3: Corrected Google Cloud billing\-column interpretation so unavailable on\-demand prices cannot inherit a Flex\-start rate\.
- 2026-10-30T18:26:24.970423Z: v4: Moved daily duplicate cleanup into every refresh, preserving saved history and normalizing equivalent numbers and commitment labels\.
- 2026-10-30T18:35:38.991961Z: v5: Corrected marketplace country labels and removed unsupported Google Cloud regional assignments in recurring collection and saved\-history reconciliation\.
- 2026-11-05T06:04:59.062177Z: v6: DigitalOcean prices now match exact GPU names directly from each price card, preventing confusion with other accelerator models\.

## Recorded repairs

- 2026-11-05T06:02:34.072908Z: no change
- 2026-11-05T06:04:19.636622Z: no change
- 2026-11-05T06:05:08.340297Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/gpu-hourly-rental-prices-312a156bf80f?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
