# Hacker News AI Story Tags: Ranked Feed Snapshot

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

A configurable Hacker News feed snapshot with story details and AI or Not AI tags based on each story’s title, URL, and post text\.

[Get the full dataset for free](https://www.jsonify.com/datasets/hacker-news-ai-067aaaf184ae?action=get) — CSV or JSON · Email required

- Refresh: hourly
- Active pipeline version: 5
- Last published: 2026-10-17T13:02:28.769497Z

## The brief

> make a pipeline that reads hackernews and tags each story whether it's ai or not\.

Original request to Jason.

## Hacker News AI Story Tags / stories

29 total rows · 29 sampled · Output revision 111
Published: 2026-10-17T13:02:28.769497Z · Producing pipeline version: 5

[CSV sample](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/sample.csv) · [JSON sample](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/sample.json) · [Schema](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/schema.json)

| author | collected\_at | comment\_count | feed | hn\_url | is\_ai | published\_at | rank |
| --- | --- | --- | --- | --- | --- | --- | --- |
| albinstman | 2026\-10\-17T13:01:01\.535498\+00:00 | 44 | top | [https://news\.ycombinator\.com/item?id=50127979](<https://news.ycombinator.com/item?id=50127979>) | True | 2026\-10\-17T04:36:53\+00:00 | 5 |
| \_\_cayenne\_\_ | 2026\-10\-17T13:02:22\.841376\+00:00 | 103 | top | [https://news\.ycombinator\.com/item?id=50118688](<https://news.ycombinator.com/item?id=50118688>) | True | 2026\-10\-16T14:18:44\+00:00 | 29 |
| ahlCVA | 2026\-10\-17T13:01:35\.346647\+00:00 | 338 | top | [https://news\.ycombinator\.com/item?id=50122800](<https://news.ycombinator.com/item?id=50122800>) | True | 2026\-10\-16T18:55:59\+00:00 | 11 |
| Anon84 | 2026\-10\-17T13:01:09\.715183\+00:00 | 75 | top | [https://news\.ycombinator\.com/item?id=50122431](<https://news.ycombinator.com/item?id=50122431>) | True | 2026\-10\-16T18:32:35\+00:00 | 8 |
| theanonymousone | 2026\-10\-17T13:01:01\.603562\+00:00 | 113 | top | [https://news\.ycombinator\.com/item?id=50129121](<https://news.ycombinator.com/item?id=50129121>) | True | 2026\-10\-17T08:37:46\+00:00 | 1 |

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
