# Trade Show List: US Conference Database, Updated Weekly

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

A list of upcoming US trade shows and conferences from 17 convention centers: event, venue, city, dates and type\. B2B events only, refreshed weekly\.

[Get the full dataset for free](https://www.jsonify.com/datasets/us-convention-center-b2b-events-c9c108704516?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-11-26T13:14:42.958453Z

## The brief

> I need this data: A list of upcoming US trade shows and conferences from 17 convention centers: event, venue, city, dates and type\. B2B events only, refreshed weekly\.

Summary from the public dataset description.

## Upcoming US convention center events / upcoming\_events

345 total rows · 50 sampled · Output revision 1
Published: 2026-11-26T13:14:42.958453Z · Producing pipeline version: 1

[CSV sample](outputs/3b2851726f69/upcoming-events-54b6d8b38960/sample.csv) · [JSON sample](outputs/3b2851726f69/upcoming-events-54b6d8b38960/sample.json) · [Schema](outputs/3b2851726f69/upcoming-events-54b6d8b38960/schema.json)

| city | end\_date | event\_name | event\_type | event\_website | expected\_attendance | first\_seen\_date | industry |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Miami Beach | 2027\-04\-18 | The Aesthetic Society Meeting 2027 | Convention | None | None | 2026\-11\-26 | None |
| Raleigh | 2027\-01\-20 | Human Trafficking Conference | Conference | None | None | 2026\-11\-26 | None |
| Madison | 2027\-05\-28 | ACD Expo 2027 | None | None | None | 2026\-11\-26 | None |
| Madison | 2027\-06\-25 | 2027 PLC at Work Institute | None | None | None | 2026\-11\-26 | None |
| Tampa | 2027\-02\-12 | DRCA D\.R\.I\.V\.E\.N | None | None | None | 2026\-11\-26 | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| city | text |
| end\_date | text |
| event\_name | text |
| event\_type | text |
| event\_website | text |
| expected\_attendance | integer |
| first\_seen\_date | text |
| industry | text |
| last\_seen\_date | text |
| open\_to | text |
| organizer | text |
| source\_name | text |
| source\_url | text |
| start\_date | text |
| state | text |
| venue\_name | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["calendar#95;requests"]
  n1["read#95;calendars"]
  n2["validate#95;listings"]
  n3["read#95;event#95;details"]
  n4["screen#95;events"]
  n5["review#95;unclear"]
  n6["confirm#95;unclear"]
  n7["prepare#95;table"]
  n8["upcoming#95;events"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n6 --> n7
  n7 --> n8
```

- **calendar\_requests**: Build bounded listing requests for the upcoming twelve months at the approved convention centers\.
- **read\_calendars**: Read official event calendars in independent venue or month batches and count unreadable pages\.
- **validate\_listings**: Keep dated, distinct listings within the next twelve months and tally unreadable records\.
- **read\_event\_details**: Read the venue’s own event detail where it can verify attendance, audience, website, and event purpose\.
- **screen\_events**: Classify small batches as qualifying professional events, excluded events, or events without enough evidence\.
- **review\_unclear**: Separate listings that need a second check from those already classified\.
- **confirm\_unclear**: Recheck ambiguous event formats and recover usable listings where the calendar provides clear professional evidence\.
- **prepare\_table**: Verify required fields, preserve first\-seen dates, and update last\-seen dates for the upcoming table\.
- **upcoming\_events**: Upcoming verified B2B convention center events, one row per venue, event name, and start date\.

## Version history

- 2026-11-26T13:06:25.694428Z: v1: Build the table and retain official event links published alongside the Tacoma listings\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/us-convention-center-b2b-events-c9c108704516?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
