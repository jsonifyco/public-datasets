# US Data Centers: Virginia, Texas, Arizona, Georgia and Ohio

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

125 US data center facility and campus listings from Datacenters\.com, with source\-linked locations and directory\-reported capacity and dates where available\.

[Get the full dataset for free](https://www.jsonify.com/datasets/us-data-centers-five-state-sample-dfb1295a7834?action=get) — CSV or JSON · Email required

- Refresh: weekly
- Active pipeline version: 9
- Last published: 2026-11-17T16:33:30.642968Z

## The brief

> I need this data: 125 US data center facility and campus listings from Datacenters\.com, with source\-linked locations and directory\-reported capacity and dates where available\.

Summary from the public dataset description.

## US Data Centers • Five\-State Sample / facilities

125 total rows · 50 sampled · Output revision 6
Published: 2026-11-17T16:33:30.642968Z · Producing pipeline version: 9

[CSV sample](outputs/128b421e373a/facilities-3c5ca5554a2f/sample.csv) · [JSON sample](outputs/128b421e373a/facilities-3c5ca5554a2f/sample.json) · [Schema](outputs/128b421e373a/facilities-3c5ca5554a2f/schema.json)

| capacity\_scope | checked\_at | city | directory\_power\_capacity\_mw | facility\_name | opened\_or\_announced\_year | operator | power\_capacity\_mw |
| --- | --- | --- | --- | --- | --- | --- | --- |
| not shown: no supported total power capacity on the directory page | 2026\-11\-17T16:02:31\.829351\+00:00 | Dallas | None | DAL05 Dallas, TX | None | IBM Cloud | None |
| host building: 5\.0 MW is described as power available to Lunavi’s colocation operation in the Equinix AT1 facility; the published figure is not stated as the whole building’s capacity\. | 2026\-11\-17T15:59:35\.273749\+00:00 | Atlanta | 5 | AT1 Atlanta Data Center | None | Lunavi | 5 |
| unclear: The 120\.0 MW figure is described as power accessible to the data center, but its capacity scope is not specified\. | 2026\-11\-17T16:02:44\.986447\+00:00 | Ashburn | 120 | IAD02 Ashburn VA Data Center | None | Aligned Data Centers | 120 |
| not shown: no supported total power capacity on the directory page | 2026\-11\-17T16:02:51\.739398\+00:00 | South Riding | None | 25420 Sutton Bay | None | Amazon AWS | None |
| unclear: 12\.0 MW is described as power the data center has access to; the capacity scope is not specified\. | 2026\-11\-17T15:59:37\.551518\+00:00 | Atlanta | 12 | AT4 Atlanta Data Center | None | Equinix | 12 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| capacity\_scope | text |
| checked\_at | text |
| city | text |
| directory\_power\_capacity\_mw | double precision |
| facility\_name | text |
| opened\_or\_announced\_year | integer |
| operator | text |
| power\_capacity\_mw | double precision |
| power\_evidence | text |
| source\_url | text |
| state | text |
| status | text |
| status\_evidence | text |
| street\_address | text |
| year\_evidence | text |
| year\_match\_evidence | text |
| year\_research\_note | text |
| year\_source\_url | text |
| year\_type | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["selected#95;facilities"]
  n1["dated#95;facilities"]
  n2["states"]
  n3["discover"]
  n4["details"]
  n5["validate"]
  n6["capacity#95;review"]
  n7["year#95;sources"]
  n8["dated#95;panel"]
  n9["date#95;identity#95;audit"]
  n10["explicit#95;capacity#95;audit"]
  n11["evidence#95;checks"]
  n12["facilities"]
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
  n0 --> n2
  n1 --> n2
  n0 --> n5
  n1 --> n8
```

- **selected\_facilities**: Optional previously validated facility snapshot for evidence updates; unbound runs rediscover the normal five\-state sample\.
- **dated\_facilities**: Optional saved facility snapshot for revalidating date identity without repeating discovery or research\.
- **states**: Choose the five requested states for a balanced public facility sample\.
- **discover**: Read the first directory page in each state and discover distinct street\-addressed business locations for a balanced sample\.
- **details**: Read each facility page for its actual city, stated total MW capacity and explicitly described lifecycle dates and status\.
- **validate**: Check unique source pages and distinct addresses, all five states and the exact requested balanced sample before replacing the saved snapshot\.
- **capacity\_review**: Recheck source capacity scope and contradictions, preserve the stated directory figure, and reject construction\-only opening years\.
- **year\_sources**: Find and verify explicit opening or announcement years on confidently matched public second\-source facility or press pages\.
- **dated\_panel**: Reuse a saved complete panel when only date identity needs rechecking\.
- **date\_identity\_audit**: Require exact address or operator\-specific facility identity before retaining a secondary\-source year\.
- **explicit\_capacity\_audit**: Withhold canonical capacity when the facility description explicitly contradicts its directory total power\.
- **evidence\_checks**: Check year/source consistency and retain the full requested five\-state panel for an ordinary refresh\.
- **facilities**: Source\-backed five\-state public data center facility sample, with secondary\-source year evidence and capacity scope notes\.

## Version history

- 2026-11-17T14:38:21.648369Z: v1: Create a balanced public five\-state facility sample with source\-backed capacity and lifecycle fields, ready for weekly refreshes\.
- 2026-11-17T15:23:45.246026Z: v2: Add cited second\-source opening and announcement years and capacity scope notes\. Remove construction\-only opening dates and flag conflicting or implausible power figures\.
- 2026-11-17T15:32:16.785620Z: v3: Fixed capacity comparisons that stopped the update when evidence came from separate passages\. Source statements remain quoted exactly\.
- 2026-11-17T15:55:46.801897Z: v4: Exclude public\-tour and groundbreaking\-only dates from opening or original announcement years\.
- 2026-11-17T15:58:53.460799Z: v5: Preserved date provenance when refreshing saved facilities and excluded publication timestamps from opening\-year evidence\.
- 2026-11-17T16:01:57.374443Z: v6: Made capacity checks require complete scope and conflict evidence before accepting a result\.
- 2026-11-17T16:20:11.364028Z: v7: Corrected cross\-operator facility\-name matches and added a final physical\-identity check for every secondary\-source year\.
- 2026-11-17T16:26:59.811585Z: v8: Withhold usable capacity when explicit facility total\-power statements contradict the directory figure, retaining both figures in the scope note\.
- 2026-11-17T16:33:05.729173Z: v9: Recognize another explicit facility\-total wording so CIN3 capacity is withheld on its 1 versus 1\.7 MW source conflict\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/us-data-centers-five-state-sample-dfb1295a7834?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
