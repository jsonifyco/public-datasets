# Short Drama Apps: Catalogue, Charts and Coin Prices

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Short drama app data for ReelShort, DramaBox and FreeReels: 71,875 catalogue rows, charts and coin packs\. Published 2 November 2026\.

[Get the full dataset for free](https://www.jsonify.com/datasets/short-drama-charts-and-catalogue-c3bee033d5c1?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 17
- Last published: 2026-11-02T16:00:17.688087Z

## The brief

> I need this data: Short drama app data for ReelShort, DramaBox and FreeReels: 71,875 catalogue rows, charts and coin packs\. Published 2 November 2026\.

Summary from the public dataset description.

## Short\-drama Android weekly data / shows

25,079 total rows · 50 sampled · Output revision 19
Published: 2026-11-02T16:00:17.688087Z · Producing pipeline version: Unknown

[CSV sample](outputs/a969dcc25198/shows-c093955cebfa/sample.csv) · [JSON sample](outputs/a969dcc25198/shows-c093955cebfa/sample.json) · [Schema](outputs/a969dcc25198/shows-c093955cebfa/schema.json)

Curated sample from revision 17; saved 2026-11-02T12:35:48.653978Z. This illustrative snapshot does not refresh with the dataset.

| cover\_url | show\_name | app | genres | release\_date | total\_episodes | free\_episodes | unlock\_model |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [https://v\-img\.crazymaplestudios\.com/v\-images/book\_cover\_batch/200000000000000231/7e5c212e\-d626\-49da\-be4e\-3935b225e42c\.jpg](<https://v-img.crazymaplestudios.com/v-images/book_cover_batch/200000000000000231/7e5c212e-d626-49da-be4e-3935b225e42c.jpg>) | My Stepbrother's Dirty Secret | ReelShort | \["Young Adult"\] | 2025\-05\-14 | 62 | 12 | mixed |
| [https://static\-v1\.mydramawave\.com/vt/prod/cover/fe1a5bf7\-5af0\-4bb8\-a97b\-94000941a118\.jpg?image\_process=quality,85/resize,w\_600/format,webp](<https://static-v1.mydramawave.com/vt/prod/cover/fe1a5bf7-5af0-4bb8-a97b-94000941a118.jpg?image_process=quality,85/resize,w_600/format,webp>) | You Hurt My Daughter, Now You Pay | FreeReels | \["Revenge", "The Comeback"\] | None | 45 | 8 | coins |
| [https://static\-v1\.mydramawave\.com/vt/prod/cover/d8fdce6b\-c99c\-4a84\-ae0e\-b8b98db05b2c\.jpg?image\_process=quality,85/resize,w\_600/format,webp](<https://static-v1.mydramawave.com/vt/prod/cover/d8fdce6b-c99c-4a84-ae0e-b8b98db05b2c.jpg?image_process=quality,85/resize,w_600/format,webp>) | Tiro Certeiro do Amor | FreeReels | \["Final Feliz", "Segunda Chance"\] | None | 59 | 59 | ad\_unlock |
| [https://hwztchapter\.dramaboxdb\.com/data/cppartner/4x1/41x0/410x0/41000107163/41000107163\.jpg?t=1730180925702](<https://hwztchapter.dramaboxdb.com/data/cppartner/4x1/41x0/410x0/41000107163/41000107163.jpg?t=1730180925702>) | Rise of the Rejected | DramaBox | \["Revenge", "Underdog Story", "Son\-in\-Law", "Modern", "Powerful Male Lead"\] | 2024\-10\-29 | 93 | 8 | mixed |
| [https://hwztchapter\.dramaboxdb\.com/data/cppartner/4x1/41x0/410x0/41000103799/41000103799\.jpg?t=1717468154048](<https://hwztchapter.dramaboxdb.com/data/cppartner/4x1/41x0/410x0/41000103799/41000103799.jpg?t=1717468154048>) | Cinta Sejati Melintasi Waktu | DramaBox | \["Bangkitnya Orang Biasa", "Serangan Balik", "Terlahir Kembali", "Intrik Keluarga", "Kekuatan Khusus", "Fantasi"\] | 2024\-06\-04 | 89 | 11 | mixed |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| cover\_url | text |
| show\_name | text |
| app | text |
| genres | jsonb |
| release\_date | text |
| total\_episodes | bigint |
| free\_episodes | bigint |
| unlock\_model | text |
| coins\_per\_episode | bigint |
| coins\_to\_finish | bigint |
| approximate\_views | bigint |
| displayed\_views | text |
| available\_locales | jsonb |
| name\_locale | text |
| views\_locale | text |
| cost\_locales | text |
| chart\_list\_appearances | bigint |
| chart\_appearances | jsonb |
| first\_seen | text |
| last\_seen | text |
| observed\_on | text |
| name\_observed\_on | text |
| views\_observed\_on | text |
| cost\_observed\_on | text |
| cost\_note | text |
| views\_note | text |
| data\_note | text |
| conflicting\_cost\_observations | boolean |

## Short\-drama Android weekly data / charts

13,247 total rows · 50 sampled · Output revision 19
Published: 2026-11-02T16:00:17.688087Z · Producing pipeline version: Unknown

[CSV sample](outputs/a969dcc25198/charts-38edf99fd464/sample.csv) · [JSON sample](outputs/a969dcc25198/charts-38edf99fd464/sample.json) · [Schema](outputs/a969dcc25198/charts-38edf99fd464/schema.json)

Curated sample from revision 15; saved 2026-10-31T15:58:11.497079Z. This illustrative snapshot does not refresh with the dataset.

| app | title | rank | run\_date | country | rail\_raw | view\_basis |
| --- | --- | --- | --- | --- | --- | --- |
| reelshort | Mated to My Sworn Enemy | 1 | 2026\-10\-26 | US | Rise to Power | locale\-based; not storefront\-verified |
| freereels | The Rise of the Lycan Queen | 1 | 2026\-10\-26 | US | RANKING / Annually | locale\-based; not storefront\-verified |
| freereels | Lycan King: Make the Betrayer Kneel | 1 | 2026\-10\-26 | US | POPULAR | locale\-based; not storefront\-verified |
| reelshort | Worth the Chase | 1 | 2026\-10\-25 | GB | Coming Soon | locale\-based; not storefront\-verified |
| dramabox | I'm Nothing but a Mortal \(DUBBED\) | 1 | 2026\-10\-26 | US | VIP | locale\-based; not storefront\-verified |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| app | text |
| title | text |
| rank | integer |
| run\_date | text |
| country | text |
| rail\_raw | text |
| view\_basis | text |

## Short\-drama Android weekly data / coin\_packs

60 total rows · 10 sampled · Output revision 19
Published: 2026-11-02T16:00:17.688087Z · Producing pipeline version: Unknown

[CSV sample](outputs/a969dcc25198/coin-packs-44368b8d70e4/sample.csv) · [JSON sample](outputs/a969dcc25198/coin-packs-44368b8d70e4/sample.json) · [Schema](outputs/a969dcc25198/coin-packs-44368b8d70e4/schema.json)

Curated sample from revision 15; saved 2026-10-31T15:58:16.175622Z. This illustrative snapshot does not refresh with the dataset.

| app | run\_date | bonus\_coins | country | currency | pack\_coins | pack\_type | price\_local |
| --- | --- | --- | --- | --- | --- | --- | --- |
| reelshort | 2026\-10\-26 | 0 | BR | BRL | 100 | one\_off | 5\.49 |
| reelshort | 2026\-10\-26 | 15 | US | USD | 300 | one\_off | 2\.99 |
| reelshort | 2026\-10\-26 | 15 | GB | GBP | 300 | one\_off | 2\.69 |
| reelshort | 2026\-10\-26 | 80 | DE | EUR | 800 | one\_off | 7\.99 |
| reelshort | 2026\-10\-26 | 100 | US | USD | 1000 | one\_off | 9\.99 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| app | text |
| run\_date | text |
| bonus\_coins | integer |
| country | text |
| currency | text |
| pack\_coins | integer |
| pack\_type | text |
| price\_local | double precision |
| price\_usd | double precision |
| source\_url | text |

## Short\-drama Android weekly data / economics

71,875 total rows · 50 sampled · Output revision 19
Published: 2026-11-02T16:00:17.688087Z · Producing pipeline version: Unknown

[CSV sample](outputs/a969dcc25198/economics-5e9ad751b5e6/sample.csv) · [JSON sample](outputs/a969dcc25198/economics-5e9ad751b5e6/sample.json) · [Schema](outputs/a969dcc25198/economics-5e9ad751b5e6/schema.json)

| app | title | run\_date | coin\_price\_per\_episode | conflict | cost\_to\_finish\_coins | economics\_status | free\_episodes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| reelshort | Kultivasi Mudah Berkat Menempa Artefak | 2026\-10\-26 | 60 | False | 3600 | coin requirement observed; cash cost unverified | 9 |
| reelshort | American Hunt \[Original\] | 2026\-11\-02 | 0 | False | 0 | coin requirement observed; cash cost unverified | 1 |
| reelshort | Die vermisste Kochkönigin: Lass den Ex betteln | 2026\-11\-02 | 60 | False | 2100 | coin requirement observed; cash cost unverified | 19 |
| freereels | Der Ausbruch | 2026\-10\-25 | 60 | False | 1920 | coin requirement observed; cash cost unverified | 4 |
| dramabox | He Was Never Their ATM | 2026\-10\-26 | 50 | False | 2100 | coin requirement observed; cash cost unverified | 1 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| app | text |
| title | text |
| run\_date | text |
| coin\_price\_per\_episode | integer |
| conflict | boolean |
| cost\_to\_finish\_coins | integer |
| economics\_status | text |
| free\_episodes | integer |
| observations | jsonb |
| observed\_locales | text |
| row\_key | text |
| title\_id | text |
| view\_basis | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["previous#95;run#95;notes"]
  n1["previous#95;coin#95;packs"]
  n2["previous#95;economics"]
  n3["previous#95;charts"]
  n4["previous#95;catalogue"]
  n5["previous#95;localisations"]
  n6["markets"]
  n7["select#95;markets"]
  n8["seeds"]
  n9["stores"]
  n10["navigation#95;jobs"]
  n11["browse"]
  n12["detail#95;jobs"]
  n13["details"]
  n14["assemble"]
  n15["outputs"]
  n16["chart#95;records"]
  n17["charts"]
  n18["catalogue#95;records"]
  n19["catalogue"]
  n20["pack#95;records"]
  n21["coin#95;packs"]
  n22["note#95;records"]
  n23["run#95;notes"]
  n24["economic#95;records"]
  n25["economics"]
  n26["localisation#95;records"]
  n27["localisations"]
  n7 --> n8
  n8 --> n9
  n9 --> n10
  n10 --> n11
  n11 --> n12
  n12 --> n13
  n13 --> n14
  n14 --> n15
  n16 --> n17
  n18 --> n19
  n20 --> n21
  n22 --> n23
  n24 --> n25
  n26 --> n27
  n0 --> n7
  n1 --> n7
  n2 --> n7
  n3 --> n7
  n4 --> n7
  n5 --> n7
  n6 --> n7
  n15 --> n18
  n15 --> n16
  n15 --> n20
  n15 --> n24
  n15 --> n26
  n15 --> n22
  n6 --> n7
  n4 --> n12
  n2 --> n12
  n5 --> n12
  n4 --> n14
  n3 --> n14
  n2 --> n14
  n5 --> n14
  n0 --> n14
```

- **previous\_run\_notes**: Previously published run\_notes history\.
- **previous\_coin\_packs**: Previously published coin\_packs history\.
- **previous\_economics**: Previously published economics history\.
- **previous\_charts**: Previously published chart history for vanished and newly discovered rails\.
- **previous\_catalogue**: Previously published catalogue history for first\-seen dates and count comparisons\.
- **previous\_localisations**: Previously published locale strings used to reconstruct saved observations without multiplying metadata\.
- **markets**: Android apps and locale views included in every weekly snapshot\.
- **select\_markets**: Select the requested app and locale views and record the actual UTC observation date\.
- **seeds**: Read all displayed Android home tabs and identify catalogue or genre navigation\.
- **stores**: Observe web\-store prices through country\-routed connections; record unavailable storefronts explicitly\.
- **navigation\_jobs**: Keep every displayed title and schedule the finite catalogue or genre traversals\.
- **browse**: Follow category or genre pages until the Android source explicitly reports exhaustion\.
- **detail\_jobs**: Deduplicate the union of home rails and all completed catalogue or genre results\.
- **details**: Read episode counts, free boundaries, genre tags and coin quotes without confirming payment\.
- **assemble**: Validate the weekly snapshot, preserve first\-seen dates and record rail and catalogue changes\.
- **outputs**: Send each validated record to its canonical public worksheet\.
- **chart\_records**: Keep only the canonical chart columns\.
- **charts**: Weekly ranked Android home rails by app and locale\.
- **catalogue\_records**: Keep title and episode metadata; coin requirements are published separately\.
- **catalogue**: Canonical title metadata without repeated country rows\.
- **pack\_records**: Keep only the canonical coin pack columns\.
- **coin\_packs**: Available web coin pack prices observed through country\-routed connections\.
- **note\_records**: Keep the coverage counts and changes for each app and locale\.
- **run\_notes**: Coverage counts, new or missing rails, and catalogue\-change flags\.
- **economic\_records**: Keep one coin\-requirement observation per app and title, flagging conflicts between locale views\.
- **economics**: Title coin requirements without unsupported country pricing\.
- **localisation\_records**: Keep titles, genre labels and other display strings at their actual locale grain\.
- **localisations**: Localised title strings and genre labels, separated from shared metadata\.

## Version history

- 2026-10-25T08:53:14.669364Z: v1: Collects weekly Android charts, title economics and coin packs across all three apps and five labelled locale views\. Includes fully free DramaBox titles and leaves unverified prices blank\.
- 2026-10-25T09:22:37.692250Z: v2: Recognizes DramaBox subscription\-only titles and leaves their coin costs blank, allowing collection to continue without inventing prices\.
- 2026-10-25T09:43:08.500026Z: v3: Recover a looping ReelShort catalogue by restarting once in a fresh logged\-out session while retaining all titles already found\.
- 2026-10-25T10:45:41.839062Z: v4: Read interactive ReelShort episode lists and their locked\-episode coin quotes alongside standard titles\.
- 2026-10-25T12:13:04.264402Z: v5: Retain confirmed upcoming FreeReels titles with announced metadata and blank unavailable episode access and costs\.
- 2026-10-25T13:48:17.384439Z: v6: Recognizes fully free ReelShort titles from their complete unlocked episode list, avoiding a false missing\-price failure\.
- 2026-10-25T14:44:46.168179Z: v7: Handles DramaBox titles whose available episodes are all free, checking the last episode before recording zero coin cost\.
- 2026-10-25T15:03:09.560101Z: v8: Handles misleading ReelShort interactive lock flags by excluding trailers and verifying every actual episode before marking an unpaid title free\.
- 2026-10-25T17:56:22.649973Z: v9: Confirmed text novels remain in charts but are excluded from the episode catalogue, with exclusions counted in run notes\.
- 2026-10-25T18:11:50.551448Z: v10: Confirms novels from their own Android metadata so titles no longer visible on the home screen can still be kept in charts only\.
- 2026-10-25T21:23:07.458201Z: v11: Retains ReelShort titles explicitly announced as coming soon, leaving unavailable episode access and costs blank\.
- 2026-10-26T09:50:00.234530Z: v12: Individual title failures now keep readable details and leave missing cells blank, with gaps recorded for later refreshes\. Fixed historical chart comparisons when saved ranks are read as text\.
- 2026-10-26T18:01:10.089020Z: v13: Separates home charts from expanded rankings, corrects observation dates and publishes coin requirements once per title\. Adds observed country web coin prices and reconciles DramaBox web recommendations by title identifier\.
- 2026-10-26T18:58:14.606322Z: v14: Removes empty and missing\-rail placeholders from chart positions\. Compares catalogue enumeration with the previous collection day and flags retained records with incomplete title details\.
- 2026-10-26T19:52:47.995725Z: v15: Separates shared title metadata from locale strings\. Moves free\-episode boundaries into economics with dated observations and explicit conflicts, and rereads unresolved discrepancies\.
- 2026-10-26T20:02:47.484826Z: v16: Adds a saved\-history rebuild so the catalogue and localisation split can be applied to existing records without recollecting them\. Preserves dated free\-episode and coin observations and marks conflicts\.
- 2026-11-02T03:05:24.967572Z: v17: ReelShort promotional image cards no longer stop updates\. Ranked titles and playlists keep their existing handling\.

## Recorded repairs

- 2026-10-26T09:37:36.463024Z: temporary blocker
- 2026-11-02T03:01:03.510739Z: no change
- 2026-11-02T03:05:34.048196Z: repaired

[Get the full dataset for free](https://www.jsonify.com/datasets/short-drama-charts-and-catalogue-c3bee033d5c1?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
