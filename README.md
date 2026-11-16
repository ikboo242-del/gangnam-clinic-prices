# Gangnam Clinic Prices — printed aesthetic treatment prices in Gangnam, Seoul

Built 2026-11-17 from the Gangnam Clinic Guide price store (https://gangnamclinicguide.com/how-we-check-prices.html).

> Released 2026-11-16. Rebuilt daily from the source store; last built 2026-11-17.

## What this is

655 price rows from 80 clinics, mostly in Gangnam-gu and Seocho-gu; branches elsewhere in Seoul that the store also tracks (e.g. Hongdae, Mokdong, Jamsil) are included and labelled in `district`. Procedures covered:
botox, filler, hair_removal, inmode, laser_toning, lip_filler, onda, other, package, rejuran, sculptra, shurink, skin_booster, thermage, thread, ultherapy.

Every row is a price **as printed on the clinic's own website**, copied as text by our price monitor. Nothing here is a quote,
an average, a recommendation or a ranking. Rows are sorted by procedure, spec, price and name — not by quality.

Last-checked dates in this file run from 2026-09-17 to 2026-11-17.

## Files

- `gangnam-clinic-prices.csv` — one row per printed price (UTF-8, comma-separated, header row).

## Columns

| Column | Meaning |
|---|---|
| record_id | Stable id: `clinic domain | procedure | spec | price type` |
| clinic_name_en / clinic_name_ko | Clinic name in English and Korean |
| clinic_website | The clinic's own website |
| district | Area label used by the guide (e.g. Apgujeong, Gangnam Station, Sinsa / Garosu-gil) |
| procedure | Normalised procedure key (thermage, ultherapy, botox, filler, rejuran, ...) |
| procedure_label_as_printed | Device/product name as the clinic prints it |
| spec, spec_n, spec_unit | Quantity as printed (e.g. `600 shots`, `1 cc`, `100 units`); `unspecified` = clinic printed no quantity |
| price_krw | Printed price in Korean won. If the clinic prints a range, this is the lower end |
| price_max_krw | Upper end of a printed range, blank otherwise |
| price_type | `published` (list price) or `promotional` (event price, usually with conditions) |
| vat | `excluded`, `included` or `unknown` as stated by the clinic |
| source_url | The clinic page the price was read from |
| archived_copy_url | Wayback Machine copy of the source page, where one exists (584 rows) |
| first_seen | First day our monitor read this price |
| last_checked | Last day the price was read on the source page |

## How the data is collected

- A monitor re-reads each clinic's price page daily. A price changes in this file only when the printed figure changes.
- A row is dropped when its figure disappears from the source page on two consecutive checks.
- Only active rows are included. Rows we could not re-confirm, superseded rows and rows for merged/duplicate clinics are left out.
- Rows whose source page sits on a different branch than the clinic, or whose branch is unclear, are held back until re-checked.
- A small number of clinics are held out of automated updates and out of this file while their source pages are reviewed by hand.
- Full method: https://gangnamclinicguide.com/how-we-check-prices.html · Change log: https://gangnamclinicguide.com/price-updates.html

## Limits

- Printed prices are not what every patient pays: event conditions, VAT, consultation and add-ons change the total.
- The store is not a census of every clinic in Gangnam; it covers clinics that print prices as text on their websites.
- Specs are not interchangeable (300 shots is not 600). Compare like with like.

## License

**Creative Commons Attribution 4.0 International (CC BY 4.0)** — https://creativecommons.org/licenses/by/4.0/
Attribution: "Gangnam Clinic Guide price store (gangnamclinicguide.com), retrieved <date>".
The prices themselves are facts published by each clinic; the license covers our compilation, ids, normalisation and dates.

## Contact

Corrections: https://gangnamclinicguide.com/contact.html
