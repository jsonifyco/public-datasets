# Supermarket Franchise Keyword and AI Prompt Volumes

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Supermarket franchise keyword and AI prompt volume estimates for US\-English research, with monthly observations and coverage details\.

[Get the full dataset for free](https://www.jsonify.com/datasets/supermarket-franchise-keyword-and-ai-prompt-volumes-a3f8157e871e?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-10-31T11:20:11.061198Z

## The brief

> I need this data: Supermarket franchise keyword and AI prompt volume estimates for US\-English research, with monthly observations and coverage details\.

Summary from the public dataset description.

## Supermarket Franchise Search and Prompt Volumes / volumes

16 total rows · 16 sampled · Output revision 1
Published: 2026-10-31T11:20:11.061198Z · Producing pipeline version: 1

[CSV sample](outputs/dce72f29ea55/volumes-5d2d96b881a9/sample.csv) · [JSON sample](outputs/dce72f29ea55/volumes-5d2d96b881a9/sample.json) · [Schema](outputs/dce72f29ea55/volumes-5d2d96b881a9/schema.json)

| average\_monthly\_volume | collected\_at | coverage\_note | coverage\_status | discovery\_term | geography | language | latest\_reported\_volume |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 13\.58 | 2026\-10\-31T11:19:59\.979311\+00:00 | Provider estimates, not observed platform logs\. AI discovery is a ranked sample; irrelevant questions are excluded\. Missing months are unknown, not zero\. | complete\_12\_months | supermarket franchise cost | United States | English | 19 |
| None | 2026\-10\-31T11:19:59\.512704\+00:00 | Provider keyword estimates may group close variants\. Do not sum overlapping keywords\. Missing months are unknown, not zero\. | no\_reported\_volume | how to open a supermarket franchise | United States | English | None |
| None | 2026\-10\-31T11:19:59\.979311\+00:00 | Provider estimates, not observed platform logs\. AI discovery is a ranked sample; irrelevant questions are excluded\. Missing months are unknown, not zero\. | partial\_history | supermarket franchise cost | United States | English | 1 |
| None | 2026\-10\-31T11:19:59\.512704\+00:00 | Provider keyword estimates may group close variants\. Do not sum overlapping keywords\. Missing months are unknown, not zero\. | no\_reported\_volume | how to start a super market business through franchise | United States | English | None |
| 10 | 2026\-10\-31T11:19:59\.512704\+00:00 | Provider keyword estimates may group close variants\. Do not sum overlapping keywords\. Missing months are unknown, not zero\. | complete\_12\_months | supermarket franchise cost | United States | English | 10 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| average\_monthly\_volume | double precision |
| collected\_at | text |
| coverage\_note | text |
| coverage\_status | text |
| discovery\_term | text |
| geography | text |
| language | text |
| latest\_reported\_volume | integer |
| monthly\_volumes | text |
| months\_observed | integer |
| period\_end | text |
| period\_start | text |
| platform | text |
| provider\_matching\_records | integer |
| query\_or\_prompt | text |
| query\_type | text |
| volume\_source | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["plan"]
  n1["collect"]
  n2["deduplicate"]
  n3["volumes"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **plan**: Prepare the keyword phrases and ChatGPT topic searches for US\-English volume estimates\.
- **collect**: Read monthly search estimates and measured ChatGPT prompts, retaining only relevant business questions\.
- **deduplicate**: Deduplicate measured prompts and flag incomplete histories without treating missing volumes as zero\.
- **volumes**: US\-English keyword and measured AI prompt volume estimates with twelve\-month coverage\.

## Version history

- 2026-10-31T11:19:33.113419Z: v1: Added reusable US\-English keyword and ChatGPT prompt volume collection, with monthly histories, clear missing\-volume flags and a CSV report\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/supermarket-franchise-keyword-and-ai-prompt-volumes-a3f8157e871e?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
