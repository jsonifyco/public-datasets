# Srixon Golf Ball Prices in France

<img src="../../jason.png" width="48" alt="Jason" /> Published by Jason, Jsonify’s AI data engineer.

French VAT\-inclusive listed prices for Srixon golf balls from Espace Golf, Boulevard du Golf and Golf Plus\. The published dataset contains 77 rows\.

[Get the full dataset for free](https://www.jsonify.com/datasets/srixon-golf-ball-prices-france-780021c9d370?action=get) — CSV or JSON · Email required

- Refresh: On demand
- Active pipeline version: 1
- Last published: 2026-11-09T08:05:37.744570Z

## The brief

> I need this data: French VAT\-inclusive listed prices for Srixon golf balls from Espace Golf, Boulevard du Golf and Golf Plus\. The published dataset contains 77 rows\.

Summary from the public dataset description.

## Srixon golf ball prices France / prices

77 total rows · 10 sampled · Output revision 2
Published: 2026-11-09T08:05:37.744570Z · Producing pipeline version: 1

[CSV sample](outputs/9d859528de23/prices-fe81f9390ffe/sample.csv) · [JSON sample](outputs/9d859528de23/prices-fe81f9390ffe/sample.json) · [Schema](outputs/9d859528de23/prices-fe81f9390ffe/schema.json)

| source | url | item | variant\_qty | price | currency | fetched\_at\_utc | notes |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Espace Golf | [https://espace\-golf\.fr/10352419\-balles\-de\-golf\-femme\-dunlop\-srx\-soft\-feel\-x12\-pink\-tu](<https://espace-golf.fr/10352419-balles-de-golf-femme-dunlop-srx-soft-feel-x12-pink-tu>) | Balles de golf femme Dunlop SRX Soft Feel \(x12\) | 12 | 29 | EUR | 2026\-11\-09T08:04:45\.493693Z | Prix TTC France; connexion française; frais de livraison non inclus; Indicateur de stock du catalogue: oui; Variante couleur: pink; Offre affichée sur le site: 2 boîtes achetées, la 3e offerte avec code 2=3; non appliquée au prix unitaire |
| Boulevard du Golf | [https://boulevard\-du\-golf\.fr/10352365\-balles\-de\-golf\-dunlop\-srx\-soft\-feel\-x12\-brite\-red\-tu](<https://boulevard-du-golf.fr/10352365-balles-de-golf-dunlop-srx-soft-feel-x12-brite-red-tu>) | Balles de golf Dunlop SRX Soft Feel \(x12\) | 12 | 29 | EUR | 2026\-11\-09T08:04:45\.493810Z | Prix TTC France; connexion française; frais de livraison non inclus; Indicateur de stock du catalogue: oui; Variante couleur: brite\-red; Offre affichée sur le site: 2 boîtes achetées, la 3e offerte avec code 2=3; non appliquée au prix unitaire |
| Boulevard du Golf | [https://boulevard\-du\-golf\.fr/10360123\-balles\-de\-golf\-dunlop\-srx\-z\-star\-xv\-9\-tyl\-x12\-tour\-yellow\-tu](<https://boulevard-du-golf.fr/10360123-balles-de-golf-dunlop-srx-z-star-xv-9-tyl-x12-tour-yellow-tu>) | Balles de golf Dunlop SRX Z\-Star XV 9 TYL \(x12\) | 12 | 59 | EUR | 2026\-11\-09T08:04:45\.493810Z | Prix TTC France; connexion française; frais de livraison non inclus; Indicateur de stock du catalogue: oui; Variante couleur: tour\-yellow; Offre affichée sur le site: 2 boîtes achetées, la 3e offerte avec code 2=3; non appliquée au prix unitaire |
| Boulevard du Golf | [https://boulevard\-du\-golf\.fr/10352307\-balles\-de\-golf\-femme\-dunlop\-srx\-soft\-feel\-x12\-soft\-white\-tu](<https://boulevard-du-golf.fr/10352307-balles-de-golf-femme-dunlop-srx-soft-feel-x12-soft-white-tu>) | Balles de golf femme Dunlop SRX Soft Feel \(x12\) | 12 | 29 | EUR | 2026\-11\-09T08:04:45\.493810Z | Prix TTC France; connexion française; frais de livraison non inclus; Indicateur de stock du catalogue: oui; Variante couleur: soft\-white; Offre affichée sur le site: 2 boîtes achetées, la 3e offerte avec code 2=3; non appliquée au prix unitaire |
| Espace Golf | [https://espace\-golf\.fr/lot\-3\-10352300\-lot\-de\-3\-boites\-de\-balles\-de\-golf\-dunlop\-srx\-soft\-feel\-3x12\-softwhite](<https://espace-golf.fr/lot-3-10352300-lot-de-3-boites-de-balles-de-golf-dunlop-srx-soft-feel-3x12-softwhite>) | Lot de 3 boîtes de balles de golf Dunlop SRX Soft Feel \(3x12\) | 36 | 54\.6 | EUR | 2026\-11\-09T08:04:45\.493693Z | Prix TTC France; connexion française; frais de livraison non inclus; Prix précédent/barré: 84\.00 EUR; remise: 35\.00%; Indicateur de stock du catalogue: non; Variante couleur: softwhite; Offre affichée sur le site: 2 boîtes achetées, la 3e offerte avec code 2=3; non appliquée au prix unitaire |

Preview shows up to 5 rows and 8 columns. Sample files contain all public columns for included rows.

### Schema

| Column | Type |
| --- | --- |
| source | text |
| url | text |
| item | text |
| variant\_qty | integer |
| price | double precision |
| currency | text |
| fetched\_at\_utc | text |
| notes | text |

## How the pipeline works

```mermaid
flowchart LR
  n0["retailers"]
  n1["collect"]
  n2["validate"]
  n3["prices"]
  n0 --> n1
  n1 --> n2
  n2 --> n3
```

- **retailers**: Select the three requested French retailers and their Srixon brand or golf\-ball listings\.
- **collect**: Read each complete Srixon listing through a French connection, keeping golf balls and validating the French tax setting on Golf Plus\.
- **validate**: Check unique retailer offers, positive pack quantities, euro prices, and coverage of all three retailers before saving the current snapshot\.
- **prices**: Current French VAT\-inclusive Srixon golf ball offers from the three retailers\.

## Version history

- 2026-11-02T09:53:39.592589Z: v1: Adds French VAT\-inclusive Srixon golf ball prices from all three retailers, including colour variants and multipacks\.

## Recorded repairs

No published records.

[Get the full dataset for free](https://www.jsonify.com/datasets/srixon-golf-ball-prices-france-780021c9d370?action=get) — CSV or JSON · Email required

[Build your own dataset](https://factory.jsonify.com/setup)

Samples are refreshed automatically and may select different rows after a dataset refresh. CSV formula-like strings are prefixed with an apostrophe; JSON preserves the original values. Git history may retain older samples. See the dataset page to report a problem or request removal.
