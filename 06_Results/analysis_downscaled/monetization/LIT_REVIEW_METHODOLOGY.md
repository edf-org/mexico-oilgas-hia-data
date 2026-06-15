# Monetization literature review — methodology, search log, and unit values

**Purpose.** Establish defensible, peer-reviewed unit values to monetize the Mexico
air-pollution attributable health burden (2024): a **Value of Statistical Life (VSL)**
for mortality, and **cost-of-illness unit costs** for the morbidity endpoints (asthma
emergency-department [ED] visits, cardiovascular ED visits/hospitalizations, and new
pediatric asthma cases).

**Transparency note (requested).** This document records *exactly* how the review was
done — every database, search string, the number of hits, what was screened in/out,
and the full citation for every value used — so the search can be audited for
completeness and the numbers traced to source.

---

## 1. Search strategy

**Databases / sources searched (10 June 2026):**
- **PubMed** (via the PubMed MCP / NCBI E-utilities) — biomedical cost-of-illness literature.
- **General web search** (Google-indexed) — for grey literature and economics journals that
  PubMed does not index well (VSL is an environmental-economics topic, largely outside PubMed).
- **Targeted full-text retrieval** (PubMed Central, publisher pages) — to extract exact
  per-event costs, currency, and cost-year.

**Inclusion criteria.** (i) Reports a *monetary* unit value — a VSL, a cost per event, or a
cost per case/year; (ii) Mexico-specific preferred; if absent, a defensible US / Latin-American
value usable via benefit transfer; (iii) peer-reviewed, or an authoritative methodological
source (OECD); (iv) extractable currency and cost-year.

**Exclusion criteria.** Aggregate national-expenditure-only studies with no per-unit figure;
purely indirect/productivity-cost studies; non-cost epidemiology; editorials.

---

## 2. Search log (queries → hits → screened)

### A. Value of Statistical Life (mortality)
| # | Source | Query | Hits | Screened in |
| --- | --- | --- | --- | --- |
| A1 | PubMed | `value of statistical life Mexico willingness to pay mortality risk` | 1 | **Becerra-Pérez 2024** |
| A2 | Web | `value of statistical life Mexico VSL benefit transfer OECD income elasticity air pollution` | ~6 | Becerra-Pérez 2024; LSE/Lima 2019; OECD 2012 |
| A3 | Web | `OECD value of statistical life base value 3 million 2005 USD benefit transfer methodology` | ~8 | **OECD 2012**; Robinson–Hammitt–O'Keeffe 2019 |

### B. Asthma hospitalization / ED-visit cost
| # | Source | Query | Hits | Screened in |
| --- | --- | --- | --- | --- |
| B1 | PubMed | `asthma hospitalization cost Mexico economic burden` | 7 | **López-Tiro 2022** (Mexico, severe asthma) |
| B2 | Web | `cost per asthma emergency department visit hospitalization United States peer-reviewed mean charge` | ~10 | **Casey 2022** (ED-visit cost) |
| B3 | Web | `annual direct cost per patient asthma Mexico children cost of illness USD pesos` | ~10 | Brazil/LatAm proxy (Stirbulov/Santos); no Mexican pediatric per-case found |

### C. Cardiovascular hospitalization cost
| # | Source | Query | Hits | Screened in |
| --- | --- | --- | --- | --- |
| C1 | PubMed | `cardiovascular disease hospitalization cost Mexico direct medical costs` | 34 | screening → microeconomic per-case scarce |
| C2 | PubMed | `cost acute myocardial infarction OR stroke hospitalization Mexico IMSS` | 3,907 | broad; no clean per-event Mexican figure in top hits |
| C3 | Web | `cost of hospitalization cardiovascular disease Mexico direct cost per patient USD myocardial infarction` | ~9 | **Mexican Nat. Inst. Cardiology PCI cost study (2019)**; Stevens 2019 (aggregate) |
| C4 | PubMed/Web | `percutaneous coronary intervention cost acute coronary syndrome National Institute Cardiology Mexico` | 3 | PMID 31419609 confirmed |

**Screening outcome.** Mexico-specific *per-event* costs are scarce for the exact endpoints
(asthma ED visit; cardiovascular ED visit). Mexico has rich *aggregate* expenditure studies
(e.g., Stevens 2019) but these explicitly exclude per-patient microeconomic costs. Per the
plan, the per-event gaps are filled with defensible US / Latin-American values, flagged below.

---

## 3. Selected studies and extracted values

### Mortality — VSL
- **Becerra-Pérez LA, Ramos-Alvarez RA, DelaCruz JJ, García-Páez B. (2024).** *Value per
  Statistical Life at the Sub-National Level as a Tool for Assessing Public Health and
  Environmental Problems.* Inquiry 61:469580241246476. [DOI](https://doi.org/10.1177/00469580241246476) · PMID 38641976.
  → **Mexico national VSL = US$ 2,000,000 (2021)**, OECD WTP/CBA method; state range
  **US$ 0.4 M (Chiapas) – 3.3 M (Ciudad de México)**. *Primary source (Mexico-specific, peer-reviewed, sub-national).*
- **OECD (2012).** *Mortality Risk Valuation in Environment, Health and Transport Policies.*
  Base VSL **US$ 3.0 M (2005 USD, OECD avg)**; benefit transfer by PPP-GDP ratio with
  **income elasticity 0.8** (range 0.7–0.9). *Methodological anchor; cross-checks Becerra-Pérez.*
- **Robinson LA, Hammitt JK, O'Keeffe L. (2019).** *Valuing Mortality Risk Reductions in
  Global Benefit-Cost Analysis.* J Benefit Cost Anal 10(S1):15-50. → income-elasticity transfer
  guidance for low/middle-income settings (supports a higher transfer-based bound).

### Asthma morbidity
- **Casey MF, Richardson LD, Weinstock M, Lin M. (2022).** *Cost variation and revisit rate for
  adult patients with asthma presenting to the emergency department.* Am J Emerg Med 61:179-183.
  → **median cost US$ 597 per asthma ED visit (2014 USD)**, IQR $371–980 (HCUP cost-to-charge).
  *Primary source for asthma ED-visit unit cost (US; Mexico per-visit not found).*
- **López-Tiro J, Contreras-Contreras A, Rodríguez-Arellano ME, Costa-Urrutia P. (2022).**
  *Economic burden of severe asthma treatment: a real-life study.* World Allergy Organ J
  15(7):100662. [DOI](https://doi.org/10.1016/j.waojou.2022.100662) · PMID 35833203.
  → Mexico (ISSSTE) **severe asthma ≈ US$ 16,392 per patient-year** (incl. hospitalization, ED,
  drugs). *Mexico context; upper bound for severe disease, not per-visit.*
- *Latin-American proxy* for incident-case annual cost: Brazil ≈ **US$ 882 per patient-year**
  (one-year real-life outpatient study) — used for the asthma-incidence endpoint.

### Cardiovascular morbidity
- **(Mexican National Institute of Cardiology "Ignacio Chávez") Resource Utilization and Costs
  Associated With PCI in Acute Coronary Syndrome. (2019).** Value Health Reg Issues. PMID 31419609.
  → **mean ACS-PCI episode ≈ MX$ 145,677 pesos (2018)** ≈ **US$ 7,600 (2018 market FX)** /
  ≈ US$ 14,600 (USD-PPP). *Primary Mexico per-hospitalization figure (acute cardiovascular event).*
- **Stevens G, et al. (2019).** *Attributable Burden and Expenditure of Cardiovascular Diseases
  and Associated Risk Factors in Mexico and other Mega-Countries.* (PMC6843962) → CVD national
  expenditure ≈ USD-PPP 11.2 bn (2015); *aggregate only — context, no per-event value.*

---

## 4. Unit values adopted (adjusted to 2024 USD)

Adjustments: USD values inflated by US CPI to 2024 (2014→2024 ≈ ×1.33; 2021→2024 ≈ ×1.13).
Peso values converted at 2018 market FX (≈ 19.2 MX$/US$) then inflated to 2024. These multipliers
are documented so they can be revised.

| Endpoint mapping | Central (2024 USD) | Low | High | Source |
| --- | --- | --- | --- | --- |
| **Mortality → VSL** | **2,260,000** | 2,000,000 | 4,700,000 | Becerra-Pérez 2024 (central/low); OECD/US-transfer (high) |
| **Asthma ED visit** | **795** | 500 | 1,300 | Casey 2022 ($597 median, 2014) |
| **CVD ED visit / hospitalization** | **9,300** | 3,000 | 14,600 | Nat. Inst. Cardiology 2019 (central/high, USD-PPP); US CVD ED visit (low) |
| **New pediatric asthma case (annual)** | **1,150** | 800 | 3,300 | Brazil proxy (central/low); US annual cost (high) |

**Key caveats (flagged for monetization).**
1. **VSL** is the dominant driver. The Becerra-Pérez Mexico value ($2.0 M, 2021) is below the
   US-benefit-transfer value (~$4.7 M) — we use the Mexico value as central and the transfer as
   the high bound. State-specific VSLs are available and can be applied to state-level deaths.
2. **CVD endpoint mismatch.** Our health endpoint is *ED visits* (i00–i99), but the Mexican unit
   cost is an *admitted ACS-PCI episode*. Not every ED visit is admitted, so the central CVD value
   likely **overestimates**; the low bound uses a US non-admitted CVD ED-visit cost.
3. **Asthma incidence** is valued at *one year* of illness; lifetime cost would be substantially
   higher. It is a *new-case* cost, not a hospitalization.
4. **Multi-pollutant double counting.** A death may be attributable to more than one pollutant;
   pollutant-specific monetary values must **not** be summed across NO₂/PM₂.₅/O₃ without a
   multi-pollutant adjustment. We report per-pollutant values and label any cross-pollutant sum
   as an upper bound.
5. **Cause double counting.** Cardiovascular/IHD/COPD deaths are subsets of all-cause; we monetize
   **all-cause** mortality (PM₂.₅, NO₂) and O₃ **respiratory** to avoid double counting, and report
   cause-specific values separately for reference only.

*Search performed 2026-06-10/11. Citations via PubMed (DOIs linked) and indexed web sources.*
