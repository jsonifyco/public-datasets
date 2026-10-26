# Global Short\-Drama Reels Catalogue and Coin Packs

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Weekly charts, catalogue and coin\-pack data for three short\-drama apps across five labelled locale views\.

[Get the full dataset for free](https://www.jsonify.com/datasets/short-drama-charts-and-catalogue-c3bee033d5c1?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 16
- Last published: 2026-10-26T20:04:36.761315Z

## The brief

> I need this data: Weekly charts, catalogue and coin\-pack data for three short\-drama apps across five labelled locale views\.

Summary from the public dataset description.

## Short\-drama Android weekly data / catalogue

47,393 total rows · 500 sampled · Output revision 15
Published: 2026-10-26T20:04:36.761315Z · Producing pipeline version: Unknown

[CSV sample](outputs/a969dcc25198/catalogue-d2504e52b8b0/sample.csv) · [JSON sample](outputs/a969dcc25198/catalogue-d2504e52b8b0/sample.json) · [Schema](outputs/a969dcc25198/catalogue-d2504e52b8b0/schema.json)

| app | cover\_url | run\_date | episode\_count | first\_seen | last\_seen | release\_date | unlock\_model |
| --- | --- | --- | --- | --- | --- | --- | --- |
| freereels | [https://static\-v1\.mydramawave\.com/vt/prod/cover/ce2298b4\-e28f\-4bc0\-866c\-d424fb0a6ed1\.jpg?image\_process=quality,85/resize,w\_600/format,webp](<https://static-v1.mydramawave.com/vt/prod/cover/ce2298b4-e28f-4bc0-866c-d424fb0a6ed1.jpg?image_process=quality,85/resize,w_600/format,webp>) | 2026\-10\-26 | 45 | 2026\-10\-25 | 2026\-10\-26 | None | ad\_unlock |
| dramabox | [https://hwztchapter\.dramaboxdb\.com/data/cppartner/4x2/42x0/420x0/42000021609/42000021609\.jpg?t=1784533403306](<https://hwztchapter.dramaboxdb.com/data/cppartner/4x2/42x0/420x0/42000021609/42000021609.jpg?t=1784533403306>) | 2026\-10\-26 | 71 | 2026\-10\-25 | 2026\-10\-26 | 2026\-07\-20 | mixed |
| freereels | [https://static\-v1\.mydramawave\.com/vt/resource/netdisk/28284/0\_ceb8fbb2c2a2ad9af1a2ae6479aba907\.jpg?image\_process=quality,85/resize,w\_600/format,webp](<https://static-v1.mydramawave.com/vt/resource/netdisk/28284/0_ceb8fbb2c2a2ad9af1a2ae6479aba907.jpg?image_process=quality,85/resize,w_600/format,webp>) | 2026\-10\-26 | 40 | 2026\-10\-26 | 2026\-10\-26 | None | coins |
| reelshort | [https://v\-mps\.crazymaplestudios\.com/images/b78dc7a0\-3b75\-11f0\-b65a\-27549cd2a91e\.jpg](<https://v-mps.crazymaplestudios.com/images/b78dc7a0-3b75-11f0-b65a-27549cd2a91e.jpg>) | 2026\-10\-25 | 1 | 2026\-10\-25 | 2026\-10\-25 | 2025\-05\-28 | free |
| reelshort | [https://v\-img\.crazymaplestudios\.com/v\-images/book\_cover\_batch/704200150000006543/26068058\-b89f\-4f7b\-b0f1\-45c295dc1809\.jpg](<https://v-img.crazymaplestudios.com/v-images/book_cover_batch/704200150000006543/26068058-b89f-4f7b-b0f1-45c295dc1809.jpg>) | 2026\-10\-26 | 32 | 2026\-10\-25 | 2026\-10\-26 | 2026\-10\-23 | mixed |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| app | text |
| cover\_url | text |
| run\_date | text |
| episode\_count | integer |
| first\_seen | text |
| last\_seen | text |
| release\_date | text |
| unlock\_model | text |
| metadata\_status | text |

## Short\-drama Android weekly data / charts

8,410 total rows · 500 sampled · Output revision 15
Published: 2026-10-26T20:04:36.761315Z · Producing pipeline version: Unknown

[CSV sample](outputs/a969dcc25198/charts-38edf99fd464/sample.csv) · [JSON sample](outputs/a969dcc25198/charts-38edf99fd464/sample.json) · [Schema](outputs/a969dcc25198/charts-38edf99fd464/schema.json)

| app | title | rank | run\_date | country | rail\_raw | view\_basis |
| --- | --- | --- | --- | --- | --- | --- |
| freereels | Patient Zero，Back from the Dead | 1 | 2026\-10\-25 | DE | RANGLISTE / Tag | locale\-based; not storefront\-verified |
| reelshort | Menolak Lima Pasangan Wanitaku | 1 | 2026\-10\-26 | ID | KATEGORI | locale\-based; not storefront\-verified |
| reelshort | My Alpha, My Forbidden Fate | 1 | 2026\-10\-26 | US | 🌙7 Werewolf Romances Bound by Fate | locale\-based; not storefront\-verified |
| dramabox | Step Back\! I'm the Hidden King | 1 | 2026\-10\-26 | GB | Counterattack | locale\-based; not storefront\-verified |
| freereels | Three Alphas Regret Too Late | 1 | 2026\-10\-26 | US | NEW | locale\-based; not storefront\-verified |

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

30 total rows · 30 sampled · Output revision 15
Published: 2026-10-26T20:04:36.761315Z · Producing pipeline version: Unknown

[CSV sample](outputs/a969dcc25198/coin-packs-44368b8d70e4/sample.csv) · [JSON sample](outputs/a969dcc25198/coin-packs-44368b8d70e4/sample.json) · [Schema](outputs/a969dcc25198/coin-packs-44368b8d70e4/schema.json)

| app | run\_date | bonus\_coins | country | currency | pack\_coins | pack\_type | price\_local |
| --- | --- | --- | --- | --- | --- | --- | --- |
| reelshort | 2026\-10\-26 | 400 | US | USD | 2000 | one\_off | 19\.99 |
| reelshort | 2026\-10\-26 | 15 | GB | GBP | 300 | one\_off | 2\.69 |
| reelshort | 2026\-10\-26 | 420 | ID | IDR | 1400 | one\_off | 239000 |
| reelshort | 2026\-10\-26 | 900 | DE | EUR | 3000 | one\_off | 30\.99 |
| reelshort | 2026\-10\-26 | 25 | DE | EUR | 500 | one\_off | 4\.99 |

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

47,393 total rows · 500 sampled · Output revision 15
Published: 2026-10-26T20:04:36.761315Z · Producing pipeline version: Unknown

[CSV sample](outputs/a969dcc25198/economics-5e9ad751b5e6/sample.csv) · [JSON sample](outputs/a969dcc25198/economics-5e9ad751b5e6/sample.json) · [Schema](outputs/a969dcc25198/economics-5e9ad751b5e6/schema.json)

| app | coin\_price\_per\_episode | conflict | cost\_to\_finish\_coins | economics\_status | free\_episodes | observations | observed\_locales |
| --- | --- | --- | --- | --- | --- | --- | --- |
| reelshort | 60 | False | 3600 | coin requirement observed; cash cost unverified | 9 | \[\{"country": "ID", "run\_date": "2026\-10\-26", "free\_episodes": 9, "cost\_to\_finish\_coins": 3600, "coin\_price\_per\_episode": 60}\] | ID |
| freereels | 60 | False | 1920 | coin requirement observed; cash cost unverified | 4 | \[\{"country": "DE", "run\_date": "2026\-10\-25", "free\_episodes": 4, "cost\_to\_finish\_coins": 1920, "coin\_price\_per\_episode": 60}\] | DE |
| dramabox | 50 | False | 2100 | coin requirement observed; cash cost unverified | 1 | \[\{"country": "GB", "run\_date": "2026\-10\-26", "free\_episodes": 1, "cost\_to\_finish\_coins": 2100, "coin\_price\_per\_episode": 50}, \{"country": "US", "run\_date": "2026\-10\-26", "free\_episodes": 1, "cost\_to\_finish\_coins": 2100, "coin\_price\_per\_episode": 50}\] | GB,US |
| freereels | 60 | False | 2460 | coin requirement observed; cash cost unverified | 9 | \[\{"country": "GB", "run\_date": "2026\-10\-26", "free\_episodes": 9, "cost\_to\_finish\_coins": 2460, "coin\_price\_per\_episode": 60}, \{"country": "US", "run\_date": "2026\-10\-26", "free\_episodes": 9, "cost\_to\_finish\_coins": 2460, "coin\_price\_per\_episode": 60}\] | GB,US |
| reelshort | 60 | False | 780 | coin requirement observed; cash cost unverified | 7 | \[\{"country": "GB", "run\_date": "2026\-10\-26", "free\_episodes": 7, "cost\_to\_finish\_coins": 780, "coin\_price\_per\_episode": 60}, \{"country": "US", "run\_date": "2026\-10\-26", "free\_episodes": 7, "cost\_to\_finish\_coins": 780, "coin\_price\_per\_episode": 60}\] | GB,US |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| app | text |
| coin\_price\_per\_episode | integer |
| conflict | boolean |
| cost\_to\_finish\_coins | integer |
| economics\_status | text |
| free\_episodes | integer |
| observations | jsonb |
| observed\_locales | text |
| row\_key | text |
| run\_date | text |
| title | text |
| title\_id | text |
| view\_basis | text |

## Short\-drama Android weekly data / localisations

69,586 total rows · 500 sampled · Output revision 15
Published: 2026-10-26T20:04:36.761315Z · Producing pipeline version: Unknown

[CSV sample](outputs/a969dcc25198/localisations-f1a3061e0655/sample.csv) · [JSON sample](outputs/a969dcc25198/localisations-f1a3061e0655/sample.json) · [Schema](outputs/a969dcc25198/localisations-f1a3061e0655/schema.json)

| app | country | genres | row\_key | run\_date | title | title\_id | title\_original |
| --- | --- | --- | --- | --- | --- | --- | --- |
| dramabox | US | \["Betrayal", "Winning Her Back", "Innocent Damsel", "Love Triangle", "Second Chance", "Love After Marriage"\] | 2026\-10\-25\|dramabox\|US\|41000100933 | 2026\-10\-25 |  The Man I Love | 41000100933 | None |
| dramabox | ID | \["Serangan Balik", "CEO", "Pembalikan Identitas", "Balas Dendam", "Modern", "Romansa"\] | 2026\-10\-26\|dramabox\|ID\|42000003873 | 2026\-10\-26 | Perceraian di Hari Pernikahan | 42000003873 | None |
| reelshort | GB | \["Historical"\] | 2026\-10\-26\|reelshort\|GB\|686cc2ad559f715c650b7eee | 2026\-10\-26 | Goodbye, My General Husband | 686cc2ad559f715c650b7eee | None |
| dramabox | GB | \["A Nobody", "The Chosen One", "Underdog Story", "Anime", "Modern", "Powerful Male Lead"\] | 2026\-10\-25\|dramabox\|GB\|42000017927 | 2026\-10\-25 | Venomous Witch Doctor: Saving Lives, Crushing Foes | 42000017927 | None |
| reelshort | ID | \["Perbedaan Usia"\] | 2026\-10\-25\|reelshort\|ID\|6acf31998d90dd0f1a0b0a6a | 2026\-10\-25 | Pak, Penyamaran Istri Anda Terbongkar Lagi\! \(S2\) | 6acf31998d90dd0f1a0b0a6a | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| app | text |
| country | text |
| genres | jsonb |
| row\_key | text |
| run\_date | text |
| title | text |
| title\_id | text |
| title\_original | text |
| total\_views\_display | text |
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

## Recorded repairs

- 2026-10-26T09:37:36.463024Z: temporary blocker

[Get the full dataset for free](https://www.jsonify.com/datasets/short-drama-charts-and-catalogue-c3bee033d5c1?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
