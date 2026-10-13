# Hacker News AI Story Tags

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Read a configurable Hacker News feed \(top 30 by default\) and tag each live story AI or Not AI from its title, URL and post text\. Each update replaces the current snapshot\. Uncertain tags are flagged; linked article bodies and comments are not read\.

[Get the full dataset for free](https://www.jsonify.com/datasets/hacker-news-ai-story-tags-067aaaf184ae) — CSV or JSON · Email required

- Refresh: hourly
- Active pipeline version: 1
- Last published: 2026-10-13T07:02:22.171940Z

## The brief

> make a pipeline that reads hackernews and tags each story whether it's ai or not\.

Original request to Jason.

## Hacker News AI Story Tags / stories

30 total rows · 30 sampled · Output revision 6
Published: 2026-10-13T07:02:22.171940Z · Producing pipeline version: 1

[CSV sample](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/sample.csv) · [JSON sample](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/sample.json) · [Schema](outputs/e4bf8da6eaee/stories-ccc5ed3d0215/schema.json)

| ai\_tag | author | classification\_basis | collected\_at | comment\_count | feed | hn\_url | is\_ai |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Not AI | rickcarlino | Hacker News title, URL and post text; linked article not read | 2026\-10\-13T07:01:45\.075750\+00:00 | 32 | top | [https://news\.ycombinator\.com/item?id=50063417](<https://news.ycombinator.com/item?id=50063417>) | False |
| AI | layer8 | Hacker News title, URL and post text; linked article not read | 2026\-10\-13T06:01:19\.096782\+00:00 | 265 | top | [https://news\.ycombinator\.com/item?id=50063427](<https://news.ycombinator.com/item?id=50063427>) | True |
| Not AI | jsomers | Hacker News title, URL and post text; linked article not read | 2026\-10\-13T06:00:58\.878087\+00:00 | 25 | top | [https://news\.ycombinator\.com/item?id=50041866](<https://news.ycombinator.com/item?id=50041866>) | False |
| AI | sbulaev | Hacker News title, URL and post text; linked article not read | 2026\-10\-13T06:00:58\.965939\+00:00 | 49 | top | [https://news\.ycombinator\.com/item?id=50065692](<https://news.ycombinator.com/item?id=50065692>) | True |
| AI | vishnukool | Hacker News title, URL and post text; linked article not read | 2026\-10\-13T06:01:19\.173779\+00:00 | 84 | top | [https://news\.ycombinator\.com/item?id=50059096](<https://news.ycombinator.com/item?id=50059096>) | True |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns.

### Schema

| Column | Type |
| --- | --- |
| ai\_tag | text |
| author | text |
| classification\_basis | text |
| collected\_at | text |
| comment\_count | integer |
| feed | text |
| hn\_url | text |
| is\_ai | boolean |
| needs\_review | boolean |
| published\_at | text |
| rank | integer |
| score | integer |
| story\_id | jsonb |
| text | text |
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
- **tag\_ai**: Tag each story AI or not AI using its Hacker News title, URL and post text; flag uncertain decisions\.
- **validate**: Check story identities and tags, then preserve the source feed ranking in the saved snapshot\.
- **stories**: Latest Hacker News stories with AI tags and source links\.

## Version history

- 2026-10-12T18:17:39.593635Z: v1: Added Hacker News story collection with AI/Not AI tags, uncertainty flags, story links and live engagement details\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/hacker-news-ai-story-tags-067aaaf184ae) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
