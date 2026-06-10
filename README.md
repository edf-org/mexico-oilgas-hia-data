# Air pollutant-attributable health burden of the oil and gas sector in Mexico — Data & Results

This repository accompanies the forthcoming manuscript:

> **Estimating the air pollutant-attributable health burden of the oil and gas sector in Mexico using a TROPOMI flux-divergence approach**
>
> M. Omar Nawaz¹, Karla Cervantes², Veronica Southerland³\*, Marlene Cortez Lugo⁴, Daniel L. Goldberg⁵, Sergio Sanchez³, Horacio Riojas Rodriguez⁴
>
> 1. School of Earth and Environmental Sciences, Cardiff University, Cardiff, Wales, UK
> 2. Independent consultant
> 3. Environmental Defense Fund, Washington, DC, USA
> 4. Instituto Nacional de Salud Pública, Cuernavaca, México
> 5. George Washington University, Washington, DC, USA
>
> \* Corresponding author

> **Manuscript status:** in preparation / under review. This citation will be updated with the journal reference and DOI upon publication.

---

## What is in this repository

This repository is the **citable landing page** for the study's inputs and results. Because the full input dataset is approximately **5 GB**, the large raw input files are archived on **Zenodo** (which is designed to host large research datasets and issues a permanent DOI), while this GitHub repository holds the documentation and the compact tabular results.

| Location | Contents |
|---|---|
| **This GitHub repository** | This README (methods + full input-file descriptions), the [`MANIFEST.md`](MANIFEST.md) inventory of every archived file, and the complete **attributable-burden results** in [`06_Results/`](06_Results/). |
| **Zenodo archive** | The full ~5 GB input dataset: risk functions, raw health data, population data, and geographic layers (folders `01`–`05`), plus a copy of these results. |

> **Zenodo DOI:** `10.5281/zenodo.XXXXXXX` *(to be inserted once the Zenodo record is published)*

The **analysis code is intentionally not included here.** This repository documents the inputs and the published results so they can be cited, inspected, and reused; it is not a software release.

---

## Methods summary

The study estimates the air-quality-related health burden attributable to the oil and natural gas (O&G) sector in Mexico. The workflow has four broad stages:

1. **Emissions from space (TROPOMI flux-divergence).** Nitrogen oxide (NOₓ) emissions associated with the oil and gas sector are derived from TROPOMI satellite observations of tropospheric NO₂ using a **flux-divergence** approach, which converts observed column densities and wind fields into a top-down estimate of surface emissions over Mexico's producing regions.

2. **Pollutant concentration surfaces.** The satellite-constrained emissions are translated into ground-level concentration fields for the pollutants of interest — nitrogen dioxide (NO₂), fine particulate matter (PM₂.₅), and ozone (O₃) — and the share of each concentration field attributable to the oil and gas sector is isolated. (These modeled concentration surfaces are described in the manuscript; only the downstream health-assessment inputs and results are archived here.)

3. **Exposure assessment.** Pollutant surfaces are combined with high-resolution population data to produce population-weighted exposure at fine spatial scale. Population counts come from the 2020 INEGI census at the **AGEB** (urban census block-group) level, with demographic structure and projections from CONAPO. Results are aggregated to the **AGEB**, **municipality (municipio)**, and **state (entidad)** levels using the geographic boundary layers in this archive.

4. **Health impact assessment.** Attributable health burden is calculated by combining population-weighted exposure, baseline health rates, and **concentration–response functions (CRFs)**. The CRF library (folder `01_RiskFunctions`) draws on the Global Burden of Disease (GBD 2021/2023 releases), the GEMM/Fusion and eSCHIF+Fusion mortality functions, and outcome-specific functions for morbidity endpoints (e.g., NO₂–asthma, O₃–COPD, short-term cardiovascular and respiratory emergencies). Baseline health data (mortality, hospital discharges, emergency visits, and disease incidence) come from Mexican national health and statistical sources for 2024.

Burden estimates are produced for multiple endpoints — **premature mortality** (linear and nonlinear CRFs), **disease incidence**, and **emergency-room visits (ERV)** — and are reported both **downscaled** and **non-downscaled** (see [Results](#results-06_results)). Quantitative methods, parameter choices, and uncertainty treatment are fully described in the manuscript.

---

## Input file descriptions

The archive is organized into numbered folders. Sizes and a complete file-by-file inventory are in [`MANIFEST.md`](MANIFEST.md).

### `01_RiskFunctions/` (≈1.1 GB)
Concentration–response functions and the supporting literature used to relate pollutant exposure to health outcomes.
- **`Fusion/`** — Fusion exposure–response parameters and 1000-draw uncertainty files (`Fusion Parameters.csv`, `fusion_ncd_lri_1000draws.csv`, `LL Parameters theta eq 97.5.csv`) plus the source papers and the WHO Fusion calculator code.
- **`eschif+fusion/`** — eSCHIF+Fusion non-accidental mortality functions (summarized and 1000-draw), including the raw GitHub-sourced CanCHEC/GEMM parameters and the `Health_burden_Fusion_CanCHEC_GEMM.R` reference implementation.
- **`GBD2021-release2024/`** — Global Burden of Disease 2021 (2024 release) air-pollution risk material: MR-BRT relative-risk curves (mean and draws) for PM₂.₅ (IHD, stroke, COPD, lung cancer, diabetes, LRI, birth weight, gestational age) and for NO₂–asthma and O₃–COPD, plus the GBD report, methods appendices, and burden-by-risk tables.
- **`GBD2023-release2025/`** — placeholder for the corresponding GBD 2023 (2025 release) material.
- **Source literature (PDF)** — peer-reviewed papers underpinning the CRF choices (Burnett 2018 GEMM, Weichenthal 2022 / Marais 2023 eSCHIF, Forastiere 2024, Kasdagli 2024, Ru 2023, Zheng/Zhen 2021 asthma, HRAPIE-2, and a CDMX short-term cardiovascular study).
- **`Linear_CRFs_summary.xlsx`** — consolidated summary of the linear CRFs applied.

### `02_HealthData_raw/` (≈2.1 GB)
Baseline health data for Mexico used to anchor the attributable-burden calculation.
- **`mortality_2024/`** — INEGI registered-deaths microdata for 2024 (`DEFUN_2024`), with catalog and field-descriptor files.
- **`hospital_discharges_2024/`** — hospital discharge records (`Egresos.txt`) with associated diagnoses (`Afecciones`), procedures, and products.
- **`emergencies_2024/`** — emergency-care records (`Urgencias.txt`) with diagnoses, procedures, and medications, plus the database descriptor.
- **`disease_cases/`** — asthma case counts 2020–2024 (`ASMA 2020-2024.xlsx`) and the corresponding data-request documentation.

### `04_PopulationData_raw/` (≈1.3 GB)
Population counts and demographic projections.
- **`PoblacionCenso_INEGI_2020/`** — 2020 INEGI census at the urban-AGEB level: national CSV tables (`conjunto_de_datos_ageb_urbana_NN_cpv2020.csv`) for all 32 states plus the per-state zipped source files.
- **`ProyeccionesPoblacion_CONAPO_1990-2040_mun/`** and **`ProyeccionesPoblacion_CONAPO_2020-2070_mun/`** — CONAPO municipal population projections (quinquennial age groups, demographic indicators, life expectancy, fertility/mortality/migration components) with their data dictionaries.

### `05_Misc/` (≈555 MB)
Geographic boundary layers (ESRI shapefiles: `.shp/.shx/.dbf/.prj/.cpg`) used for spatial aggregation and mapping.
- **`AGEB_layer/`** and **`AGEB_layer_upd/`** — urban AGEB polygons (original and updated).
- **`Municipalities_layer/`** and **`Municipalities_layer_upd/`** — municipal polygons (original and updated).
- **`Entities_layer/`** and **`Entities_layer_upd/`** — state (entidad) polygons (original and updated).

---

## Results (`06_Results/`)

Attributable-burden estimates, provided as CSV tables in two parallel sets: **`ab_results_downscaled/`** and **`ab_results_non_downscaled/`**. Within each set, results are reported at three spatial scales — **national**, **by state (`_by_ent`)**, and **by municipality (`_by_mun`)** — for 2024:

| File prefix | Endpoint |
|---|---|
| `1.Erv_ab_*` | Emergency-room visits attributable burden |
| `3.Incid_ab_*` | Disease incidence attributable burden |
| `4.Mort_ab_*` | Premature mortality attributable burden (linear CRF) |
| `5.Mort_ab_*_nonlinear_*` | Premature mortality attributable burden (nonlinear CRF) |

"Attributable burden" (`ab`) refers to the portion of each health endpoint attributable to oil-and-gas-sector air pollution. The non-downscaled set carries the `_non_downscaled` suffix.

---

## Data sources & attribution

The archived inputs incorporate third-party data that remain subject to their original terms and citation requirements, including:
- **TROPOMI / Sentinel-5P** tropospheric NO₂ (ESA / Copernicus).
- **Global Burden of Disease (GBD 2021/2023)** risk curves — Institute for Health Metrics and Evaluation (IHME).
- **INEGI** — 2020 Population and Housing Census; 2024 mortality, hospital-discharge, and emergency records.
- **CONAPO** — municipal population projections.
- Published concentration–response functions as cited in `01_RiskFunctions/` and in the manuscript.

When reusing these inputs, please cite the original data providers in addition to this archive.

## How to cite

Until the manuscript is published, please cite the Zenodo archive (DOI above). The full bibliographic reference will be added here on publication.

## License

- **Results and documentation** produced by the authors (this README, `MANIFEST.md`, and `06_Results/`) are released under **CC BY 4.0**.
- **Third-party raw inputs** archived on Zenodo remain under the licenses and terms of their respective providers (IHME/GBD, INEGI, CONAPO, ESA/Copernicus, and the cited publications).

## Contact

Corresponding author: **Veronica Southerland**, Environmental Defense Fund — veronica.tinney@gmail.com
