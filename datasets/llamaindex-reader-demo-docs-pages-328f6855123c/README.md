# LlamaIndex reader demo: docs pages

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.



[Get the full dataset for free](https://www.jsonify.com/datasets/llamaindex-reader-demo-docs-pages-328f6855123c?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-10-14T09:05:41.861355Z

## LlamaIndex Module Guides docs / docs\_pages

84 total rows · 84 sampled · Output revision 1
Published: 2026-10-14T09:05:41.861355Z · Producing pipeline version: 1

[CSV sample](outputs/5c79b6ad4535/docs-pages-0c7e7490cb5b/sample.csv) · [JSON sample](outputs/5c79b6ad4535/docs-pages-0c7e7490cb5b/sample.json) · [Schema](outputs/5c79b6ad4535/docs-pages-0c7e7490cb5b/schema.json)

| crawled\_at | description | section | text | title | url | word\_count |
| --- | --- | --- | --- | --- | --- | --- |
| 2026\-10\-14T09:05:19\.433147\+00:00 | None | loading | Data Connectors  Concept  A data connector \(aka Reader\) ingest data from different data sources and data formats into a simple Document representation \(text and simple metadata\)\.  Integration packages | Data Connectors | [https://developers\.llamaindex\.ai/python/framework/module\_guides/loading/connector/](<https://developers.llamaindex.ai/python/framework/module_guides/loading/connector/>) | 148 |
| 2026\-10\-14T09:05:33\.468152\+00:00 | None | querying | Retriever Modules  We are actively adding more tailored retrieval guides\. In the meanwhile, please take a look at the API References\.  Index Retrievers  Please see the retriever modes for mor… | Retriever Modules | [https://developers\.llamaindex\.ai/python/framework/module\_guides/querying/retriever/retrievers/](<https://developers.llamaindex.ai/python/framework/module_guides/querying/retriever/retrievers/>) | 239 |
| 2026\-10\-14T09:05:30\.011980\+00:00 | None | deploying | Module Guides  We provide a few simple implementations to start, with more sophisticated modes coming soon\!  More specifically, the SimpleChatEngine does not make use of a knowledge base, whereas all  | Module Guides | [https://developers\.llamaindex\.ai/python/framework/module\_guides/deploying/chat\_engines/modules/](<https://developers.llamaindex.ai/python/framework/module_guides/deploying/chat_engines/modules/>) | 55 |
| 2026\-10\-14T09:05:21\.332895\+00:00 | None | models | Embeddings  Concept  Embeddings are used in LlamaIndex to represent your documents using a sophisticated numerical representation\. Embedding models take text as input, and return a long list … | Embeddings | [https://developers\.llamaindex\.ai/python/framework/module\_guides/models/embeddings/](<https://developers.llamaindex.ai/python/framework/module_guides/models/embeddings/>) | 1857 |
| 2026\-10\-14T09:05:18\.517308\+00:00 | None | storing | Storing  Concept  LlamaIndex provides a high\-level interface for ingesting, indexing, and querying your external data\.  Under the hood, LlamaIndex also supports swappable storage components t… | Storing | [https://developers\.llamaindex\.ai/python/framework/module\_guides/storing/](<https://developers.llamaindex.ai/python/framework/module_guides/storing/>) | 319 |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| crawled\_at | text |
| description | text |
| section | text |
| text | text |
| title | text |
| url | text |
| word\_count | integer |

## How the pipeline works

```mermaid
flowchart LR
  n0["discover"]
  n1["extract#95;article"]
  n2["deduplicate"]
  n3["docs#95;pages"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **discover**: Read the supplied LlamaIndex sitemap, retain only Module Guides URLs, deduplicate and cap at 100; order sections round\-robin for representative small runs\.
- **extract\_article**: Fetch each server\-rendered page, verify final URL and HTTP status, and extract full H1, metadata and article text with code preserved and site chrome excluded\.
- **deduplicate**: Keep one article row for each final canonical URL after redirects\.
- **docs\_pages**: Complete Module Guides articles suitable for Document\(text=item\['text'\], metadata=\{'url': item\['url'\]}\)\.

## Version history

- 2026-10-14T08:40:35.879157Z: v1: Added the unscheduled Module Guides sitemap collection with full article text, preserved code blocks, canonical URLs and the requested docs\_pages fields\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/llamaindex-reader-demo-docs-pages-328f6855123c?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
