# Unicorn Factory Lisboa startup portfolio

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

All startups listed in the Unicorn Factory Lisboa portfolio, with names, official website taglines, published pricing or quote information, source links and availability statuses\. Refreshes replace the saved snapshot; no schedule is enabled\. Includes an alive true/false homepage accessibility check, separate from company identity or operating status\.

[Get the full dataset for free](https://www.jsonify.com/datasets/unicorn-factory-lisboa-startup-portfolio-81b2a4675212) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 2
- Last published: 2026-10-12T15:41:47.150674Z

## The brief

> I want to build a pipeline: A list of all startups on https://unicornfactorylisboa\.com/portfolio/ \-\- go to each website and find name, tagline, pricing information too\.

Original request to Jason.

## Unicorn Factory Lisboa startups / startups

502 total rows · 100 sampled · Output revision 2
Published: 2026-10-12T15:41:47.150674Z · Producing pipeline version: 2

[CSV sample](outputs/c0d257d8a9fc/startups-eef5aa92dccb/sample.csv) · [JSON sample](outputs/c0d257d8a9fc/startups-eef5aa92dccb/sample.json) · [Schema](outputs/c0d257d8a9fc/startups-eef5aa92dccb/schema.json)

| startup\_id | name | website | portfolio\_url | alive | website\_name | tagline | pricing\_information |
| --- | --- | --- | --- | --- | --- | --- | --- |
| m\-24991 | Grupo MHS | https://www\.mariabike\.com/en | https://unicornfactorylisboa\.com/portfolio/9/ | True | Maria Bike | An electric vehicle | None |
| m\-25002 | Mixrift | https://www\.mixrift\.com/about | https://unicornfactorylisboa\.com/portfolio/14/ | True | MIXRIFT | XR Gaming Studio \- Dublin &amp; Bucharest | None |
| m\-24736 | Grafema | https://www\.grafema\.xyz/ | https://unicornfactorylisboa\.com/portfolio/9/ | True | Grafema | AI that executes your B2B prospecting | None |
| m\-20120 | ANNEA | http://www\.annea\.ai | https://unicornfactorylisboa\.com/portfolio/2/ | True | ANNEA | The brain for RENEWABLES | None |
| m\-24990 | Grenaa Games | https://www\.grenaagames\.com | https://unicornfactorylisboa\.com/portfolio/9/ | True | Grenaa Games | None | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns.

### Schema

| Column | Type |
| --- | --- |
| startup\_id | text |
| name | text |
| website | text |
| portfolio\_url | text |
| alive | boolean |
| website\_name | text |
| tagline | text |
| pricing\_information | text |
| pricing\_status | text |
| website\_status | text |
| checked\_urls | jsonb |
| pricing\_source\_urls | jsonb |
| notes | text |
| checked\_at | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["pages"]
  n1["directory"]
  n2["validate#95;directory"]
  n3["website#95;details"]
  n4["startups"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
  n3 --> n4
```

- **pages**: Read the portfolio&\#x27;s current pagination and enumerate every directory page\.
- **directory**: Parse every startup card on each portfolio page and preserve the listed company website\.
- **validate\_directory**: Validate unique portfolio identities before visiting websites; never silently discard repeated pages\.
- **website\_details**: Visit each official homepage and relevant linked pricing pages; extract evidence\-backed taglines and prices, retaining unavailable sites with explicit status\.
- **startups**: One row per portfolio startup, with official website tagline, pricing evidence, and explicit availability statuses\.

## Version history

- 2026-10-12T11:18:58.351833Z: v1: Build the complete Unicorn Factory Lisboa portfolio collection with official website taglines, pricing evidence and clear missing\-data statuses\.
- 2026-10-12T14:11:43.103133Z: v2: Added an alive true/false field indicating whether each startup’s homepage is accessible\. Website accessibility is separate from company identity and operating status\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/unicorn-factory-lisboa-startup-portfolio-81b2a4675212) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
