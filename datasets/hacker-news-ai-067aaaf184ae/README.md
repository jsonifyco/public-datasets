# Hacker News AI Story Tags

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

A Hacker News stories dataset with story details and AI or Not AI tags based on each story’s title, URL, and post text\.

[Get the full dataset for free](https://www.jsonify.com/datasets/hacker-news-ai-067aaaf184ae?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 5
- Last published: 2026-11-02T09:04:03.677197Z

## The brief

> make a pipeline that reads hackernews and tags each story whether it's ai or not\.

Original request to Jason.

## Hacker News AI Story Tags / stories

30 total rows · 10 sampled · Output revision 210
Published: 2026-11-02T09:04:03.677197Z · Producing pipeline version: 5

[CSV sample](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/sample.csv) · [JSON sample](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/sample.json) · [Schema](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/schema.json)

| author | collected\_at | comment\_count | feed | hn\_url | is\_ai | published\_at | rank |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Anon84 | 2026\-11\-02T09:02:57\.277964\+00:00 | 70 | top | [https://news\.ycombinator\.com/item?id=50325454](<https://news.ycombinator.com/item?id=50325454>) | True | 2026\-11\-01T13:24:49\+00:00 | 18 |
| n\_plus\_1\_acc | 2026\-11\-02T09:03:43\.922076\+00:00 | 55 | top | [https://news\.ycombinator\.com/item?id=50324371](<https://news.ycombinator.com/item?id=50324371>) | False | 2026\-11\-01T10:44:20\+00:00 | 28 |
| ecares | 2026\-11\-02T09:03:54\.875538\+00:00 | 205 | top | [https://news\.ycombinator\.com/item?id=50320963](<https://news.ycombinator.com/item?id=50320963>) | False | 2026\-10\-31T22:41:06\+00:00 | 29 |
| LecroJS | 2026\-11\-02T09:01:41\.923426\+00:00 | 489 | top | [https://news\.ycombinator\.com/item?id=50328896](<https://news.ycombinator.com/item?id=50328896>) | False | 2026\-11\-01T19:35:27\+00:00 | 6 |
| misswaterfairy | 2026\-11\-02T09:03:23\.219798\+00:00 | 150 | top | [https://news\.ycombinator\.com/item?id=50331402](<https://news.ycombinator.com/item?id=50331402>) | False | 2026\-11\-02T00:17:27\+00:00 | 21 |

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
