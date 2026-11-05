# SEC Form D Filings Search: New Private Funding Rounds

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

SEC Form D filings, updated weekly: issuer, state, industry, offering amount, amount sold, first sale date and exemption for every new private funding round\.

[Get the full dataset for free](https://www.jsonify.com/datasets/sec-form-d-filings-6d5f1a7a0494?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 3
- Last published: 2026-11-05T11:59:05.068703Z

## The brief

> I need this data: SEC Form D filings, updated weekly: issuer, state, industry, offering amount, amount sold, first sale date and exemption for every new private funding round\.

Summary from the public dataset description.

## SEC Form D filings / filings

1,266 total rows · 50 sampled · Output revision 2
Published: 2026-11-05T11:59:05.068703Z · Producing pipeline version: 2

[CSV sample](outputs/c449a470b322/filings-4b3249d71f72/sample.csv) · [JSON sample](outputs/c449a470b322/filings-4b3249d71f72/sample.json) · [Schema](outputs/c449a470b322/filings-4b3249d71f72/schema.json)

| accession\_number | cik | date\_of\_first\_sale | entity\_type | federal\_exemptions | filing\_date | filing\_url | first\_sale\_yet\_to\_occur |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 0002157581\-26\-000001 | 0002157581 | 2026\-10\-15 | Corporation | 06b | 2026\-10\-29 | [https://www\.sec\.gov/Archives/edgar/data/2157581/000215758126000001/0002157581\-26\-000001\-index\.html](<https://www.sec.gov/Archives/edgar/data/2157581/000215758126000001/0002157581-26-000001-index.html>) | None |
| 0002159667\-26\-000001 | 0002159667 | None | Other | 06b, 3C, 3C\.7 | 2026\-11\-04 | [https://www\.sec\.gov/Archives/edgar/data/2159667/000215966726000001/0002159667\-26\-000001\-index\.html](<https://www.sec.gov/Archives/edgar/data/2159667/000215966726000001/0002159667-26-000001-index.html>) | True |
| 0001442838\-26\-000001 | 0001442838 | 2005\-09\-15 | Limited Liability Company | 06b, 3C, 3C\.1 | 2026\-11\-03 | [https://www\.sec\.gov/Archives/edgar/data/1442838/000144283826000001/0001442838\-26\-000001\-index\.html](<https://www.sec.gov/Archives/edgar/data/1442838/000144283826000001/0001442838-26-000001-index.html>) | None |
| 0001839195\-26\-000001 | 0001839195 | 2021\-01\-01 | Other | 06c, 3C, 3C\.1 | 2026\-10\-29 | [https://www\.sec\.gov/Archives/edgar/data/1839195/000183919526000001/0001839195\-26\-000001\-index\.html](<https://www.sec.gov/Archives/edgar/data/1839195/000183919526000001/0001839195-26-000001-index.html>) | None |
| 0001930720\-26\-000003 | 0001930720 | 2022\-03\-29 | Limited Partnership | 06b, 3C, 3C\.7 | 2026\-10\-29 | [https://www\.sec\.gov/Archives/edgar/data/1930720/000193072026000003/0001930720\-26\-000003\-index\.html](<https://www.sec.gov/Archives/edgar/data/1930720/000193072026000003/0001930720-26-000003-index.html>) | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| accession\_number | text |
| cik | text |
| date\_of\_first\_sale | text |
| entity\_type | text |
| federal\_exemptions | text |
| filing\_date | text |
| filing\_url | text |
| first\_sale\_yet\_to\_occur | boolean |
| form\_type | text |
| industry\_group | text |
| is\_amendment | boolean |
| issuer\_city | text |
| issuer\_name | text |
| issuer\_state | text |
| jurisdiction\_of\_incorporation | text |
| minimum\_investment\_usd | double precision |
| offering\_amount\_indefinite | boolean |
| revenue\_range | text |
| total\_amount\_sold\_usd | double precision |
| total\_number\_already\_invested | integer |
| total\_offering\_amount\_usd | double precision |
| total\_remaining\_usd | double precision |
| year\_of\_incorporation | integer |

## How the pipeline works

```mermaid
flowchart LR
  n0["published"]
  n1["days"]
  n2["indexes"]
  n3["reserve"]
  n4["filings"]
  n5["validate"]
  n6["filings"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n0 --> n1
  n0 --> n1
```

- **published**: Previously saved filings used to exclude existing accession numbers\.
- **days**: Select SEC daily indexes within the previous ten completed UTC calendar days\.
- **indexes**: Read each SEC form index and retain only D and D/A filing links\.
- **reserve**: Deduplicate new filings and reserve no more than 5,000 distinct filings per UTC month\.
- **filings**: Read and checkpoint each filing, retaining only the specified non\-personal issuer and offering fields\.
- **validate**: Count skipped documents and verify unique accession numbers before saving the new filing batch\.
- **filings**: One row per SEC Form D or D/A filing, without people or contact details\.

## Version history

- 2026-11-05T11:48:34.455281Z: v1: Create private incremental SEC Form D collection with requested fields and monthly limit\.
- 2026-11-05T11:53:56.561402Z: v2: Resolve primary issuer identity for filings listed under multiple issuers\.
- 2026-11-05T12:10:52.133260Z: v3: Check the prior ten completed UTC days on every refresh and read fresh SEC indexes to catch late additions\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/sec-form-d-filings-6d5f1a7a0494?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
