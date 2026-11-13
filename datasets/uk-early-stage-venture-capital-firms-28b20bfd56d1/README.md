# UK Early\-Stage Venture Capital Firms

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

UK early\-stage venture capital firms with investment focus, stages, location, websites and evidence links\.

[Get the full dataset for free](https://www.jsonify.com/datasets/uk-early-stage-venture-capital-firms-28b20bfd56d1?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-11-13T16:00:54.241404Z

## The brief

> I need this data: UK early\-stage venture capital firms with investment focus, stages, location, websites and evidence links\.

Summary from the public dataset description.

## UK early\-stage venture capital firms / main

50 total rows · 10 sampled · Output revision 1
Published: 2026-11-13T16:00:54.241404Z · Producing pipeline version: 1

[CSV sample](outputs/180d7f4cb807/main-0d6e4079e367/sample.csv) · [JSON sample](outputs/180d7f4cb807/main-0d6e4079e367/sample.json) · [Schema](outputs/180d7f4cb807/main-0d6e4079e367/schema.json)

| checked\_date | evidence\_urls | focus | name | notes | stages | uk\_location | website |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 2026\-11\-12 | [https://dawncapital\.com](<https://dawncapital.com>) | B2B technology | Dawn Capital | Website describes investing in early founders and states a London address; precise initial rounds not stated\. | Early stage \(precise rounds not stated\) | London | [https://dawncapital\.com](<https://dawncapital.com>) |
| 2026\-11\-12 | [https://localglobe\.vc](<https://localglobe.vc>); [https://ukiz\.co\.uk/investors](<https://ukiz.co.uk/investors>) | UK and European technology | LocalGlobe | Official website plus UKIZ directory corroboration for location and/or stages\. | Pre\-seed; seed | London | [https://localglobe\.vc](<https://localglobe.vc>) |
| 2026\-11\-12 | [https://firstminute\.capital](<https://firstminute.capital>) | European technology founders, particularly AI and deep tech | firstminute capital | London address and investment stage stated on official website\. | Inception; seed | London | [https://firstminute\.capital](<https://firstminute.capital>) |
| 2026\-11\-12 | [https://northstarventures\.co\.uk](<https://northstarventures.co.uk>); [https://ukiz\.co\.uk/investors](<https://ukiz.co.uk/investors>); [https://seedtable\.com/investors/northstar\-ventures?sector=health](<https://seedtable.com/investors/northstar-ventures?sector=health>) | Early\-stage technology, life sciences and climate businesses in the North East | Northstar Ventures | Official site and linked public directory/news evidence\. Broader\-stage mandate where indicated\. | Pre\-seed; seed | Newcastle upon Tyne | [https://northstarventures\.co\.uk](<https://northstarventures.co.uk>) |
| 2026\-11\-12 | [https://oxfordscienceenterprises\.com](<https://oxfordscienceenterprises.com>) | Deep tech, life sciences, and healthtech | Oxford Science Enterprises | Official website states Oxford base and investment range\. | Pre\-seed to growth | Oxford | [https://oxfordscienceenterprises\.com](<https://oxfordscienceenterprises.com>) |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| checked\_date | text |
| evidence\_urls | text |
| focus | text |
| name | text |
| notes | text |
| stages | text |
| uk\_location | text |
| website | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["saved0"]
  n1["prepare"]
  n2["tables"]
  n3["main"]
  n1 --> n2
  n2 --> n3
  n0 --> n1
  n0 --> n1
```

- **saved0**: Read the existing saved worksheet without contacting any sources\.
- **prepare**: Copy the saved sample and sort it for public reading without refreshing sources\.
- **tables**: Keep the saved worksheets separate in the public workbook\.
- **main**: Existing saved sample records\.

## Version history

- 2026-11-13T16:00:43.006315Z: v1: Make the saved sample available for a neutral public page without new collection\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/uk-early-stage-venture-capital-firms-28b20bfd56d1?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
