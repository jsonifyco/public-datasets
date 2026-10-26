# AI hiring radar

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.



[Get the full dataset for free](https://www.jsonify.com/datasets/ai-hiring-radar-e7adb9b7e394?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 1
- Last published: 2026-10-26T09:01:09.738470Z

## Cedar AI hiring radar / roles

75 total rows · 75 sampled · Output revision 10
Published: 2026-10-26T09:01:09.738470Z · Producing pipeline version: 1

[CSV sample](outputs/0642c473c8e3/roles-66cf5513b374/sample.csv) · [JSON sample](outputs/0642c473c8e3/roles-66cf5513b374/sample.json) · [Schema](outputs/0642c473c8e3/roles-66cf5513b374/schema.json)

| application\_url | company | company\_open\_roles | first\_published\_at | job\_key | job\_title | location | observed\_at |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [https://job\-boards\.greenhouse\.io/togetherai/jobs/5238467007](<https://job-boards.greenhouse.io/togetherai/jobs/5238467007>) | Together AI | 85 | 2026\-09\-18T15:46:07\+00:00 | togetherai:5238467007 | Research Intern, Frontier Agents \(Winter 2027\) | San Francisco | 2026\-10\-26T09:00:59\.926346\+00:00 |
| [https://job\-boards\.greenhouse\.io/figureai/jobs/4719239006](<https://job-boards.greenhouse.io/figureai/jobs/4719239006>) | Figure | 104 | 2026\-10\-05T21:23:36\+00:00 | figureai:4719239006 | Commercial Operations Associate | San Jose, CA | 2026\-10\-26T09:00:59\.776309\+00:00 |
| [https://job\-boards\.greenhouse\.io/anthropic/jobs/5462881008](<https://job-boards.greenhouse.io/anthropic/jobs/5462881008>) | Anthropic | 682 | 2026\-10\-24T04:26:19\+00:00 | anthropic:5462881008 | Incident Manager, Safeguards | Boston, MA; San Francisco, CA \| Seattle, WA \| New York City, NY \| Washington, DC | 2026\-10\-26T09:01:00\.028125\+00:00 |
| [https://job\-boards\.greenhouse\.io/anthropic/jobs/5461873008](<https://job-boards.greenhouse.io/anthropic/jobs/5461873008>) | Anthropic | 682 | 2026\-10\-23T14:31:11\+00:00 | anthropic:5461873008 | Applied AI Security Architect \- Healthcare &amp; Life Sciences | New York City, NY; San Francisco, CA \| New York City, NY | 2026\-10\-26T09:01:00\.028125\+00:00 |
| [https://job\-boards\.greenhouse\.io/figureai/jobs/4719591006](<https://job-boards.greenhouse.io/figureai/jobs/4719591006>) | Figure | 104 | 2026\-10\-06T22:53:50\+00:00 | figureai:4719591006 | Commercial Operations Intern \[Winter 2027\] | San Jose, CA | 2026\-10\-26T09:00:59\.776309\+00:00 |

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
