# Portugal Food and Drink Venues with Photos

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Food and drink venue listings from Google Maps, with venue details and photo\-related fields\. The published venues table contains 12 rows; photo details may be available where provided\.

[Get the full dataset for free](https://www.jsonify.com/datasets/portugal-food-and-drink-venues-with-photos-9943f1952c47?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 6
- Last published: 2026-11-06T15:06:13.370601Z

## The brief

> I need this data: Food and drink venue listings from Google Maps, with venue details and photo\-related fields\. The published venues table contains 12 rows; photo details may be available where provided\.

Summary from the public dataset description.

## Portugal food and drink venues / venues

12 total rows · 10 sampled · Output revision 6
Published: 2026-11-06T15:06:13.370601Z · Producing pipeline version: Unknown

[CSV sample](outputs/11031619bf36/venues-bc318ecbb352/sample.csv) · [JSON sample](outputs/11031619bf36/venues-bc318ecbb352/sample.json) · [Schema](outputs/11031619bf36/venues-bc318ecbb352/schema.json)

| address | amenities | categories | collected\_at | collected\_review\_count | collection\_area | credit\_cards\_accepted | description |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Taberna do São Paulo, Rua de S\. Paulo 196, 1200\-109 Lisboa | \[\{"name": "Assisted listening d… | \["Portuguese restaurant"\] | 2026\-11\-06T15:04:45\.203142\+00:00 | 5 | Lisbon sample | None | None |
| Daily Dose Lisboa \(Speciality Coffee\), R\. do Alecrim 26 D, 1200\-018 Lisboa | \[\] | \["Coffee shop", "Bakery", "Breakfast restaurant", "Brunch restaurant", "Restaurant", "Tea house"\] | 2026\-11\-06T15:04:43\.320641\+00:00 | 5 | Lisbon sample | None | None |
| Noitada Bar &amp; Tapas, R\. Nova do Carvalho 7, 1200\-161 Lisboa | \[\{"name": "Wheelchair\-accessible entrance", "group": "Accessibility", "enabled": true}, \{"name": "Wheelchair\-accessible seating", "group": "Accessibility", "enabled": true}\] | \["Bar", "Cocktail bar", "Gastropub", "Lounge bar", "Night club", "Restaurant"\] | 2026\-11\-06T15:04:43\.798085\+00:00 | 5 | Lisbon sample | None | None |
| Santa Marta, R\. de Santa Marta 61, 1150\-294 Lisboa | \[\{"name": "Wheelchair\-accessibl… | \["Mediterranean restaurant", "Restaurant"\] | 2026\-11\-06T15:04:45\.203142\+00:00 | 5 | Lisbon sample | None | None |
| Episode \- coffee place, R\. Artilharia 1 44B, 1250\-040 Lisboa | \[\] | \["Coffee shop"\] | 2026\-11\-06T15:04:43\.320641\+00:00 | 5 | Lisbon sample | None | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| address | text |
| amenities | jsonb |
| categories | jsonb |
| collected\_at | text |
| collected\_review\_count | bigint |
| collection\_area | text |
| credit\_cards\_accepted | text |
| description | text |
| first\_collected\_at | text |
| geographic\_coverage\_complete | boolean |
| google\_maps\_url | text |
| latitude | double precision |
| longitude | double precision |
| normalized\_category | text |
| normalized\_name | text |
| open\_state | text |
| opening\_hours | jsonb |
| phone | text |
| photo\_collection\_status | text |
| photo\_count | bigint |
| photo\_coverage\_complete | boolean |
| photos | jsonb |
| price\_range | text |
| primary\_category | text |
| review\_collection\_status | text |
| review\_count | bigint |
| review\_coverage\_complete | boolean |
| review\_media | jsonb |
| review\_rating | text |
| reviews | jsonb |
| reviews\_collected\_at | text |
| reviews\_link | text |
| service\_links | jsonb |
| timezone | text |
| title | text |
| venue\_id | text |
| videos | jsonb |
| website | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["collected#95;venues"]
  n1["plan#95;searches"]
  n2["search#95;level#95;0"]
  n3["search#95;level#95;1"]
  n4["search#95;level#95;2"]
  n5["search#95;level#95;3"]
  n6["search#95;level#95;4"]
  n7["venues"]
  n8["venue#95;galleries"]
  n9["photo#95;metadata"]
  n10["final#95;venues"]
  n11["venue#95;reviews"]
  n12["review#95;photo#95;metadata"]
  n13["join#95;review#95;media"]
  n14["prepare#95;listing#95;photos"]
  n15["listing#95;photo#95;metadata"]
  n16["plan#95;listing#95;comparisons"]
  n17["compare#95;listing#95;photos"]
  n18["merge#95;listing#95;photos"]
  n19["clean#95;venues"]
  n20["venues"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n6 --> n7
  n7 --> n8
  n8 --> n9
  n9 --> n10
  n10 --> n11
  n11 --> n12
  n12 --> n13
  n13 --> n14
  n14 --> n15
  n15 --> n16
  n16 --> n17
  n17 --> n18
  n18 --> n19
  n19 --> n20
  n0 --> n1
  n0 --> n10
```

- **collected\_venues**: Optional previously collected venue rows to reshape without collecting again\.
- **plan\_searches**: Prepare Lisbon sample searches or a land\-only Portugal grid covering the mainland and islands\.
- **search\_level\_0**: Search each initial grid cell and category, saving completed searches so failures can resume\.
- **search\_level\_1**: Search the first set of smaller cells where the parent searches were crowded\.
- **search\_level\_2**: Search second\-level dense\-area cells while retaining all completed venue observations\.
- **search\_level\_3**: Search third\-level dense\-area cells, independently checkpointing each search\.
- **search\_level\_4**: Search the final dense\-area cells and retain any remaining coverage limitations\.
- **venues**: Merge exact Google place identities, union their photo URLs, and keep every available Maps field in one venues table\.
- **venue\_galleries**: Save each venue’s public gallery and retain its available photos and videos without requesting sign\-in\.
- **photo\_metadata**: Save each photo’s full\-size link, source date, caption, dimensions and attribution separately so completed photos survive a failure\.
- **final\_venues**: Join photos back to their exact venue and verify that every discovered public photo has metadata\.
- **venue\_reviews**: Collect each venue’s public review selection, including text, author, rating and dates, and checkpoint completed venues\.
- **review\_photo\_metadata**: Save newly discovered review photos individually at original size\.
- **join\_review\_media**: Merge review photos once per identity and verify every attached photo was saved\.
- **prepare\_listing\_photos**: Retain every distinct listing\-photo source for comparison with the collected gallery and review photos\.
- **listing\_photo\_metadata**: Read each listing image at original size and save its real dimensions and visual signature independently\.
- **plan\_listing\_comparisons**: Compare listing photos only with gallery or review originals of the same dimensions, preserving uncertain matches\.
- **compare\_listing\_photos**: Check candidate duplicate photos using their original image pixels, saving each comparison separately\.
- **merge\_listing\_photos**: Keep genuinely additional listing originals, dropping only pixel\-matched copies already in the gallery or reviews\.
- **clean\_venues**: Remove duplicated source payloads and thumbnail variants, keeping shallow venue fields and original\-size photos\.
- **venues**: One venue per row, with simple fields and a single list of original\-size photo records\.

## Version history

- 2026-11-06T12:32:00.069130Z: v1: Creates a Lisbon sample of food and drink venues with full\-size photo links, dates, captions and attribution\. Completed searches, galleries and photos are saved for recovery, with Portugal\-wide geographic controls ready for later use\.
- 2026-11-06T13:30:03.883515Z: v2: Replaces duplicate raw payloads and thumbnails with simple venue fields and flat photo/video records\. Keeps original\-size images, largest videos and available dates, dimensions, captions and attribution\.
- 2026-11-06T14:00:31.233505Z: v3: Adds individual public reviews with text, rating, author and dates as flat records\. Each venue’s review collection is resumable, and limited review coverage is labelled explicitly\.
- 2026-11-06T14:15:03.935046Z: v4: Added photos attached to public reviews, numeric latitude and longitude, and normalized venue names and categories\.
- 2026-11-06T15:03:29.118536Z: v5: Categories are now a simple list of values, with the primary category in its own field\.
- 2026-11-06T16:57:02.218400Z: v6: Collect across Lisbon with adaptive searches, expanded reviews and original\-size listing photos\. Record and skip individual venue failures throughout normalization and enrichment\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/portugal-food-and-drink-venues-with-photos-9943f1952c47?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
