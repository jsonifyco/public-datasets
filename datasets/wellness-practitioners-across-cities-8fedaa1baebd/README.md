# Wellness Practitioners in Lisbon, Porto, Barcelona and London

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

A search\-based snapshot of yoga and meditation teachers, massage and holistic practitioners, and psychotherapists across four European cities, with source evidence and conservative duplicate matching\.

[Get the full dataset for free](https://www.jsonify.com/datasets/wellness-practitioners-across-cities-8fedaa1baebd?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-10-22T14:20:21.555858Z

## The brief

> I need this data: A search\-based snapshot of yoga and meditation teachers, massage and holistic practitioners, and psychotherapists across four European cities, with source evidence and conservative duplicate matching\.

Summary from the public dataset description.

## Wellness practitioners / practitioners

200 total rows · 200 sampled · Output revision 1
Published: 2026-10-22T14:20:21.555858Z · Producing pipeline version: 1

[CSV sample](outputs/3b0a5677c0b5/practitioners-8bb9895cc443/sample.csv) · [JSON sample](outputs/3b0a5677c0b5/practitioners-8bb9895cc443/sample.json) · [Schema](outputs/3b0a5677c0b5/practitioners-8bb9895cc443/schema.json)

| name | city | country | categories | roles | specialties | website | email |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Irene TOLU | Lisbon | Portugal | \["Yoga"\] | \["teacher"\] | Yoga instruction | None | None |
| Dr\.ª Rita Sousa | Porto | Portugal | \["Psychotherapy"\] | \["therapist"\] | Intervenção em trauma, vinculação e regulação emocional com adultos, crianças, adolescentes e famílias; EMDR\. | None | None |
| Katya | London | United Kingdom | \["Massage"\] | \["therapist"\] | Massage | None | None |
| Charli Van Ness | London | United Kingdom | \["Yoga"\] | \["teacher"\] | 200\-hour and 300\-hour yoga teacher training | None | None |
| Zoe | London | United Kingdom | \["Meditation", "Psychotherapy"\] | \["teacher", "therapist"\] | Mindfulness and Mindful Self\-Compassion programmes; counselling\-psychotherapy; mindfulness teacher supervision | None | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| name | text |
| city | text |
| country | text |
| categories | jsonb |
| roles | jsonb |
| specialties | text |
| website | text |
| email | text |
| phone | text |
| languages | jsonb |
| qualifications | text |
| profile\_urls | jsonb |
| source\_urls | jsonb |
| source\_names | jsonb |
| location\_evidence | jsonb |
| practice\_evidence | jsonb |
| checked\_at | text |
| source\_count | integer |
| observations\_merged | integer |
| identity\_basis | text |
| practitioner\_key | text |
| possible\_duplicate | boolean |

## How the pipeline works

```mermaid
flowchart LR
  n0["source#95;lists"]
  n1["plan#95;searches"]
  n2["discover#95;lists"]
  n3["combine#95;lists"]
  n4["read#95;professionals"]
  n5["consolidate#95;people"]
  n6["practitioners"]
  n1 --> n2
  n2 --> n3
  n3 --> n4
  n4 --> n5
  n5 --> n6
  n0 --> n1
  n0 --> n3
```

- **source\_lists**: Additional public directories, studio teacher lists and clinic teams to consolidate alongside web discovery\. Each row has city, country, url and label\.
- **plan\_searches**: Plan a public directory search for every selected city and wellness practice area\.
- **discover\_lists**: Find public directories, clinic teams, teacher lists and individual professional pages for each city and practice area\.
- **combine\_lists**: Combine discovered pages with the editable source lists and remove repeated source URLs within each city\.
- **read\_professionals**: Read each public source page and extract named professionals with evidence of their city, services and teaching roles\.
- **consolidate\_people**: Merge verified cross\-list duplicates, flag unresolved same\-name matches and balance the saved list across cities and practice areas\.
- **practitioners**: Consolidated wellness practitioners, teachers and therapists with public evidence and source links\.

## Version history

- 2026-10-22T14:15:31.375870Z: v1: Find and consolidate wellness practitioners, teachers and therapists across Lisbon, Porto, Barcelona and London, with editable cities, practice areas and source lists\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/wellness-practitioners-across-cities-8fedaa1baebd?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
