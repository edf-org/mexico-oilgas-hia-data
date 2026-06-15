# Downstream analysis — downscaled results (Mexico 2024)

This folder contains the downstream analysis of the air-pollution attributable health
burden in Mexico for 2024, built directly on the municipality-level attributable results
in [`../ab_results_downscaled/`](../ab_results_downscaled/).

Concentrations for NO₂ and O₃ are in µg/m³ (ppb→µg/m³ conversion applied to NO₂, O₃, and the
GBD O₃ endpoint); PM₂.₅ is natively µg/m³. Concentration–response functions are applied per
10 µg/m³. Headline figures are all-source (with-oil-&-gas) burden; the oil & gas contribution
is the significance-restricted with-O&G minus no-O&G difference (NO₂ + PM₂.₅ only).

## Contents

- `RESULTS.md` — national mortality, morbidity, and oil & gas summary tables.
- `tables/` — national (all combinations, mortality, morbidity) and state mortality CSVs, plus
  the oil & gas significance-restricted contribution.
- `charts/` — national burden bars, municipal distribution CDFs, morbidity burden, oil & gas.
- `maps/muni/` — municipal choropleths (attributable rate and attributable fraction) for the
  primary endpoints.
- `monetization/` — VSL / cost-of-illness valuation (`MONETIZED_RESULTS.md`,
  `LIT_REVIEW_METHODOLOGY.md`, and value CSVs), 2024 USD.
- `equity/` — burden and exposure by CONAPO marginación grade and by demographic subgroup.

National totals in this analysis reproduce the published `*_national_*.csv` figures in
`../ab_results_downscaled/` (aggregated up from the municipality level).
