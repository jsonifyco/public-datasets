# Lisbon Coffee Brands at Street Venues

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Dataset with 810 rows across published tables, including 405 venue records with observed coffee brands, listing details, and photo evidence fields\.

[Get the full dataset for free](https://www.jsonify.com/datasets/coffee-brand-on-the-street-lisbon-poc-823f5bfb06bb?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 13
- Last published: 2026-11-04T01:16:15.887580Z

## The brief

> I need this data: Dataset with 810 rows across published tables, including 405 venue records with observed coffee brands, listing details, and photo evidence fields\.

Summary from the public dataset description.

## Coffee brand on the street — Lisbon PoC / raw\_observations

405 total rows · 50 sampled · Output revision 6
Published: 2026-11-04T00:19:09.994141Z · Producing pipeline version: 10

[CSV sample](outputs/aa237b99a777/raw-observations-f951fd3fe3cc/sample.csv) · [JSON sample](outputs/aa237b99a777/raw-observations-f951fd3fe3cc/sample.json) · [Schema](outputs/aa237b99a777/raw-observations-f951fd3fe3cc/schema.json)

| venue\_name | address | category | rating | review\_count | maps\_url | latitude | longitude |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Copenhagen Coffee Lab \- Campo de Ourique | R\. Coelho da Rocha 108, 1350\-007, Lisbon, Portugal | Coffee shop | 3\.7 | 149 | [https://www\.google\.com/maps/place/?q=place\_id:ChIJn0s4myIzGQ0RmrgYP\_9sVBE](<https://www.google.com/maps/place/?q=place_id:ChIJn0s4myIzGQ0RmrgYP_9sVBE>) | 38\.7165684 | \-9\.1670675 |
| Brasa Lisboa | R\. Castelo Branco Saraiva 95, Lisbon, 1170\-085, PT | Barbecue restaurant | 4\.9 | 346 | [https://www\.google\.com/maps/place/?q=place\_id:ChIJGfiKVQAzGQ0Rox7\-YPdLb9g](<https://www.google.com/maps/place/?q=place_id:ChIJGfiKVQAzGQ0Rox7-YPdLb9g>) | 38\.7263421 | \-9\.1241124 |
| Focaccia in Giro | Focaccia in Giro, Campo de Santa Clara 141, Lisbon, 1100\-474, PT | Ligurian restaurant, Brunch restaurant, Italian restaurant | 4\.7 | 626 | [https://www\.google\.com/maps/place/?q=place\_id:ChIJl9UL64ozGQ0R4EYkgxv\-cr0](<https://www.google.com/maps/place/?q=place_id:ChIJl9UL64ozGQ0R4EYkgxv-cr0>) | 38\.7160242 | \-9\.1251684 |
| Restaurante Peão\. | R\. Coelho da Rocha 63, 1350\-302, Lisbon, Portugal | Portuguese restaurant | 4\.3 | 69 | [https://www\.google\.com/maps/place/?q=place\_id:ChIJe0c5z24zGQ0Rfp1VJtw8FLE](<https://www.google.com/maps/place/?q=place_id:ChIJe0c5z24zGQ0Rfp1VJtw8FLE>) | 38\.716468 | \-9\.1641637 |
| Há Tapas no Mercado | PVP9\+232 Mercado de Arroios, R\. Ângela Pinto, Lisbon, 1900\-067, PT | Tapas restaurant | 4\.9 | 1346 | [https://www\.google\.com/maps/place/?q=place\_id:ChIJPxmrfL0zGQ0Rzisx5fU4fHI](<https://www.google.com/maps/place/?q=place_id:ChIJPxmrfL0zGQ0Rzisx5fU4fHI>) | 38\.7349939 | \-9\.1324003 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| venue\_name | text |
| address | text |
| category | text |
| rating | double precision |
| review\_count | integer |
| maps\_url | text |
| latitude | double precision |
| longitude | double precision |
| place\_id | text |
| scope | text |
| distance\_m | integer |
| baseline\_brand | text |
| baseline\_audit\_status | text |
| baseline\_audit\_notes | text |
| batch\_coverage | jsonb |
| latest\_batch\_coverage | jsonb |
| gallery\_candidate\_count | integer |
| source\_errors | jsonb |
| center\_name | text |
| center\_latitude | double precision |
| center\_longitude | double precision |
| center\_maps\_url | text |
| center\_source\_url | text |
| coverage\_radius\_m | integer |
| supplier\_status | text |
| observation\_limitations | text |
| coordinate\_source | text |
| coffee\_brand | text |
| confidence | text |
| brand\_text | text |
| evidence\_types | text |
| supporting\_photos | integer |
| conflicting\_brands | text |
| best\_photo\_url | text |
| photos\_checked | integer |
| photo\_status | text |
| photo\_evidence | jsonb |
| source\_summary | text |
| observed\_at | text |
| validation\_method | text |
| baseline\_supporting\_photos | integer |
| direct\_audit\_scope | text |
| direct\_audit\_status | text |
| reviewed\_photo\_notes | jsonb |
| correction\_checked\_at | text |
| direct\_photo\_audit | jsonb |
| archived\_photo\_evidence | jsonb |
| supplemental\_source\_note | text |

## cafe\_coffee\_brand\_lisbon / cafe\_coffee\_brand\_lisbon

405 total rows · 50 sampled · Output revision 20
Published: 2026-11-04T01:16:15.887580Z · Producing pipeline version: 13

[CSV sample](outputs/b39c541a129d/cafe-coffee-brand-lisbon-bbe279b222b1/sample.csv) · [JSON sample](outputs/b39c541a129d/cafe-coffee-brand-lisbon-bbe279b222b1/sample.json) · [Schema](outputs/b39c541a129d/cafe-coffee-brand-lisbon-bbe279b222b1/schema.json)

| address | area | audit | branding\_status | category | confidence | conflicting\_brands | distance\_from\_beato\_m |
| --- | --- | --- | --- | --- | --- | --- | --- |
| R\. Passos Manuel 100A, Lisbon, 1150\-258, PT | Beato | \{"scope": "Beato radius sample", "rating": 4\.3, "address": "… | unclear\_photo | Portuguese restaurant | low | None | 2562 |
| R\. de Dona Estefânia 131, Lisbon, 1000\-156, PT | Beato | \{"scope": "Beato radius sample", "rating": 4\.2, "address": "… | branding\_observed | Hamburger restaurant | medium | None | 2926 |
| R\. Actriz Palmira Bastos 43, Lisbon, 1950\-261, PT | Beato | \{"scope": "Beato radius sample", "rating": 4\.3, "address": "… | branding\_observed | Pastry shop, Bakery, Beer store, Cheese shop, Coffee shop, Cafe, Sandwich shop, Wine bar | medium | None | 2658 |
| R\. Fernando Palha 39, Lisbon, 1950\-087, PT | Beato | \{"scope": "Beato radius sample", "rating": 4\.3, "address": "… | no\_visible\_branding | Restaurant | low | None | 1790 |
| Praça Francisco Sá Carneiro 7 D, Lisbon, 1000\-159, PT | Beato | \{"scope": "Beato radius sample", "rating": 4\.2, "address": "… | unclear\_photo | Pastry shop, Cake shop | low | None | 2683 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| address | text |
| area | text |
| audit | jsonb |
| branding\_status | text |
| category | text |
| confidence | text |
| conflicting\_brands | text |
| distance\_from\_beato\_m | integer |
| evidence\_note | text |
| evidence\_photo\_url | text |
| evidence\_seen | jsonb |
| last\_checked\_at | text |
| maps\_url | text |
| named\_roaster | text |
| observed\_coffee\_brand | text |
| photo\_captured\_at | text |
| photos\_checked | integer |
| source\_published\_at | text |
| source\_url | text |
| supporting\_photos | integer |
| venue\_name | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["reviewed#95;supplemental#95;photos"]
  n1["reviewed#95;photo#95;notes"]
  n2["reinspect#95;venue#95;ids"]
  n3["confirmed#95;photo#95;observations"]
  n4["saved#95;observations"]
  n5["previous#95;observations"]
  n6["verified#95;instagram#95;posts"]
  n7["photo#95;audit"]
  n8["demo#95;center"]
  n9["baseline#95;evidence"]
  n10["search#95;plan"]
  n11["maps#95;search"]
  n12["qualify#95;venues"]
  n13["collect#95;photos"]
  n14["inspect#95;photos"]
  n15["verify#95;sample"]
  n16["reinspect#95;saved#95;photos"]
  n17["venue#95;profiles"]
  n18["cafe#95;coffee#95;brand#95;lisbon"]
  n10 --> n11
  n11 --> n12
  n12 --> n13
  n13 --> n14
  n14 --> n15
  n15 --> n16
  n16 --> n17
  n17 --> n18
  n0 --> n10
  n1 --> n10
  n2 --> n10
  n3 --> n10
  n4 --> n10
  n5 --> n10
  n6 --> n10
  n7 --> n10
  n8 --> n10
  n9 --> n10
  n8 --> n10
  n7 --> n10
  n9 --> n12
  n5 --> n12
  n6 --> n13
  n4 --> n15
  n7 --> n16
  n2 --> n16
  n3 --> n17
  n7 --> n17
  n1 --> n17
  n0 --> n17
```

- **reviewed\_supplemental\_photos**: Public source photos independently matched to exact venue and inspected for readable branding\.
- **reviewed\_photo\_notes**: Exact source\-photo notes distinguishing evidence strength and named roaster from product brand\.
- **reinspect\_venue\_ids**: Exact saved venue identities selected for deeper small\-logo inspection, without new venue discovery\.
- **confirmed\_photo\_observations**: Human\-confirmed photo observations with exact venue, source URL and content hash; retain earlier automated readings\.
- **saved\_observations**: Optional exact saved observations for schema\-only republication without recollecting public sources\.
- **previous\_observations**: Exact prior published observations retained without re\-fetching during staged expansion; bind the last completed dataset version\.
- **verified\_instagram\_posts**: Public posts independently matched to an exact venue by full address and visible branding; Instagram coordinates are not used\.
- **photo\_audit**: Independent direct\-pixel audit of the original 24 photos, keyed by content hash; does not assert current supply contracts\.
- **demo\_center**: Beato campus entrance matched to the official campus address and exact Maps listing\.
- **baseline\_evidence**: Preserved published Campo de Ourique version\-one rows, exact source coordinates, original photos and independent photo audit\.
- **search\_plan**: Prepare category searches near the verified Beato entrance and retain the immutable Campo de Ourique baseline\.
- **maps\_search**: Read public Maps places around Beato, retaining source coordinates, identities, ratings and photo links\.
- **qualify\_venues**: Measure source coordinates from the Beato center, keep the nearest in\-radius food venues, and preserve baseline records with explicit audit status\.
- **collect\_photos**: Add public review\-gallery photos and the verified Praça Beato bakery gallery, preferring exterior and coffee captions without retaining reviewer identities\.
- **inspect\_photos**: Inspect up to ten unique photos, perform two blind visual readings for every photo, and retain exact photo\-level evidence, failures and dates\.
- **verify\_sample**: Check unique venue identities, preserved baseline fields and actual usable photo evidence before publication\.
- **reinspect\_saved\_photos**: Reinspect deliberately selected unknown venues using saved full\-resolution photos, including small background logos and meal\-scene saucers; preserve prior readings\.
- **venue\_profiles**: Publish concise typed venue profiles with one evidence photo, distinct source and capture dates, and complete raw evidence under an expandable audit object\.
- **cafe\_coffee\_brand\_lisbon**: Concise venue profiles of historical coffee branding, with complete raw source and audit evidence in the expandable audit field\.

## Version history

- 2026-11-03T20:02:37.109536Z: v1: Created a Campo de Ourique coffee\-brand sample with public Maps venue details and visual photo evidence\.
- 2026-11-03T20:43:46.790395Z: v2: Adds deeper photo evidence and a bounded Beato sample with map coordinates\. Separates unresolved photo checks from images with no visible brand and preserves the original Campo de Ourique audit\.
- 2026-11-03T21:00:19.365792Z: v3: Adds verified public Instagram cup photos to the Beato evidence and keeps stable post links alongside expiring image links\. Preserves the ten\-photo limit and source\-backed map coordinates\.
- 2026-11-03T21:20:33.049144Z: v4: Venue records now show one canonical evidence photo, specific observed brands and separate source/capture dates\. Complete original records remain in expandable audit evidence\.
- 2026-11-03T22:10:14.477817Z: v5: Adds nearby venues in manageable batches while keeping all saved venues and photo evidence\. Tracks remaining discoveries and independent photo\-audit status\.
- 2026-11-03T23:12:24.086655Z: v6: Corrects Leitaria Tejo’s missed Delta branding and supports targeted small\-logo reinspection with independent audit safeguards\.
- 2026-11-03T23:22:38.212324Z: v7: Adds precise photo evidence notes and named roaster, preserves multiple brands, and incorporates two verified Baobá Instagram photos\.
- 2026-11-03T23:46:01.710608Z: v8: Corrected seven independently inspected missed coffee\-brand observations, preserving exact photos and qualifications\. All expanded venues remain included\.
- 2026-11-03T23:55:10.056595Z: v9: Added independent qualifications for 26 new positive photos and normalized documented brand spellings, preserving original baseline evidence\.
- 2026-11-04T00:07:32.525254Z: v10: Every new photo now receives two independent readings, including when the first sees no brand\. Small logos on meal tableware and promotional objects receive explicit attention while uncertain readings remain unknown\.
- 2026-11-04T00:15:15.487754Z: v11: Added personally verified branding for thirteen previously unknown venues, retaining exact evidence and qualifications for sugar sachets, furniture, packaging and food saucers\.
- 2026-11-04T00:59:58.196043Z: v12: Added personally verified branding at five existing venues, including mixed historical branding at Central do Areeiro and Monte Novo\.
- 2026-11-04T01:15:22.126212Z: v13: Added Camelo at Doce Mila and qualified the additional historical branding at Os Brasileiros and Café Tradicional\. The ambiguous Vitta Roma photo remains unaccepted\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/coffee-brand-on-the-street-lisbon-poc-823f5bfb06bb?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
