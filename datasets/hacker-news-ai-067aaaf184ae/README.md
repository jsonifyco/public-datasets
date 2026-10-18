# Hacker News AI Story Tags: Ranked Feed Snapshot

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

A configurable Hacker News feed snapshot with story details and AI or Not AI tags based on each story’s title, URL, and post text\.

[Get the full dataset for free](https://www.jsonify.com/datasets/hacker-news-ai-067aaaf184ae?action=get) — CSV or JSON · Email required

- Refresh: hourly
- Active pipeline version: 5
- Last published: 2026-10-18T23:02:42.370707Z

## The brief

> make a pipeline that reads hackernews and tags each story whether it's ai or not\.

Original request to Jason.

## Hacker News AI Story Tags / stories

30 total rows · 30 sampled · Output revision 145
Published: 2026-10-18T23:02:42.370707Z · Producing pipeline version: 5

[CSV sample](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/sample.csv) · [JSON sample](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/sample.json) · [Schema](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/schema.json)

| author | collected\_at | comment\_count | feed | hn\_url | is\_ai | published\_at | rank |
| --- | --- | --- | --- | --- | --- | --- | --- |
| speckx | 2026\-10\-18T23:02:14\.072866\+00:00 | 43 | top | [https://news\.ycombinator\.com/item?id=50093020](<https://news.ycombinator.com/item?id=50093020>) | False | 2026\-10\-14T18:53:52\+00:00 | 22 |
| RobotToaster | 2026\-10\-18T23:01:06\.193867\+00:00 | 48 | top | [https://news\.ycombinator\.com/item?id=50141076](<https://news.ycombinator.com/item?id=50141076>) | False | 2026\-10\-18T13:48:48\+00:00 | 5 |
| jsomau | 2026\-10\-18T23:01:59\.514262\+00:00 | 88 | top | [https://news\.ycombinator\.com/item?id=50140769](<https://news.ycombinator.com/item?id=50140769>) | False | 2026\-10\-18T13:06:54\+00:00 | 18 |
| \_Microft | 2026\-10\-18T23:02:14\.210834\+00:00 | 13 | top | [https://news\.ycombinator\.com/item?id=50140001](<https://news.ycombinator.com/item?id=50140001>) | False | 2026\-10\-18T11:16:22\+00:00 | 20 |
| pwg | 2026\-10\-18T23:01:43\.180207\+00:00 | 23 | top | [https://news\.ycombinator\.com/item?id=50142449](<https://news.ycombinator.com/item?id=50142449>) | False | 2026\-10\-18T16:20:27\+00:00 | 16 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| author | text |
| collected\_at | text |
| comment\_count | integer |
| feed | text |
| hn\_url | text |
| is\_ai | boolean |
| published\_at | text |
| rank | integer |
| score | integer |
| story\_id | jsonb |
| title | text |
| url | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["read#95;feed"]
  n1["read#95;story"]
  n2["tag#95;ai"]
  n3["validate"]
  n4["stories"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
```

- **read\_feed**: Read a fresh ranked snapshot of the selected Hacker News feed\.
- **read\_story**: Read each story's title, URL, post text, score, author and comment count from Hacker News\.
- **tag\_ai**: Tag each story AI or not AI using its Hacker News title, URL and post text\.
- **validate**: Check story identities and tags, then preserve the source feed ranking in the saved snapshot\.
- **stories**: Latest Hacker News stories with AI tags and source links\.

## Version history

- 2026-10-12T18:17:39.593635Z: v1: Added Hacker News story collection with AI/Not AI tags, uncertainty flags, story links and live engagement details\.
- 2026-10-13T11:39:47.049116Z: v2: Removed ai\_tag, text, classification\_basis and needs\_review\. is\_ai is now the first column and title the second\.
- 2026-10-16T20:05:12.946828Z: v3: Correct AI tagging for discoveries made using AI models, including Claude research in non\-AI disciplines\. Keep the existing metadata\-only scope and saved columns\.
- 2026-10-16T22:06:11.875731Z: v4: Improved AI tagging for agent harnesses and token\-efficiency infrastructure while distinguishing unrelated uses such as Token Ring networking\.
- 2026-10-17T10:08:11.370834Z: v5: Correct Ultramarine 1 Flash's AI tag when its model name appears with its maker's product or technical\-report URL\. Keep the metadata\-only classification scope and other behavior unchanged\.

## Recorded repairs

- 2026-10-17T03:07:22.757514Z: repair failed

[Get the full dataset for free](https://www.jsonify.com/datasets/hacker-news-ai-067aaaf184ae?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
