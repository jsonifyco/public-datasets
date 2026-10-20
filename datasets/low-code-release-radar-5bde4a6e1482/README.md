# Low\-Code Release Radar: Latest n8n, Appsmith and Budibase Releases

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

A daily snapshot of the latest stable GitHub releases for n8n, Appsmith and Budibase, with publication dates, release notes and source links\.

[Get the full dataset for free](https://www.jsonify.com/datasets/low-code-release-radar-5bde4a6e1482?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 1
- Last published: 2026-10-20T08:00:49.277060Z

## The brief

> I need this data: A daily snapshot of the latest stable GitHub releases for n8n, Appsmith and Budibase, with publication dates, release notes and source links\.

Summary from the public dataset description.

## TechWB Low\-Code Releases / releases

3 total rows · 3 sampled · Output revision 8
Published: 2026-10-20T08:00:49.277060Z · Producing pipeline version: 1

[CSV sample](outputs/a4973f437b80/releases-20195541dc5d/sample.csv) · [JSON sample](outputs/a4973f437b80/releases-20195541dc5d/sample.json) · [Schema](outputs/a4973f437b80/releases-20195541dc5d/schema.json)

| checked\_at | published\_at | release\_age\_days | release\_id | release\_name | release\_notes | release\_url | repository |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 2026\-10\-20T08:00:45\.704097\+00:00 | 2026\-10\-19T08:09:46Z | 0 | 417045683 | v3\.50\.0 | \#\# What's Changed \* Bump uuid from 8\.3\.2 to 14\.0\.0 by @dependabot\[bot\] in [https://github\.com/Budibase…](<https://github.com/Budibase%E2%80%A6>) | [https://github\.com/Budibase/budibase/releases/tag/v3\.50\.0](<https://github.com/Budibase/budibase/releases/tag/v3.50.0>) | Budibase/budibase |
| 2026\-10\-20T08:00:45\.797438\+00:00 | 2026\-10\-09T15:59:16Z | 10 | 400884069 | Release v2\.5\.0 🌈 | \#\# 🗑️ Feature Removal Reminder \- September 30, 2026 \- EOL    \*\*Appsmith AI reached end of life on Sep… | [https://github\.com/appsmithorg/appsmith/releases/tag/v2\.5\.0](<https://github.com/appsmithorg/appsmith/releases/tag/v2.5.0>) | appsmithorg/appsmith |
| 2026\-10\-20T08:00:45\.733748\+00:00 | 2026\-10\-19T07:23:26Z | 1 | 417010683 | n8n@2\.43\.8 | \#\# \[2\.43\.8\]\([https://github\.com/n8n\-io/n8n/compare/n8n@2\.43\.7\.\.\.n8n@2\.43\.8](<https://github.com/n8n-io/n8n/compare/n8n@2.43.7...n8n@2.43.8>)\) \(2026\-10\-19\)   \#\#\# Bug Fix… | [https://github\.com/n8n\-io/n8n/releases/tag/n8n%402\.43\.8](<https://github.com/n8n-io/n8n/releases/tag/n8n%402.43.8>) | n8n\-io/n8n |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| checked\_at | text |
| published\_at | text |
| release\_age\_days | integer |
| release\_id | text |
| release\_name | text |
| release\_notes | text |
| release\_url | text |
| repository | text |
| repository\_url | text |
| source\_url | text |
| tool | text |
| use\_case | text |
| version | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["watchlist"]
  n1["latest#95;release"]
  n2["releases"]
  n0 --> n1
  n1 --> n2
```

- **watchlist**: Choose three low\-code tools relevant to TechWB's MVP and automation work\.
- **latest\_release**: Read each project's latest stable GitHub release, validating identity and publication fields before saving it\.
- **releases**: Latest stable releases for three curated low\-code tools; refreshed snapshot, not a release archive\.

## Version history

- 2026-10-13T11:18:15.883478Z: v1: Created a low\-code release radar for n8n, Appsmith and Budibase with fresh source checks, release notes and direct links\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/low-code-release-radar-5bde4a6e1482?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
