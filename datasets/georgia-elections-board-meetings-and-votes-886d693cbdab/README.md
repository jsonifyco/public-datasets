# Georgia Elections Board Meetings and Votes

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Meeting\-level records of Fulton County Board of Registration and Elections meetings, motions, recorded vote tallies, and explicitly named votes from January 1, 2026 onward\.

[Get the full dataset for free](https://www.jsonify.com/datasets/georgia-elections-board-meetings-and-votes-886d693cbdab?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 19
- Last published: 2026-10-18T21:14:33.754956Z

## The brief

> I need this data: Meeting\-level records of Fulton County Board of Registration and Elections meetings, motions, recorded vote tallies, and explicitly named votes from January 1, 2026 onward\.

Summary from the public dataset description.

## Georgia Elections Board Meetings and Votes / meeting\_actions

1,257 total rows · 100 sampled · Output revision 2
Published: 2026-10-18T21:14:33.754956Z · Producing pipeline version: 19

[CSV sample](outputs/02a6e71cfebc/meeting-actions-7c510d42b127/sample.csv) · [JSON sample](outputs/02a6e71cfebc/meeting-actions-7c510d42b127/sample.json) · [Schema](outputs/02a6e71cfebc/meeting-actions-7c510d42b127/schema.json)

| agenda\_item | board | checked\_at | county | evidence\_quote | meeting\_date | meeting\_location | meeting\_summary |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Executive session | Board of Registration and Elections | 2026\-10\-18T21:07:24\.393700\+00:00 | Fulton | After the executive session, Chair Allen entertained a motion to reconvene from the executive session\. The motion was made by Mrs\. Crawford, seconded by Mrs\. Crawford, and carried by a unanimous vote  | 2026\-02\-12 | None | The board amended its agenda, approved… |
| \#1 – Approval of Agenda | Board of Registration and Elections | 2026\-10\-18T21:07:36\.197770\+00:00 | Fulton | Chair Allen entertained a motion to am… | 2026\-07\-16 | None | The board amended its agenda, approved… |
| 1\) Discussion of Policy for Pre\-Certification Review of Precinct Returns | Board of Elections and Registration | 2026\-10\-18T21:07:58\.213952\+00:00 | Cobb | Motion by Ms\. Efrat to adopt the polic… | 2026\-07\-13 | 100 Cherokee Street | The board approved the agenda and four… |
| Approval of Previous Meeting Minutes — Regular Monthly Board Meeting, December 1, 2025 | Board of Elections and Voter Registration | 2026\-10\-18T21:08:12\.919767\+00:00 | Cherokee | Member Hand made a motion to approve the minutes of the December 1, 2025, meeting; Second by Member Little\.  Motion carries 5\-0\. | 2026\-01\-05 | Northside Cherokee/Bluffs Conference Center, 1130 Bluffs Parkway, Canton, GA 30114 | The board approved its agenda, minutes… |
| 8\. Business — Gainesville City Special Election Council Member Ward 1 | Board of Elections and Registration | 2026\-10\-18T21:13:17\.255358\+00:00 | Hall | MEMBER COCHRAN MADE A MOTION TO APPROVE THE RESOLUTION\. MEMBER SHEATS MADE A SECOND\. UNANIMOUSLY APPROVED\. | 2026\-02\-10 | None | The board approved the agenda and Janu… |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| agenda\_item | text |
| board | text |
| checked\_at | text |
| county | text |
| evidence\_quote | text |
| meeting\_date | text |
| meeting\_location | text |
| meeting\_summary | text |
| meeting\_time | text |
| meeting\_type | text |
| members\_present | jsonb |
| minutes\_status | text |
| minutes\_url | text |
| motion | text |
| motion\_number | integer |
| named\_votes | jsonb |
| outcome | text |
| proposed\_by | text |
| record\_id | text |
| record\_type | text |
| schedule\_url | text |
| seconded\_by | text |
| source\_index\_url | text |
| source\_notes | text |
| state | text |
| video\_timestamp | text |
| video\_url | text |
| vote\_tally\_text | text |
| votes\_abstained | integer |
| votes\_against | integer |
| votes\_for | integer |
| voting\_record\_status | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["official#95;sources"]
  n1["discover#95;documents"]
  n2["read#95;meetings"]
  n3["reconcile#95;coverage"]
  n4["meeting#95;actions"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
```

- **official\_sources**: Choose official election\-board records for the selected Georgia counties; default to the ten largest by population\.
- **discover\_documents**: Read each county's complete official archive and follow its observed pagination; distinguish minutes, drafts, summaries, cancellations, and pending records\.
- **read\_meetings**: Read each official PDF or DOCX completely and extract actual motions and explicitly named votes, retaining collective tallies separately\.
- **reconcile\_coverage**: Keep all approved meeting motions and flag scheduled meetings whose minutes are not yet posted; reject duplicate action identities\.
- **meeting\_actions**: One row per recorded motion, plus an explicit status row for meetings with no motions or unposted minutes\.

## Version history

- 2026-10-18T17:04:55.230934Z: v1: Added Fulton County elections board meeting tracking for 2026 to date, with recorded motions, tallies, explicitly named votes, official evidence and pending\-minutes flags\.
- 2026-10-18T17:09:30.238620Z: v2: Corrected reading of complex PDF layouts so meeting motions can be collected without scrambling their source evidence\.
- 2026-10-18T17:14:15.103409Z: v3: Corrected recognition of explicitly recorded abstentions so valid named votes no longer stop collection\.
- 2026-10-18T17:54:13.606104Z: v4: Expands 2026 meeting records to Georgia’s ten largest counties, with approved minutes, drafts, summaries and missing\-minute status clearly distinguished\. Corrects the Fulton narrative agreement that was previously counted as a motion\.
- 2026-10-18T18:02:31.485010Z: v5: Read Gwinnett’s voting charts correctly, preserving every recorded decision and each member’s explicitly recorded vote\.
- 2026-10-18T18:10:38.290702Z: v6: Handle both Gwinnett voting\-chart layouts without duplicating group decisions, and include ballot decisions in meeting summaries\.
- 2026-10-18T18:18:04.447793Z: v7: Read merged voting\-chart cells correctly while avoiding duplicate rows for grouped ballot decisions\.
- 2026-10-18T18:20:28.736279Z: v8: Recognize explicitly recorded votes described as “voted in opposition\.”
- 2026-10-18T18:23:40.490376Z: v9: Preserve corroborated source\-date discrepancies and include the entire selected final day for Cobb meetings\.
- 2026-10-18T18:28:20.153353Z: v10: Recognize corroborating primary\-election wording in Cobb’s minutes while preserving source\-date discrepancy notes\.
- 2026-10-18T20:01:42.406796Z: v11: Process fewer meeting documents at once to reduce processing interruptions without reducing coverage\.
- 2026-10-18T20:08:31.905910Z: v12: Reads board\-identifying headers in Word minutes so valid DeKalb records are retained without weakening source checks\.
- 2026-10-18T20:12:24.776077Z: v13: Preserves brief official\-summary approvals as notes when no formal motion or member vote is recorded, while retaining explicit motions\.
- 2026-10-18T20:17:02.845796Z: v14: Corrects reading order for Chatham’s scanned minutes so sidebar labels no longer interrupt verified motion quotations\.
- 2026-10-18T20:28:56.289467Z: v15: Corrects scanned Chatham motions split by page footers or sidebar headings, while retaining exact\-source and named\-vote checks\.
- 2026-10-18T20:35:50.055440Z: v16: Reads scanned motions continuously across page breaks without treating generated page markers as source text\.
- 2026-10-18T20:47:58.313542Z: v17: Keeps Forsyth motions intact across scanned page breaks while preserving named votes and source checks\.
- 2026-10-18T20:54:14.623966Z: v18: Verifies Forsyth canvassing minutes that omit the county name using the official board name, office address and named officers\.
- 2026-10-18T21:05:00.914289Z: v19: Handles misread page numbers and reads longer scanned minutes in full, preserving motions and named votes across every page\.

## Recorded repairs

- 2026-10-18T18:32:22.830483Z: temporary blocker

[Get the full dataset for free](https://www.jsonify.com/datasets/georgia-elections-board-meetings-and-votes-886d693cbdab?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
