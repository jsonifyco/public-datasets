# Worldwide Literary Agents, Agencies &amp; Fiction Publishers Directory

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

A source\-backed directory of literary agents and agencies across ten configurable language markets, with optional fiction publishers and publicly sourced professional details\.

[Get the full dataset for free](https://www.jsonify.com/datasets/worldwide-literary-agents-and-fiction-publishers-0f2335ceed4c?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 6
- Last published: 2026-10-17T17:35:55.531140Z

## The brief

> build &lt;[https://www\.reddit\.com/r/webscraping/comments/1x78b0s/scraping\_streaming\_subscription\_prices\_per/?share\_id=Y0pFrx3EXo3RlwIoYK6Br&amp;amp;utm\_content=2&amp;amp;utm\_medium=ios\_app&amp;amp;utm\_name=iossmf&amp;amp;utm\_source=share&amp;amp;utm\_term=2\|reddit\.com/r/webscraping/…/scraping\_streaming\_subscription\_prices\_per?share\_id=…&amp;amp;…](<https://www.reddit.com/r/webscraping/comments/1x78b0s/scraping_streaming_subscription_prices_per/?share_id=Y0pFrx3EXo3RlwIoYK6Br&amp;amp;utm_content=2&amp;amp;utm_medium=ios_app&amp;amp;utm_name=iossmf&amp;amp;utm_source=share&amp;amp;utm_term=2%7Creddit.com/r/webscraping/%E2%80%A6/scraping_streaming_subscription_prices_per?share_id=%E2%80%A6&amp;amp;%E2%80%A6>)&gt; and &lt;[https://www\.reddit\.com/r/webscraping/comments/1x7d07k/literary\_agents\_scraping/?share\_id=Q9c6L](<https://www.reddit.com/r/webscraping/comments/1x7d07k/literary_agents_scraping/?share_id=Q9c6L>) … (excerpt)

Original request to Jason.

## Worldwide literary contacts / contacts

145 total rows · 100 sampled · Output revision 6
Published: 2026-10-17T17:35:55.531140Z · Producing pipeline version: 6

[CSV sample](outputs/f5fba97fc3b2/contacts-aa5af4084f37/sample.csv) · [JSON sample](outputs/f5fba97fc3b2/contacts-aa5af4084f37/sample.json) · [Schema](outputs/f5fba97fc3b2/contacts-aa5af4084f37/schema.json)

| contact\_url | country | email | email\_evidence | email\_owner | email\_source\_url | entity\_type | evidence |
| --- | --- | --- | --- | --- | --- | --- | --- |
| None | None | None | None | None | None | None | None |
| None | None | None | None | None | None | None | None |
| None | None | None | None | None | None | None | None |
| [https://greyhoundliterary\.co\.uk/contact](<https://greyhoundliterary.co.uk/contact>) | United Kingdom | None | None | None | None | agent | Maria Brannan Agent, Translation Rights Manager Fiction, Non\-Fiction, Young Adult |
| None | None | None | None | None | None | None | None |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| contact\_url | text |
| country | text |
| email | text |
| email\_evidence | text |
| email\_owner | text |
| email\_source\_url | text |
| entity\_type | text |
| evidence | text |
| fiction\_evidence | text |
| fiction\_source\_url | text |
| genres | jsonb |
| languages\_evidence | text |
| name | text |
| observed\_at | text |
| organization | text |
| search\_language | text |
| source\_url | text |
| status | text |
| submission\_guidelines | text |
| website | text |
| working\_languages | jsonb |

## How the pipeline works

```mermaid
flowchart LR
  n0["source#95;seeds"]
  n1["source#95;pages"]
  n2["previous#95;contacts"]
  n3["preferred#95;entity#95;sources"]
  n4["entity#95;name#95;aliases"]
  n5["markets"]
  n6["discover"]
  n7["source#95;panel"]
  n8["verify"]
  n9["reconcile"]
  n10["contacts"]
  n5 --> n6
  n6 --> n7
  n7 --> n8
  n8 --> n9
  n9 --> n10
  n0 --> n5
  n1 --> n5
  n2 --> n5
  n3 --> n5
  n4 --> n5
  n2 --> n5
  n1 --> n5
  n0 --> n6
  n3 --> n8
  n4 --> n9
  n2 --> n9
```

- **source\_seeds**: Additional known literary\-source pages by language market and entity category; combined with fresh discovery and verified from their live pages\.
- **source\_pages**: Optional explicit source nominations, each with search\_language, wanted and source\_url; all undergo normal live verification\.
- **previous\_contacts**: Saved contacts used only for targeted publisher evidence refresh\.
- **preferred\_entity\_sources**: Preferred official pages for named entities; fetched and verified, never treated as evidence by configuration alone\.
- **entity\_name\_aliases**: Source\-confirmed multilingual names for the same entity, scoped to its official host and entity type\.
- **markets**: Plan literary\-agent discovery in the selected language markets, optionally adding fiction publishers\.
- **discover**: Search native\-language and international terms for each market; search results only nominate pages and are never delivered as verified contacts\.
- **source\_panel**: Deduplicate nominated pages and interleave language markets so bounded runs do not silently cover English only\.
- **verify**: Read source pages, verify literary representation or fiction publishing, and retain only quoted public emails attributable to the named agent or agency\. Never guess emails\.
- **reconcile**: Deduplicate named entities and public contact emails while retaining source failures and missing coverage\. Fail when no source\-backed contacts were found\.
- **contacts**: Source\-backed literary agents/agencies and optional fiction publishers with attributable public emails, plus explicit discovery coverage gaps\.

## Version history

- 2026-10-17T16:36:14.339731Z: v1: Build worldwide literary\-agent discovery across ten language markets, with optional verified fiction publishers and public emails\.
- 2026-10-17T17:03:31.765588Z: v2: Deduplicate multilingual agency identities and save explicit fiction\-publishing evidence and source links\. Refresh publisher evidence without dropping other saved contacts\.
- 2026-10-17T17:13:02.589864Z: v3: Merge punctuation and agency\-name variants only when their source websites match\. Allow saved\-contact reconciliation without refetching or changing observation dates\.
- 2026-10-17T17:26:23.018122Z: v4: Merge duplicate entities that differ only by a missing email while retaining distinct public contacts\. Prefer configured official entity pages over conflicting directory quotations and refresh Anagrama's evidence\.
- 2026-10-17T17:30:21.936394Z: v5: Recognize Dar Al Adab's English and Arabic names as one publisher, retaining its public email and removing the duplicate\.
- 2026-10-17T17:35:41.159715Z: v6: Require organization names outside email addresses when checking ownership evidence\. Repair the saved Eram and Rajmangal quotations while preserving their public email addresses\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/worldwide-literary-agents-and-fiction-publishers-0f2335ceed4c?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
