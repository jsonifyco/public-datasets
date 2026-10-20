# WDIWF company monitors

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.



[Get the full dataset for free](https://www.jsonify.com/datasets/wdiwf-company-monitors-f8658ad4c63e?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 3
- Last published: 2026-10-14T13:14:12.125029Z

## browse\_ai\_monitors / monitors

54 total rows · 54 sampled · Output revision 3
Published: 2026-10-14T13:14:12.125029Z · Producing pipeline version: 3

[CSV sample](outputs/3a3b5c8044ab/monitors-e5c19e68e5a3/sample.csv) · [JSON sample](outputs/3a3b5c8044ab/monitors-e5c19e68e5a3/sample.json) · [Schema](outputs/3a3b5c8044ab/monitors-e5c19e68e5a3/schema.json)

| company\_name | company\_slug | content\_hash | content\_summary | error\_message | key\_facts | last\_checked\_at | page\_title |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Microsoft | microsoft | e33d259bbe04bcab46c84cee3bbf5e050f20c154e2059019ea4cb008569e2751 | Microsoft describes benefits that support employees’ physical, mental, emotional, and financial wellbeing, including time off, parental and family caregiver leave, education, discounts, and giving pro | None | \{"named\_benefits": \["not stated on page"\], "parental\_leave\_weeks": \["not stated on page"\], "401k\_match": \["not stated on page"\], "geographic\_eligibility": \["Benefits information may vary depending on  | 2026\-10\-14T13:05:04\.861684\+00:00 | Our benefits |
| Meta Platforms | meta | a43545cab0be4e9d2b700a3d77aa61d14b7478d9206a0333ac83dc84abd95548 | Meta’s leadership page lists its senior leadership team\. The listed leaders include executives with titles spanning company\-wide roles and leadership of products and business groups\. | None | \{"executives": \[\{"name": "Mark Zuckerberg", "title": "Founder, Chairman and Chief Executive Officer"}, \{"name": "Dina Po… | 2026\-10\-14T13:05:04\.861684\+00:00 | Meta Leadership: Executives &amp; Company Leaders \| Meta |
| Meta Platforms | meta | e98e72abafa170cf8d8e7cc378fb9b16e11045832eb0dc5de33dd5af1c2f6e54 | Meta Careers invites people to join teams building technologies, including AI, metaverse and wearables, and infrastructure\. The page features jobs, including a Critical Facility Engineer role in Henri | None | \{"career\_programs": \["not stated on page"\], "employee\_working\_arrangements": \["not stated on page"\], "employment\_locations": \["Henrico, VA \+ 23 locations"\]} | 2026\-10\-14T13:05:04\.861684\+00:00 | Put your skills to work as we build for the future of AI — today |
| Accenture | accenture | 7d213f0e880b6e15e59a574099536a5732f68eaeaf4511772153a80e448a20e7 | The page says, “There are currently no jobs available that match your search criteria\.” It also says the listings shown are the 10,000 newest job listings or the 10,000 most relevant open jobs\. | None | \{"open\_role\_count": \["not stated on page"\], "listed\_roles\_and\_locations": \["not stated on page"\]} | 2026\-10\-14T13:05:04\.861684\+00:00 | Search jobs at Accenture |
| Boeing | boeing | f2dcfdeabcca15f512fcc778544b182b3a0b2fb9202802017b0263a56c30fcc8 | The page lists Boeing executive biographies and associated titles\. It identifies Kelly Ortberg as president and chief executive officer\. | None | \{"executives": \[\{"name": "Kelly Ortberg", "title": "President and Chief Executive Officer"}, \{"name": "Jesus “Jay” Malav… | 2026\-10\-14T13:05:04\.861684\+00:00 | Executive Biographies |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| company\_name | text |
| company\_slug | text |
| content\_hash | text |
| content\_summary | text |
| error\_message | text |
| key\_facts | text |
| last\_checked\_at | text |
| page\_title | text |
| page\_type | text |
| page\_url | text |
| status | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["companies#95;pages"]
  n1["monitor#95;plan"]
  n2["read#95;monitor"]
  n3["monitors"]
  n1 --> n2
  n2 --> n3
  n0 --> n1
  n0 --> n1
```

- **companies\_pages**: 54 official employer pages discovered from corporate and careers navigation, with official report/disclosure lookups where navigation was incomplete\.
- **monitor\_plan**: Prepare the six employers and nine exact page categories with a shared run timestamp\.
- **read\_monitor**: Read each official page, resolve redirects, extract factual summaries and quoted facts, and hash normalized main text; retain honest error rows\.
- **monitors**: One current page\-change monitor per employer and page type\.

## Version history

- 2026-10-14T09:38:57.857301Z: v1: Added the six\-employer monitor table covering nine official page types, with factual summaries, quoted key facts, change hashes and explicit unavailable\-page errors\.
- 2026-10-14T10:24:02.831200Z: v2: Corrected the main English Meta privacy policy and US locale pages, privacy title fallback, political disclosures, and latest three dated newsroom headlines\. Added rendered reads for Meta jobs and Accenture’s latest news list while keeping the monitors table and columns unchanged\.
- 2026-10-14T12:38:39.210993Z: v3: Standardized key facts across all nine page types, with people\-only leadership objects and dated news links\. Google leadership now uses the official Alphabet proxy statement linked from abc\.xyz, with the document URL and disclosure date\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/wdiwf-company-monitors-f8658ad4c63e?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
