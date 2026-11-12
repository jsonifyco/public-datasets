# Six Senses Dubai Room Images

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

Six Senses Dubai room images linked to room types, with image descriptions, categories, URLs and classification basis\. The published dataset contains 36 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/six-senses-dubai-room-images-420e2c20c4c8?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-11-12T10:08:59.773143Z

## The brief

> I need this data: Six Senses Dubai room images linked to room types, with image descriptions, categories, URLs and classification basis\. The published dataset contains 36 rows\.

Summary from the public dataset description.

## Six Senses Dubai Room Images / images

36 total rows · 10 sampled · Output revision 1
Published: 2026-11-12T10:08:59.773143Z · Producing pipeline version: 1

[CSV sample](outputs/d912b2e21508/images-21b2eed1e328/sample.csv) · [JSON sample](outputs/d912b2e21508/images-21b2eed1e328/sample.json) · [Schema](outputs/d912b2e21508/images-21b2eed1e328/schema.json)

| accommodation\_category | checked\_date | classification\_basis | hotel | image\_category | image\_description | image\_id | image\_url |
| --- | --- | --- | --- | --- | --- | --- | --- |
| One\-bedroom suite | 2026\-11\-12 | Official gallery caption and image filename | Six Senses The Palm, Dubai | Bathroom | A dressing area with a double vanity, built\-in wooden wardrobe, and central bench, with a doorway opening to a bedroom with ocean views\. | 99dbbeed468f84cf7b3ef387 | [https://media\.sixsenses\.com/B60H3R33/at/mwsm4528rp4j7vmzhnr6pm3w/Breeze\_Suite\_Palm\_Sea\_View\_bathroom\.jpg?format=webp&amp;width=585](<https://media.sixsenses.com/B60H3R33/at/mwsm4528rp4j7vmzhnr6pm3w/Breeze_Suite_Palm_Sea_View_bathroom.jpg?format=webp&amp;width=585>) |
| One\-bedroom suite | 2026\-11\-12 | Official gallery caption and image filename | Six Senses The Palm, Dubai | Living area | A hotel suite living area with a sofa and lounge chair, looking out through floor\-to\-ceiling glass doors toward a beach and city skyline\. | 6a32bfe287402ef8ed74d99c | [https://media\.sixsenses\.com/B60H3R33/at/m5nk2fwf7psn3v5hs3bmgqjm/Pearl\_Suite\_Palm\_Sea\_View\_living\_room\.jpg?format=webp&amp;width=585](<https://media.sixsenses.com/B60H3R33/at/m5nk2fwf7psn3v5hs3bmgqjm/Pearl_Suite_Palm_Sea_View_living_room.jpg?format=webp&amp;width=585>) |
| One\-bedroom suite | 2026\-11\-12 | Official gallery caption and image filename | Six Senses The Palm, Dubai | Bathroom | Marble double vanity featuring dark green vessel sinks and two round mirrors, complemented by a white freestanding bathtub\. | cbea89115e9094b7b5cdb384 | [https://media\.sixsenses\.com/B60H3R33/at/4vfjnf3jjnnvgkvrwvb6gf66/Pearl\_Suite\_Sea\_View\_bathroom\.jpg?format=webp&amp;width=585](<https://media.sixsenses.com/B60H3R33/at/4vfjnf3jjnnvgkvrwvb6gf66/Pearl_Suite_Sea_View_bathroom.jpg?format=webp&amp;width=585>) |
| One\-bedroom suite | 2026\-11\-12 | Official gallery caption and image filename | Six Senses The Palm, Dubai | Bedroom | King bed in a guest room featuring floor\-to\-ceiling windows, a glass\-railed balcony, and a sea view\. | e00b8320384f221905216781 | [https://media\.sixsenses\.com/B60H3R33/at/pwcwr8rhtfvj5pspg9gc4s/Horizon\_Suite\_with\_Hydrotherapy\_Pool\_bedroom\_with\_vie\.jpg?format=webp&amp;width=585](<https://media.sixsenses.com/B60H3R33/at/pwcwr8rhtfvj5pspg9gc4s/Horizon_Suite_with_Hydrotherapy_Pool_bedroom_with_vie.jpg?format=webp&amp;width=585>) |
| Three\-bedroom suite | 2026\-11\-12 | Official gallery caption and image filename | Six Senses The Palm, Dubai | Bedroom | Two twin beds with bedside lamps and foot\-of\-bed benches, set before floor\-to\-ceiling windows with a view of palm trees\. | df3be4712c597d9ebae34f21 | [https://media\.sixsenses\.com/B60H3R33/at/9nv4gxjwtn4t88fvth3vwpqp/Three\_Bedroom\_Pool\_Retreat\_twin\_bedroom\.jpg?format=webp&amp;width=585](<https://media.sixsenses.com/B60H3R33/at/9nv4gxjwtn4t88fvth3vwpqp/Three_Bedroom_Pool_Retreat_twin_bedroom.jpg?format=webp&amp;width=585>) |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| accommodation\_category | text |
| checked\_date | text |
| classification\_basis | text |
| hotel | text |
| image\_category | text |
| image\_description | text |
| image\_id | text |
| image\_url | text |
| room\_type | text |
| room\_url | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["discover#95;rooms"]
  n1["collect#95;gallery"]
  n2["validate#95;images"]
  n3["images"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **discover\_rooms**: Read all suite types and their image galleries from the official Six Senses The Palm Dubai accommodation page\.
- **collect\_gallery**: Collect each suite's official gallery images and classify their subjects using published captions and filenames\.
- **validate\_images**: Check that each selected suite has image records and that no image\-to\-suite links are duplicated before publishing the refreshed collection\.
- **images**: Official Dubai suite images linked to their room types and classified by space\.

## Version history

- 2026-11-12T10:08:32.241268Z: v1: Created the Six Senses Dubai suite image collection with room\-linked image classifications and a downloadable CSV\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/six-senses-dubai-room-images-420e2c20c4c8?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
