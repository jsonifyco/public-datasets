# Weekly U\.S\. Diesel and Gas Price History

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Weekly U\.S\. retail diesel and regular gasoline prices from the U\.S\. Energy Information Administration \(EIA\)\. The published dataset contains 2,160 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/weekly-us-retail-diesel-and-regular-gasoline-prices-ecf766d923b4?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 1
- Last published: 2026-11-11T06:01:03.609834Z

## The brief

> I need this data: Weekly U\.S\. retail diesel and regular gasoline prices from the U\.S\. Energy Information Administration \(EIA\)\. The published dataset contains 2,160 rows\.

Summary from the public dataset description.

## EIA weekly retail fuel prices / prices

2,160 total rows · 50 sampled · Output revision 5
Published: 2026-11-11T06:01:03.609834Z · Producing pipeline version: 1

[CSV sample](outputs/a71484658f80/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/a71484658f80/prices-fe81f9390ffe/sample.json) · [Schema](outputs/a71484658f80/prices-fe81f9390ffe/schema.json)

| area | area\_type | eia\_series\_id | price\_usd\_per\_gallon | product | source\_url | week\_date |
| --- | --- | --- | --- | --- | --- | --- |
| Denver | city | EMM\_EPMR\_PTE\_YDEN\_DPG | 2\.328 | regular gasoline | [https://www\.eia\.gov/dnav/pet/xls/PET\_PRI\_GND\_DCUS\_YDEN\_W\.xls](<https://www.eia.gov/dnav/pet/xls/PET_PRI_GND_DCUS_YDEN_W.xls>) | 2025\-12\-01 |
| Los Angeles | city | EMM\_EPMR\_PTE\_Y05LA\_DPG | 4\.407 | regular gasoline | [https://www\.eia\.gov/dnav/pet/xls/PET\_PRI\_GND\_DCUS\_Y05LA\_W\.xls](<https://www.eia.gov/dnav/pet/xls/PET_PRI_GND_DCUS_Y05LA_W.xls>) | 2026\-02\-23 |
| Lower Atlantic \(PADD 1C\) | PADD region | EMM\_EPMR\_PTE\_R1Z\_DPG | 3\.783 | regular gasoline | [https://www\.eia\.gov/dnav/pet/xls/PET\_PRI\_GND\_DCUS\_R1Z\_W\.xls](<https://www.eia.gov/dnav/pet/xls/PET_PRI_GND_DCUS_R1Z_W.xls>) | 2026\-08\-31 |
| New York City | city | EMM\_EPMR\_PTE\_Y35NY\_DPG | 4\.316 | regular gasoline | [https://www\.eia\.gov/dnav/pet/xls/PET\_PRI\_GND\_DCUS\_Y35NY\_W\.xls](<https://www.eia.gov/dnav/pet/xls/PET_PRI_GND_DCUS_Y35NY_W.xls>) | 2026\-06\-01 |
| Denver | city | EMM\_EPMR\_PTE\_YDEN\_DPG | 2\.842 | regular gasoline | [https://www\.eia\.gov/dnav/pet/xls/PET\_PRI\_GND\_DCUS\_YDEN\_W\.xls](<https://www.eia.gov/dnav/pet/xls/PET_PRI_GND_DCUS_YDEN_W.xls>) | 2026\-03\-02 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| area | text |
| area\_type | text |
| eia\_series\_id | text |
| price\_usd\_per\_gallon | double precision |
| product | text |
| source\_url | text |
| week\_date | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["published#95;prices"]
  n1["discover#95;areas"]
  n2["collect#95;area"]
  n3["validate#95;prices"]
  n4["prices"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n0 --> n1
  n0 --> n1
```

- **published\_prices**: Existing saved prices, used to exclude keys already collected\.
- **discover\_areas**: Read all listed EIA areas and exclude previously saved series\-week keys\.
- **collect\_area**: Checkpoint each area's history batch and verify recent prices against its live EIA table\.
- **validate\_prices**: Count skips, check required fields and unique keys, then save verified prices\.
- **prices**: One source\-backed retail fuel price for one EIA product, area and week\.

## Version history

- 2026-10-29T16:42:49.403624Z: v1: Collects the latest 52 weeks of EIA diesel and regular gasoline prices across every listed area\. Keeps new keys only, counts skipped items, and enforces a conservative monthly collection limit\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/weekly-us-retail-diesel-and-regular-gasoline-prices-ecf766d923b4?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
