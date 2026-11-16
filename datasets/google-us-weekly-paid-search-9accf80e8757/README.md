# Google US Paid Search

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Google US paid search dataset with 577 published rows: 173 text ads and 404 Shopping listings\.

[Get the full dataset for free](https://www.jsonify.com/datasets/google-us-weekly-paid-search-9accf80e8757?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 4
- Last published: 2026-11-16T14:24:19.796937Z

## The brief

> I need this data: Google US paid search dataset with 577 published rows: 173 text ads and 404 Shopping listings\.

Summary from the public dataset description.

## Google US paid search observations / text\_ads

173 total rows · 50 sampled · Output revision 4
Published: 2026-11-16T14:24:19.796937Z · Producing pipeline version: 4

[CSV sample](outputs/53ce068c513e/text-ads-74d560e8a207/sample.csv) · [JSON sample](outputs/53ce068c513e/text-ads-74d560e8a207/sample.json) · [Schema](outputs/53ce068c513e/text-ads-74d560e8a207/schema.json)

| advertiser\_domain | collected\_at | description | display\_url | headline | keyword | position\_block | position\_rank |
| --- | --- | --- | --- | --- | --- | --- | --- |
| flexispot\.com | 2026\-11\-16T14:01:22\.423085\+00:00 | Alternate between sitting and standing to boost productivity and reduce daily\.\.\. | [https://www\.flexispot\.com](<https://www.flexispot.com>) | FlexiSpot Standing Desks \- Black Friday Sale | standing desk | top | 3 |
| onuia\.com | 2026\-11\-16T14:14:04\.082115\+00:00 | Black Friday: the Suite Topper is up to 50% off\. Free worldwide shipping\. Shop now\! Twice the fill of a standard topper, box\-stitched so it keeps its depth\. Shop\.\.\. | [https://www\.onuia\.com](<https://www.onuia.com>) › black\-friday › cloud | Black Friday Topper Deal \- Black Friday: Up To 50% Off | mattress topper | bottom | 1 |
| amazon\.com | 2026\-11\-14T21:46:50\.578576\+00:00 | Capture 4K Front And 1080P Rear Video With STARVIS 2 Imaging And Night Recording\. Shop REDTIGER F7N Touch 4K Dash Cam With Front And Rear Recording On Amazon\. 4K Uhd Resolution\. 128GB Memory Included\. 18 Months\.\.\. | [https://www\.amazon\.com](<https://www.amazon.com>) › redtiger › 4k\-starvis | amazon\.com \| View The 128GB Camera Bundle | dash cam | top | 2 |
| chicagotribune\.com | 2026\-11\-14T21:37:53\.080045\+00:00 | We Compared Deco BE63 Tri\-Band WiFi 7 vs Deco X55 AX3000 3\-Pack vs eero Read more | [https://reviews\.chicagotribune\.com](<https://reviews.chicagotribune.com>) › wifi | 5 Best Mesh WiFi Systems 2026 \- There's One Clear Winner Now | mesh wifi router | top | 1 |
| bose\.com | 2026\-11\-16T14:07:14\.028816\+00:00 | Featuring Classic, Comfortable Design With All\-Day Comfort &amp; Up To 24 Hours Battery Life\. Enjoy A 1 Year Limited Warranty on Select Products From Bose\. | [https://www\.bose\.com](<https://www.bose.com>) › shop › headphones | Bose® Official Site \| $160 Off QC Ultra In Sandstone | noise cancelling headphones | bottom | 2 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| advertiser\_domain | text |
| collected\_at | text |
| description | text |
| display\_url | text |
| headline | text |
| keyword | text |
| position\_block | text |
| position\_rank | bigint |
| sitelinks\_offers\_text | text |

## Google US paid search observations / shopping\_ads

404 total rows · 50 sampled · Output revision 4
Published: 2026-11-16T14:24:19.796937Z · Producing pipeline version: 4

[CSV sample](outputs/53ce068c513e/shopping-ads-21f812a8c390/sample.csv) · [JSON sample](outputs/53ce068c513e/shopping-ads-21f812a8c390/sample.json) · [Schema](outputs/53ce068c513e/shopping-ads-21f812a8c390/schema.json)

| collected\_at | currency | keyword | merchant | original\_price | price | product\_title | rank |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 2026\-11\-14T21:19:58\.249590\+00:00 | USD | air fryer | Kroger | None | 34\.99 | Chefman TurboFry Touch 6\-Quart Easy\-View Air Fryer \- Thanksgiving Essentials | 7 |
| 2026\-11\-14T21:46:39\.759306\+00:00 | USD | carry on luggage | NOBL Travel | None | 289 | Silver Carry On Luggage \- 20\.5" Best Multi Functional Carry On Suitcase with Polycarbonate Shell &amp; Battery Charger with Capacity 35L by NOBL Travel | 1 |
| 2026\-11\-14T21:46:30\.268001\+00:00 | USD | weighted blanket | Bare Home | 92 | 73\.59 | Bare Home Cotton Weighted Blanket, 12 lb, 48"x72", Sand – Glass Bead Weighted Blanket with Stitched Pockets | 8 |
| 2026\-11\-14T21:47:01\.404729\+00:00 | USD | portable power station | UDPower | None | 529\.99 | 1200W Portable power Station for Camping \| 1200W Solar Generator for RV Camping | 8 |
| 2026\-11\-14T21:40:54\.272933\+00:00 | USD | air fryer | Walmart | 70 | 54\.99 | Air Fryer 8 Quart 8qt, 8\-in\-1 Multifunction Cooking Modes, Digital Touch Panel, Easy\-Viewing Window, Max 400 Fast Heat, 1700w, Black | 6 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| collected\_at | text |
| currency | text |
| keyword | text |
| merchant | text |
| original\_price | double precision |
| price | double precision |
| product\_title | text |
| rank | integer |
| rating | double precision |
| review\_count | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["keywords"]
  n1["collect"]
  n2["tables"]
  n3["text#95;ads"]
  n4["shopping#95;ads"]
  n0 --> n1
  n1 --> n2
  n2 --> n4
  n2 --> n3
```

- **keywords**: Use the fixed list of twenty US English search terms\.
- **collect**: Read the first Google US desktop results page and retain only marked paid text and Shopping ads\.
- **tables**: Separate paid text ads from paid Shopping listings\.
- **text\_ads**: One paid text ad per keyword and collection\.
- **shopping\_ads**: One paid Shopping listing per keyword and collection\.

## Version history

- 2026-11-14T21:18:08.531796Z: v1: Create weekly historical Google US paid\-search observations for the twenty requested keywords, with separate text and Shopping tables\.
- 2026-11-14T21:27:20.750584Z: v2: Check a second US desktop search when an ad category is absent, improving keyword coverage while keeping existing observations\.
- 2026-11-14T21:37:27.157497Z: v3: Correct US location handling, collect keywords sequentially, and recover blocked or incomplete captures with a bounded second attempt\.
- 2026-11-16T14:12:27.405556Z: v4: Keep successfully collected ads when checking a second page capture for a missing ad category\.

## Recorded repairs

- 2026-11-16T14:06:09.304962Z: no change
- 2026-11-16T14:06:32.078655Z: repaired
- 2026-11-16T14:09:59.699018Z: no change
- 2026-11-16T14:12:38.704940Z: repaired
- 2026-11-16T14:17:16.483454Z: no change
- 2026-11-16T14:18:57.367948Z: repaired
- 2026-11-16T14:22:20.514671Z: no change
- 2026-11-16T14:22:26.927111Z: repaired
- 2026-11-16T14:24:43.338371Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/google-us-weekly-paid-search-9accf80e8757?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
