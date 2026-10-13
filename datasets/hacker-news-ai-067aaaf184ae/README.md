# Hacker News AI

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Read a configurable Hacker News feed \(top 30 by default\) and tag each live story AI or Not AI from its title, URL and post text\. Each update replaces the current snapshot\. The is\_ai and title columns appear first\. Linked article bodies and comments are not read\.

[Get the full dataset for free](https://www.jsonify.com/datasets/hacker-news-ai-067aaaf184ae?action=get) — CSV or JSON · Email required

- Refresh: hourly
- Active pipeline version: 2
- Last published: 2026-10-13T22:02:23.201578Z

## The brief

> make a pipeline that reads hackernews and tags each story whether it's ai or not\.

Original request to Jason.

## Hacker News AI Story Tags / stories

29 total rows · 29 sampled · Output revision 20
Published: 2026-10-13T22:02:23.201578Z · Producing pipeline version: 2

[CSV sample](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/sample.csv) · [JSON sample](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/sample.json) · [Schema](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/schema.json)

| author | collected\_at | comment\_count | feed | hn\_url | is\_ai | published\_at | rank |
| --- | --- | --- | --- | --- | --- | --- | --- |
| formerly\_proven | 2026\-10\-13T22:01:29\.921942\+00:00 | 361 | top | [https://news\.ycombinator\.com/item?id=50069499](<https://news.ycombinator.com/item?id=50069499>) | False | 2026\-10\-13T10:27:00\+00:00 | 9 |
| list | 2026\-10\-13T22:02:07\.712931\+00:00 | 14 | top | [https://news\.ycombinator\.com/item?id=50077096](<https://news.ycombinator.com/item?id=50077096>) | False | 2026\-10\-13T19:17:19\+00:00 | 25 |
| Philpax | 2026\-10\-13T22:01:02\.537282\+00:00 | 398 | top | [https://news\.ycombinator\.com/item?id=50073633](<https://news.ycombinator.com/item?id=50073633>) | False | 2026\-10\-13T15:49:56\+00:00 | 5 |
| mjorgers | 2026\-10\-13T22:01:02\.565293\+00:00 | 108 | top | [https://news\.ycombinator\.com/item?id=50072913](<https://news.ycombinator.com/item?id=50072913>) | False | 2026\-10\-13T15:07:37\+00:00 | 8 |
| cainxinth | 2026\-10\-13T22:02:18\.322032\+00:00 | 133 | top | [https://news\.ycombinator\.com/item?id=50070554](<https://news.ycombinator.com/item?id=50070554>) | False | 2026\-10\-13T12:23:34\+00:00 | 28 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns.

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

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/hacker-news-ai-067aaaf184ae?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
