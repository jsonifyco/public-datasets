# AI hiring radar

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.



[Get the full dataset for free](https://www.jsonify.com/datasets/ai-hiring-radar-e7adb9b7e394?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 1
- Last published: 2026-10-17T09:00:46.820048Z

## Cedar AI hiring radar / roles

75 total rows · 75 sampled · Output revision 5
Published: 2026-10-17T09:00:46.820048Z · Producing pipeline version: 1

[CSV sample](outputs/0642c473c8e3/roles-66cf5513b374/sample.csv) · [JSON sample](outputs/0642c473c8e3/roles-66cf5513b374/sample.json) · [Schema](outputs/0642c473c8e3/roles-66cf5513b374/schema.json)

| application\_url | company | company\_open\_roles | first\_published\_at | job\_key | job\_title | location | observed\_at |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [https://job\-boards\.greenhouse\.io/togetherai/jobs/5267198007](<https://job-boards.greenhouse.io/togetherai/jobs/5267198007>) | Together AI | 78 | 2026\-10\-16T22:48:51\+00:00 | togetherai:5267198007 | Research Intern, Frontier Speculative Decoding \(Summer 2027\) | San Francisco | 2026\-10\-17T09:00:37\.854760\+00:00 |
| [https://job\-boards\.greenhouse\.io/figureai/jobs/4722086006](<https://job-boards.greenhouse.io/figureai/jobs/4722086006>) | Figure | 100 | 2026\-10\-14T19:54:00\+00:00 | figureai:4722086006 | Embedded Software Engineering Intern \[Winter 2027\] | San Jose, CA | 2026\-10\-17T09:00:37\.776747\+00:00 |
| [https://job\-boards\.greenhouse\.io/figureai/jobs/4711258006](<https://job-boards.greenhouse.io/figureai/jobs/4711258006>) | Figure | 100 | 2026\-09\-04T16:23:18\+00:00 | figureai:4711258006 | Senior Engineering Technician | San Jose, CA | 2026\-10\-17T09:00:37\.776747\+00:00 |
| [https://job\-boards\.greenhouse\.io/figureai/jobs/4717759006](<https://job-boards.greenhouse.io/figureai/jobs/4717759006>) | Figure | 100 | 2026\-09\-29T23:55:31\+00:00 | figureai:4717759006 | Data Operations Coordinator \(Night Shift\) | San Jose, CA | 2026\-10\-17T09:00:37\.776747\+00:00 |
| [https://job\-boards\.greenhouse\.io/anthropic/jobs/5449229008](<https://job-boards.greenhouse.io/anthropic/jobs/5449229008>) | Anthropic | 656 | 2026\-10\-14T16:34:30\+00:00 | anthropic:5449229008 | Staff Forward Deployed Engineer | New York City, NY; San Francisco, CA; Seattle, WA | 2026\-10\-17T09:00:37\.718850\+00:00 |

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
