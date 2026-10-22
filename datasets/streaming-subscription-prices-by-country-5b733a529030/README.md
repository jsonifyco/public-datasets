# Streaming Subscription Prices by Country: Official Monthly Plans

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Explore source\-supported monthly plan prices for eleven streaming services across a selected country panel, with country verification and unresolved coverage clearly distinguished\.

[Get the full dataset for free](https://www.jsonify.com/datasets/streaming-subscription-prices-by-country-5b733a529030?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 10
- Last published: 2026-10-19T13:30:45.861816Z

## The brief

> I need this data: Explore source\-supported monthly plan prices for eleven streaming services across a selected country panel, with country verification and unresolved coverage clearly distinguished\.

Summary from the public dataset description.

## Streaming subscription prices / prices

859 total rows · 100 sampled · Output revision 8
Published: 2026-10-19T13:30:45.861816Z · Producing pipeline version: 7

[CSV sample](outputs/eb6e054729e9/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/eb6e054729e9/prices-fe81f9390ffe/sample.json) · [Schema](outputs/eb6e054729e9/prices-fe81f9390ffe/schema.json)

| billing\_period | country | country\_evidence | country\_name | currency | features | monthly\_price | notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| month | UY | Requested country route UY; official page locale en\. Source pricing market is not independently confirmed\. | Uruguay | UYU | No ads; complete access to Crunchyroll's library; new episodes shortly after airing in Japan; stream on 1 device at a time; offline viewing\. | 99 | Regular base monthly subscription; no currency conversion\. Price observed but country is not independently confirmed; do not use as a verified country comparison\. |
| month | RO | Official country\-specific pricing URL: [https://www\.skyshowtime\.com/ro/plans](<https://www.skyshowtime.com/ro/plans>) | Romania | EUR | Ad\-free; Full HD; 2 simultaneous screens; up to 30 downloads per month\. May include promotional trailers\. | 6\.99 | Regular base monthly subscription; no currency conversion\. Country established by source\. |
| month | CA | Requested country route CA; official page locale en\. Source pricing market is not independently confirmed\. | Canada | CAD | No ads; complete access to Crunchyroll's library; new episodes shortly after airing in Japan; stream on 4 devices at a time; offline viewing; access to Crunchyroll Game Vault and Crunchyroll Store\. | 13\.49 | Regular base monthly subscription; no currency conversion\. Price observed but country is not independently confirmed; do not use as a verified country comparison\. |
| month | PT | Official country\-specific pricing URL: [https://www\.disneyplus\.com/en\-pt](<https://www.disneyplus.com/en-pt>) | Portugal | EUR | Up to 1080p Full HD and 2 concurrent streams\. All plans include Disney promotions and sponsorship and may include ads before or after playback and in certain content\. | 6\.99 | Regular base monthly subscription; no currency conversion\. Country established by source\. |
| None | BR | None | Brazil | None | None | None | No verifiable normal monthly base plans on this page; No verifiable normal monthly base plans on this page |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| billing\_period | text |
| country | text |
| country\_evidence | text |
| country\_name | text |
| currency | text |
| features | text |
| monthly\_price | double precision |
| notes | text |
| observed\_at | text |
| plan | text |
| price\_evidence | text |
| service | text |
| source\_url | text |
| status | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["previous#95;prices"]
  n1["coverage"]
  n2["panel"]
  n3["prices"]
  n4["validate"]
  n5["prices"]
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n0 --> n2
  n1 --> n2
  n1 --> n2
  n0 --> n2
  n0 --> n4
```

- **previous\_prices**: Saved price snapshot used only when preserve\_previous is enabled; unchanged observations keep their original timestamps\.
- **coverage**: Supplied country, service and distributor targets with original checked\-price and redirect evidence\.
- **panel**: Combine every supplied service and distributor target with the existing major\-service country panel, preserving the original checking notes\.
- **prices**: Find official pricing pages, request the selected country, and collect only source\-supported monthly plans\. Keep unresolved coverage explicit\.
- **validate**: Deduplicate service/country/plan observations and reject a run that found no verified monthly prices\.
- **prices**: Current official country/plan monthly prices, plus explicit unresolved coverage records\.

## Version history

- 2026-10-17T11:25:22.016336Z: v1: Collect current streaming plan prices with source\-country checks, excluding historical launch announcements and retaining ad\-supported variants\.
- 2026-10-17T11:54:32.865851Z: v2: Fix Apple TV country attribution and use the UK pricing page for UK subscriptions\. Reject bare country\-picker labels as proof that prices belong to a market\.
- 2026-10-17T16:40:22.779178Z: v3: Correct UK and New Zealand Apple pricing, preserve the country panel during targeted refreshes, and reject weak or falsely matched country evidence\.
- 2026-10-17T16:48:28.801836Z: v4: Use Brazil's current Prime membership offer instead of obsolete corporate copy, and Sweden's own Apple TV pricing page\. Preserve the rest of the saved country panel during targeted corrections\.
- 2026-10-17T16:54:18.087813Z: v5: Use current Prime subscription pages in the US, UK and India, and stop treating currency\-only Netflix headings as verified country evidence\.
- 2026-10-17T17:10:21.818626Z: v6: Reject mismatched Max country routes and promotional terms as regular pricing sources\. Revalidate saved country\-specific URL claims and refresh Finnish Max from its subscription page\.
- 2026-10-17T17:20:25.785824Z: v7: Respect country restrictions on subscription benefits and stop treating bare country labels as verified pricing evidence\. Refresh affected Apple observations while preserving the rest of the country panel\.
- 2026-10-22T16:13:52.075007Z: v8: Expanded coverage to the supplied countries, services and distributor channels\. Ad\-supported and ad\-free plans now have separate rows, with original checking notes preserved alongside current observations\.
- 2026-10-22T17:41:14.745186Z: v9: Fix handling of long official\-site search results so they do not stop the streaming price refresh\.
- 2026-10-22T17:49:43.489269Z: v10: Fix official\-site search parsing and strengthen rejection of coupon and review sites\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/streaming-subscription-prices-by-country-5b733a529030?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
