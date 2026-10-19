# AI hiring radar

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.



[Get the full dataset for free](https://www.jsonify.com/datasets/ai-hiring-radar-e7adb9b7e394?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 1
- Last published: 2026-10-19T09:01:07.099200Z

## Cedar AI hiring radar / roles

75 total rows · 75 sampled · Output revision 7
Published: 2026-10-19T09:01:07.099200Z · Producing pipeline version: 1

[CSV sample](outputs/0642c473c8e3/roles-66cf5513b374/sample.csv) · [JSON sample](outputs/0642c473c8e3/roles-66cf5513b374/sample.json) · [Schema](outputs/0642c473c8e3/roles-66cf5513b374/schema.json)

| application\_url | company | company\_open\_roles | first\_published\_at | job\_key | job\_title | location | observed\_at |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [https://job\-boards\.greenhouse\.io/figureai/jobs/4722786006](<https://job-boards.greenhouse.io/figureai/jobs/4722786006>) | Figure | 100 | 2026\-10\-16T21:26:36\+00:00 | figureai:4722786006 | Mobile Service Technician | San Jose, CA | 2026\-10\-19T09:00:53\.774701\+00:00 |
| [https://job\-boards\.greenhouse\.io/figureai/jobs/4710288006](<https://job-boards.greenhouse.io/figureai/jobs/4710288006>) | Figure | 100 | 2026\-09\-01T19:44:54\+00:00 | figureai:4710288006 | IT Client Engineer | San Jose, CA | 2026\-10\-19T09:00:53\.774701\+00:00 |
| [https://job\-boards\.greenhouse\.io/anthropic/jobs/5424305008](<https://job-boards.greenhouse.io/anthropic/jobs/5424305008>) | Anthropic | 657 | 2026\-10\-16T09:34:58\+00:00 | anthropic:5424305008 | Manager, Applied AI Architects \- Digital Natives, EMEA | London, UK | 2026\-10\-19T09:00:53\.895599\+00:00 |
| [https://job\-boards\.greenhouse\.io/togetherai/jobs/5238654007](<https://job-boards.greenhouse.io/togetherai/jobs/5238654007>) | Together AI | 78 | 2026\-09\-15T20:56:31\+00:00 | togetherai:5238654007 | Director of Brand | San Francisco | 2026\-10\-19T09:00:53\.673791\+00:00 |
| [https://job\-boards\.greenhouse\.io/anthropic/jobs/5432425008](<https://job-boards.greenhouse.io/anthropic/jobs/5432425008>) | Anthropic | 657 | 2026\-10\-15T21:32:39\+00:00 | anthropic:5432425008 | Risk &amp; Insurance Specialist | San Francisco, CA | 2026\-10\-19T09:00:53\.895599\+00:00 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| application\_url | text |
| company | text |
| company\_open\_roles | integer |
| first\_published\_at | text |
| job\_key | text |
| job\_title | text |
| location | text |
| observed\_at | text |
| source\_updated\_at | text |
| source\_url | text |
| work\_type | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["companies"]
  n1["open#95;roles"]
  n2["rank#95;roles"]
  n3["roles"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **companies**: Select the demo AI\-company watchlist: Anthropic, Figure, and Together AI; these are not asserted Cedar customers\.
- **open\_roles**: Read each company's live public Greenhouse board, validate complete counts, apply optional title/location filters, and retain its newest\-listed open roles\.
- **rank\_roles**: Sort the current snapshot by source first\-published date, newest first; do not infer candidate fit or treat updates as new postings\.
- **roles**: Newest\-listed open roles across the selected AI\-company watchlist\.

## Version history

- 2026-10-13T11:16:08.365368Z: v1: Created a Cedar\-focused AI hiring radar with daily\-ready snapshots of newest\-listed open jobs at Anthropic, Figure and Together AI, plus company, title, location and size controls\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/ai-hiring-radar-e7adb9b7e394?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
