# TDI and TPCIGA data: Texas insurance receiverships and insolvencies dataset, refreshed weekly

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Every Texas insurance receivership on TDI's lists, plus every P&amp;C insolvency in TPCIGA's liquidation directory, with placement, liquidation and closure dates\. Refreshed weekly; export to CSV or Google Sheets\.

[Get the full dataset for free](https://www.jsonify.com/datasets/texas-insurance-company-receiverships-e519ee9a85b0?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 3
- Last published: 2026-11-21T12:48:25.113739Z

## The brief

> I need this data: Every Texas insurance receivership on TDI's lists, plus every P&amp;C insolvency in TPCIGA's liquidation directory, with placement, liquidation and closure dates\. Refreshed weekly; export to CSV or Google Sheets\.

Summary from the public dataset description.

## Texas Insurance Company Receiverships / receiverships

702 total rows · 50 sampled · Output revision 3
Published: 2026-11-21T12:48:25.113739Z · Producing pipeline version: 3

[CSV sample](outputs/d03bd13018e8/receiverships-dec6f28e2698/sample.csv) · [JSON sample](outputs/d03bd13018e8/receiverships-dec6f28e2698/sample.json) · [Schema](outputs/d03bd13018e8/receiverships-dec6f28e2698/schema.json)

| company\_name | date\_closed | date\_placed | date\_placed\_source\_url | directory\_date | domicile\_state | line\_of\_business | liquidation\_date |
| --- | --- | --- | --- | --- | --- | --- | --- |
| ADCO Fire &amp; Casualty | 1991\-12\-20 | 1983\-02\-04 | [https://www\.tdi\.texas\.gov/receiverships/documents/historicrcvrshp\.pdf\#page=1](<https://www.tdi.texas.gov/receiverships/documents/historicrcvrshp.pdf#page=1>) | None | TX | TPA | None |
| Marrs\-Mundy\-Quill Life Ins\. Co\. | 1965\-07\-08 | 1960\-06\-13 | [https://www\.tdi\.texas\.gov/receiverships/documents/historicrcvrshp\.pdf\#page=9](<https://www.tdi.texas.gov/receiverships/documents/historicrcvrshp.pdf#page=9>) | None | TX | LAH | None |
| Summit Ins\. Company of NY | 1986\-06\-26 | 1982\-09\-28 | [https://www\.tdi\.texas\.gov/receiverships/documents/historicrcvrshp\.pdf\#page=13](<https://www.tdi.texas.gov/receiverships/documents/historicrcvrshp.pdf#page=13>) | None | None | P&amp;C | None |
| ICM Insurance Company | None | None | None | 2013\-12\-24 | NY | P&amp;C | 2013\-12\-24 |
| Iowa National Mutual Ins\. Co\. | 1991\-01\-24 | 1985\-12\-16 | [https://www\.tdi\.texas\.gov/receiverships/documents/historicrcvrshp\.pdf\#page=8](<https://www.tdi.texas.gov/receiverships/documents/historicrcvrshp.pdf#page=8>) | None | IA | P&amp;C | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| company\_name | text |
| date\_closed | text |
| date\_placed | text |
| date\_placed\_source\_url | text |
| directory\_date | text |
| domicile\_state | text |
| line\_of\_business | text |
| liquidation\_date | text |
| liquidation\_date\_source\_url | text |
| matched\_tdi\_case\_key | text |
| raw\_status | text |
| receivership\_type | text |
| source | text |
| source\_url | text |
| status | text |
| tdi\_case\_key | text |
| tdi\_match\_status | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["sources"]
  n1["read#95;cases"]
  n2["document#95;scope"]
  n3["case#95;documents"]
  n4["reconcile"]
  n5["receiverships"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
```

- **sources**: Select TDI's Texas case list and the full historical PDF\.
- **read\_cases**: Read all pages of closed historical cases and all three sections of the Texas case list\.
- **document\_scope**: Record the full live\-list count before checking case documents\.
- **case\_documents**: Read linked court documents for each TDI live case and verify date evidence against the document text\.
- **reconcile**: Match the same case across the two sources while retaining separate placements and reopened episodes\.
- **receiverships**: One company per TDI receivership episode, with the status and dates TDI publishes\.

## Version history

- 2026-11-21T11:23:34.246822Z: v1: Combined TDI's current and historic lists into one dataset, keeping separate reopened cases and source links\.
- 2026-11-21T12:28:42.674743Z: v2: Added sourced placement and liquidation dates, TPCIGA records with linked TDI matches, and separate records for the three Members insurers\.
- 2026-11-21T12:43:53.645592Z: v3: Corrected ACCC's effective liquidation date and removed a Petrosurance match to an earlier, closed estate\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/texas-insurance-company-receiverships-e519ee9a85b0?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
