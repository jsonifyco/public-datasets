# Chicago Building Permits Data: New Permits Issued Weekly

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Chicago building permits data: permit type, work description, reported cost, fees, address, ward and coordinates for permits issued, updated every week\.

[Get the full dataset for free](https://www.jsonify.com/datasets/chicago-building-permits-e1c447fbcc9c?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 2
- Last published: 2026-11-03T08:00:39.577664Z

## The brief

> I need this data: Chicago building permits data: permit type, work description, reported cost, fees, address, ward and coordinates for permits issued, updated every week\.

Summary from the public dataset description.

## Chicago Building Permits / permits

1,208 total rows · 50 sampled · Output revision 3
Published: 2026-11-03T08:00:39.577664Z · Producing pipeline version: Unknown

[CSV sample](outputs/c9ef3e98e123/permits-f9b6938a67e1/sample.csv) · [JSON sample](outputs/c9ef3e98e123/permits-f9b6938a67e1/sample.json) · [Schema](outputs/c9ef3e98e123/permits-f9b6938a67e1/schema.json)

| permit\_number | permit\_type | review\_type | permit\_status | work\_type | work\_description | application\_start\_date | issue\_date |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 101069539 | PERMIT \- RENOVATION/ALTERATION | STANDARD PLAN REVIEW | ACTIVE | None | SPR 2019: FOUNDATION UNDERPINNING OF EAST WALL FOUNDATION, 5 STORY TYPE 1 CONSTRUCTION TO ADDRESS SETTLEMENT ISSUE\.                                  NO CONCRETE WORK UNDER THIS PERMIT\. | 2025\-05\-21 | 2026\-10\-19 |
| 101077099 | PERMIT \- RENOVATION/ALTERATION | STANDARD PLAN REVIEW | ACTIVE | None | SPR 2019 CBRC \- INTERIOR AND EXTERIOR RENOVATIONS TO AN EXISTING 3 STORY 6 DWELLING UNIT RESIDENCE WITH BASEMENT AND REAR PORCH WITH STAIRS TO CONVERT TO 8 DWELLING UNITS WITH A NEW TRASH ENCLOSURE, 6 UNENCLOSED PARKING SPACES AND 8 BICYCLE SPACES AS PER PLANS\*\*CERTIFIED CORRECTIONS SUBJECT TO FIELD INSPECTIONS &amp; AUDIT \*\* | 2026\-01\-05 | 2026\-10\-19 |
| 101082574 | PERMIT \- RENOVATION/ALTERATION | STANDARD PLAN REVIEW | ACTIVE | None | SPR 2019 CBRC: INTERIOR REMODELING TO ADD A 2\-STOP CHAIR LIFT IN THE EXISTING GRAND BALLROOM\. \(OCC\. GRP: A\-2; CONST\. TYPE: IA\) | 2026\-04\-23 | 2026\-10\-19 |
| 101083551 | PERMIT \- RENOVATION/ALTERATION | STANDARD PLAN REVIEW | ACTIVE | None | SPR 2019 CBC \(STANDARD\) FULL BUILDINGTHE WORK INCLUDES THE INTERIOR REMODELING ON THE FIRST AND SECOND FLOOR \(WINDOW REPLACEMENT &amp; 35 SF LOFT EXTENSION\) OF AN EXISTING 3 STORY MASONRY, SINGLE FAMILY RESIDENCE\.OCCUPANCY GROUP R5TYPE IIIA CONSTRUCTIONNO CHANGE IN ZONING | 2026\-06\-04 | 2026\-10\-19 |
| 101083940 | PERMIT \- RENOVATION/ALTERATION | STANDARD PLAN REVIEW | ACTIVE | None | INTERIOR &amp; EXTERIOR RENOVATIONS TO CONVERT 2ND &amp; 3RD FLOOR \(2\) D\.U\. INTO \(4\) D\.U\. ON MIXED\-USE MULTI\-FAMILY MASONRY BUILDING WITH EXIST\. HAIR SALON GROUND FLOOR \(NO WORK\) &amp; BASEMENT \(III\-A CONS\./ OCCUPANCY R2/B\) | 2026\-06\-01 | 2026\-10\-19 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| permit\_number | text |
| permit\_type | text |
| review\_type | text |
| permit\_status | text |
| work\_type | text |
| work\_description | text |
| application\_start\_date | text |
| issue\_date | text |
| processing\_time\_days | bigint |
| address | text |
| city | text |
| community\_area | bigint |
| ward | bigint |
| reported\_cost\_usd | double precision |
| total\_fee\_usd | double precision |
| residential\_unit\_change | bigint |
| latitude | double precision |
| longitude | double precision |
| source\_url | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["published"]
  n1["discover"]
  n2["collect#95;batches"]
  n3["permits"]
  n1 --> n2
  n2 --> n3
  n0 --> n1
  n0 --> n1
```

- **published**: Already saved permits; used to add only unseen permit numbers\.
- **discover**: Find unseen issued permit numbers and reserve room within the monthly limit\.
- **collect\_batches**: Save batches of up to 100 permits, preserving source values and counting unreadable or privacy\-sensitive records\.
- **permits**: One row per issued Chicago building permit; no contact columns\.

## Version history

- 2026-11-03T07:58:52.490899Z: v1: Add a private Chicago building permit collection with source\-matched fields, new\-permit\-only updates, batch saving and a monthly limit\. Scheduling remains off\.
- 2026-11-03T08:09:06.157277Z: v2: Use the latest saved permit issue date as the strict cutoff for future updates, preserving the existing fields, exclusions and monthly cap\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/chicago-building-permits-e1c447fbcc9c?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
