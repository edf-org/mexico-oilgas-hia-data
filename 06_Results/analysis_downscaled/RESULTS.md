# Air-pollution attributable health burden in Mexico, 2024 — Final results

Downstream analysis (tables, charts, maps, monetization, equity) built directly on the
authoritative municipality-level results, with NO₂ and O₃ concentrations in µg/m³ (ppb→µg/m³
conversion applied to NO₂, O₃, and the GBD O₃ endpoint) and the Zheng 2021 O₃ asthma-ED CRF.

> **Scenarios.** Headline figures are all-source (with-O&G) burden. The oil & gas contribution
> (Section 3) is the significance-restricted with-O&G minus no-O&G difference, NO₂ + PM₂.₅ only.

---

## Headline (2024)

- **PM₂.₅ all-cause mortality: 75,961**, incl. 31,576 cardiovascular.
- **NO₂ all-cause mortality: 31,525**.
- **O₃ respiratory mortality: 25,116** (Kasdagli 2024); O₃ COPD 5,678 (GBD 2021).
- **PM₂.₅ pediatric asthma incidence: 21,406**.

---

## 1. National mortality (all combinations)

| Pollutant | Cause | Age | CRF | Baseline | Attributable | 95% CI | AF % | Rate/100k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| NO₂ | All-cause | Adults 25+ | Kasdagli 2024 | 677,132 | 31,525 | 19,579–42,688 | 5 | 41 |
| NO₂ | Cardiovascular disease | Adults 25+ | Kasdagli 2024 | 221,470 | 10,027 | 6,228–15,263 | 5 | 13 |
| NO₂ | Ischemic heart disease | Adults 25+ | Kasdagli 2024 | 136,628 | 5,971 | 3,708–9,094 | 4 | 8 |
| NO₂ | COPD | Adults 25+ | Kasdagli 2024 | 18,490 | 763 | 396–1,104 | 4 | 1 |
| O₃ | Respiratory disease | Adults 25+ | Kasdagli 2024 | 65,127 | 25,116 | 11,711–34,870 | 39 | 32 |
| O₃ | COPD | Adults 25+ | Kasdagli 2024 | 18,490 | 8,189 | 4,757–9,940 | 44 | 11 |
| O₃ | COPD | All ages | GBD 2021 | 18,510 | 5,678 | 1,274–8,925 | 31 | 4 |
| PM₂.₅ | All-cause | Adults 25+ | Orellano 2024 | 677,132 | 75,961 | 53,157–97,775 | 11 | 98 |
| PM₂.₅ | Cardiovascular disease | Adults 25+ | Orellano 2024 | 221,470 | 31,576 | 26,113–36,733 | 14 | 41 |
| PM₂.₅ | All-cause | Adults 25+ | EsCHIF + fusion (NL) | 677,132 | 78,322 | 69,423–87,227 | 12 | 101 |

---

## 2. National morbidity

| Pollutant | Cause | Outcome | Age | CRF | Baseline | Attributable | 95% CI | AF % | Rate/100k |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| NO₂ | Asthma | Emergency department visits | Under 20 | Zheng 2021 | 28,568 | 567 | 317–807 | 2 | 1 |
| NO₂ | Asthma | Emergency department visits | All ages | Zheng 2021 | 47,305 | 651 | 376–918 | 1 | 0 |
| NO₂ | Cardiovascular disease | Emergency department visits | All ages | Ugalde 2022 (lag0) | 264,191 | 3,657 | 594–6,379 | 1 | 3 |
| NO₂ | Cardiovascular disease | Emergency department visits | All ages | Ugalde 2022 (lagmax) | 264,191 | 4,763 | 594–8,631 | 2 | 4 |
| NO₂ | Cardiovascular disease | Emergency department visits | All ages | Ugalde 2022 (lagmean) | 264,191 | 4,763 | 594–8,631 | 2 | 4 |
| O₃ | Asthma | Emergency department visits | Under 20 | Zheng 2021 | 28,470 | 2,342 | 541–4,236 | 8 | 5 |
| O₃ | Asthma | Emergency department visits | All ages | Zheng 2021 | 47,142 | 3,474 | 2,208–4,699 | 7 | 3 |
| PM₂.₅ | Asthma | Emergency department visits | All ages | Ru 2023 | 47,305 | 2,452 | 1,520–3,440 | 5 | 2 |
| PM₂.₅ | Cardiovascular disease | Emergency department visits | All ages | Ugalde 2022 (lag0) | 264,191 | 8,751 | 2,573–14,871 | 3 | 7 |
| PM₂.₅ | Cardiovascular disease | Emergency department visits | All ages | Ugalde 2022 (lagmax) | 264,191 | 13,446 | 3,207–23,027 | 5 | 10 |
| PM₂.₅ | Cardiovascular disease | Emergency department visits | All ages | Ugalde 2022 (lagmean) | 264,191 | 11,418 | 325–22,240 | 4 | 9 |
| NO₂ | Asthma | Incidence | Under 20 | Khreis 2017 | 75,434 | 7,633 | 3,452–9,835 | 10 | 18 |
| PM₂.₅ | Asthma | Incidence | Under 20 | Khreis 2017 | 75,434 | 21,406 | 8,055–31,383 | 28 | 49 |
*CVD ED-visit rows (Ugalde 2022) are sensitivity analyses reported across three lag specifications.*

---

## 3. Oil & gas — significance-restricted (secondary)

NO₂ + PM₂.₅ only (O₃ has no significant O&G signal). 'Significant' munis by the *any* rule (≥1 significant AGEB).

| Pollutant | Cause | CRF | Total burden | O&G (significant) | O&G (full country) | Sig. munis |
| --- | --- | --- | --- | --- | --- | --- |
| NO₂ | All-cause | Kasdagli 2024 | 31,525 | +128 | -64 | 813 |
| PM₂.₅ | All-cause | Orellano 2024 | 75,961 | +116 | +77 | 965 |
| PM₂.₅ | All-cause | EsCHIF + fusion | 78,322 | +113 | +30 | 965 |
| PM₂.₅ | Cardiovascular disease | Orellano 2024 | 31,576 | +51 | +36 | 965 |
| NO₂ | Cardiovascular disease | Kasdagli 2024 | 10,027 | +45 | -16 | 813 |
| NO₂ | Ischemic heart disease | Kasdagli 2024 | 5,971 | +29 | -7 | 813 |
| NO₂ | COPD | Kasdagli 2024 | 763 | +2 | -2 | 813 |

---

## Notes

- **Units:** NO₂ and O₃ concentrations are in µg/m³ (ppb→µg/m³ conversion applied to NO₂, O₃, and the GBD O₃ endpoint); PM₂.₅ is natively µg/m³. CRFs are applied per 10 µg/m³.
- **CRFs:** mortality from Kasdagli 2024, Orellano 2024, GBD 2021, and the EsCHIF+fusion non-linear function; morbidity from Zheng 2021 (asthma ED), Ru 2023 (PM₂.₅ asthma ED), Khreis 2017 (pediatric asthma incidence), and Ugalde 2022 (CVD ED, sensitivity, three lags).
- **Baselines:** mortality from the 2024 cause × age municipal death counts; ED-visit and asthma-incidence baselines from the vetted case counts.
- **Oil & gas:** significance-restricted using the *any* rule on the AGEB significance file (≥1 significant AGEB ⇒ municipality counts as significant for that pollutant).
- Source results: `ab_results_downscaled/` (municipality, state, national). Regenerate this analysis via `code/04`–`40`.

