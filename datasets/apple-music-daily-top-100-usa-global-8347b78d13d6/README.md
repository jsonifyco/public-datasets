# Apple Music data: Top 100 USA and Global chart dataset

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Apple Music Top 100 USA and Global chart dataset with 800 rows, including chart position, song, artist and Apple Music song ID\. Export to CSV, Excel or Google Sheets\.

[Get the full dataset for free](https://www.jsonify.com/datasets/apple-music-daily-top-100-usa-global-8347b78d13d6?action=get) — CSV or JSON · Email required

- Refresh: daily
- Active pipeline version: 1
- Last published: 2026-11-20T10:00:20.516875Z

## The brief

> I need this data: Apple Music Top 100 USA and Global chart dataset with 800 rows, including chart position, song, artist and Apple Music song ID\. Export to CSV, Excel or Google Sheets\.

Summary from the public dataset description.

## Apple Music Daily Top 100 / daily\_charts

800 total rows · 50 sampled · Output revision 5
Published: 2026-11-20T10:00:20.516875Z · Producing pipeline version: 1

[CSV sample](outputs/a7335034808b/daily-charts-f8952c615818/sample.csv) · [JSON sample](outputs/a7335034808b/daily-charts-f8952c615818/sample.json) · [Schema](outputs/a7335034808b/daily-charts-f8952c615818/schema.json)

| chart | chart\_date | position | song\_title | artist | apple\_music\_song\_id | apple\_music\_song\_url | snapshot\_key |
| --- | --- | --- | --- | --- | --- | --- | --- |
| USA | 2026\-11\-17 | 75 | Passionfruit | Drake | 1440891494 | [https://music\.apple\.com/us/song/passionfruit/1440891494](<https://music.apple.com/us/song/passionfruit/1440891494>) | USA:2026\-11\-17:75 |
| USA | 2026\-11\-17 | 12 | Stop The Wedding\! | Ashe | 6795697687 | [https://music\.apple\.com/us/song/stop\-the\-wedding/6795697687](<https://music.apple.com/us/song/stop-the-wedding/6795697687>) | USA:2026\-11\-17:12 |
| USA | 2026\-11\-20 | 42 | So Good \(feat\. Kendrick Lamar\) | Jhené Aiko | 6810716062 | [https://music\.apple\.com/us/song/so\-good\-feat\-kendrick\-lamar/6810716062](<https://music.apple.com/us/song/so-good-feat-kendrick-lamar/6810716062>) | USA:2026\-11\-20:42 |
| Global | 2026\-11\-19 | 56 | E85 | Don Toliver | None | None | Global:2026\-11\-19:56 |
| Global | 2026\-11\-19 | 62 | I'm The Problem | Morgan Wallen | 1802103970 | [https://music\.apple\.com/us/song/im\-the\-problem/1802103970](<https://music.apple.com/us/song/im-the-problem/1802103970>) | Global:2026\-11\-19:62 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| chart | text |
| chart\_date | text |
| position | integer |
| song\_title | text |
| artist | text |
| apple\_music\_song\_id | text |
| apple\_music\_song\_url | text |
| snapshot\_key | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["charts"]
  n1["collect"]
  n2["validate"]
  n3["daily#95;charts"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **charts**: Select Apple's official USA and Global daily Top 100 playlists\.
- **collect**: Read and validate all 100 positions, song titles, artists and song links from each official chart\.
- **validate**: Require both full charts before saving the daily history\.
- **daily\_charts**: Daily Top 100 chart history for USA and Global\. Chart date is the Lisbon observation date\.

## Version history

- 2026-11-17T08:13:56.624892Z: v1: Add daily USA and Global Apple Music Top 100 snapshots with retained chart history\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/apple-music-daily-top-100-usa-global-8347b78d13d6?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
