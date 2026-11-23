# SaaS pricing data: public plan prices for 15 tools

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

SaaS pricing data for public plans from Notion, Slack, Zoom, Canva, HubSpot, Asana, monday\.com, ClickUp, Airtable, Calendly, Loom, Miro, Figma, Linear and Zapier\. Includes monthly and annual\-billing prices in USD\. Export to CSV, Excel or Google Sheets\.

[Get the full dataset for free](https://www.jsonify.com/datasets/weekly-saas-pricing-tracker-8945b8ca58c0?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 2
- Last published: 2026-11-23T08:06:07.277131Z

## The brief

> I need this data: SaaS pricing data for public plans from Notion, Slack, Zoom, Canva, HubSpot, Asana, monday\.com, ClickUp, Airtable, Calendly, Loom, Miro, Figma, Linear and Zapier\. Includes monthly and annual\-billing prices in USD\. Export to CSV, Excel or Google Sheets\.

Summary from the public dataset description.

## SaaS Pricing History / prices

144 total rows · 50 sampled · Output revision 3
Published: 2026-11-23T08:06:07.277131Z · Producing pipeline version: 2

[CSV sample](outputs/e71016acd6f7/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/e71016acd6f7/prices-fe81f9390ffe/sample.json) · [Schema](outputs/e71016acd6f7/prices-fe81f9390ffe/schema.json)

| billing\_unit | captured\_at | headline\_limit | is\_contact\_sales | plan\_name | price\_annual\_billing\_usd\_per\_month | price\_monthly\_billing\_usd | pricing\_page\_url |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Full seat | 2026\-11\-16T22:01:16\.418716\+00:00 | 3,000 AI credits/mo | False | Professional | 16 | 20 | [https://www\.figma\.com/pricing/](<https://www.figma.com/pricing/>) |
| flat | 2026\-11\-23T08:00:21\.860942\+00:00 | Free for up to 2 users\. | False | Free | 0 | 0 | [https://www\.hubspot\.com/pricing/sales](<https://www.hubspot.com/pricing/sales>) |
| per seat / month | 2026\-11\-16T22:01:16\.418716\+00:00 | None | False | Plus | 10 | 12 | [https://www\.notion\.com/pricing](<https://www.notion.com/pricing>) |
| None | 2026\-11\-23T08:00:21\.860942\+00:00 | 25 videos | False | Starter | 0 | 0 | [https://www\.loom\.com/pricing](<https://www.loom.com/pricing>) |
| per member | 2026\-11\-23T08:00:21\.860942\+00:00 | 50 AI credits/member/month | False | Business | 20 | 25 | [https://miro\.com/pricing/](<https://miro.com/pricing/>) |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| billing\_unit | text |
| captured\_at | text |
| headline\_limit | text |
| is\_contact\_sales | boolean |
| plan\_name | text |
| price\_annual\_billing\_usd\_per\_month | double precision |
| price\_monthly\_billing\_usd | double precision |
| pricing\_page\_url | text |
| product | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["sources"]
  n1["read#95;pricing"]
  n2["publish#95;prices"]
  n3["prices"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **sources**: Select the fifteen official public pricing pages and timestamp this weekly capture\.
- **read\_pricing**: Read US dollar plan cards and inspect both billing states; retain evidence and report unreadable pages\.
- **publish\_prices**: Publish only verified plan prices with the capture timestamp; keep skipped\-product reasons in the run record\.
- **prices**: Weekly history of public US dollar SaaS plan prices\.

## Version history

- 2026-11-16T20:51:16.324770Z: v1: Track weekly public SaaS plan prices in USD, preserving monthly and annual billing prices and capture history while reporting unreadable pages\.
- 2026-11-16T22:01:05.302546Z: v2: Expanded verified pricing collection to all fifteen products, with correct billing selections, official currency checks and core\-plan filtering\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/weekly-saas-pricing-tracker-8945b8ca58c0?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
