# dengue-hospital-demand-rio
---

# Where Will the Next Dengue Bed Be Needed?
### From city-level forecasts to district-level hospital demand in Rio de Janeiro's public health system (SUS)

**Author:** Carla de Jesus Dutra Paula - B.Sc. in Data Science, Universidade Presbiteriana Mackenzie (Brazil)

**Academic supervision:** Prof. Gustavo Scalabrini Sampaio

**Context:** Applied Project IV (community-outreach/extension course), 2026 - work in progress, final results expected Nov 2026

## Overview
An end-to-end pipeline that turns weekly arbovirus (dengue + chikungunya) forecasts into hospital bed demand,
Normal/Attention/Critical alerts and district-level prioritization for Rio de Janeiro's 10 health planning areas.

## Data (public, 2015–2025)
InfoDengue (case estimates) · Open-Meteo (climate) · SIH-SUS (hospital admissions and length of stay) ·
CNES (SUS bed capacity) · SINAN/Tabnet SMS-Rio (cases by planning area) · Census 2022 (population)

## Key results (rolling-origin validation 2023–2025, no information leakage)
- Seasonal SARIMAX reduced error by **9%** vs. persistence at a 4-week horizon; 80% prediction intervals well calibrated (82–93% coverage)
- Bed-demand forecasts 4 weeks ahead vs. real hospital records: **WAPE 44% vs. 49%** (persistence)
- Flagged both Critical months of the 2024 epidemic in advance
- Most affected planning areas identified in up to **80%** of months
- At the 2024 peak, arboviruses occupied only **~3%** of the city's public clinical and pediatric beds: pressure is localized, not citywide

## Notebooks (in Portuguese)
| Notebook | Content |
|---|---|
| `project_dengue.ipynb` | Project documentation |
| `eda_sarimax.ipynb` | Case forecasting, baselines, walk-forward validation |
| `demand_alert.ipynb` | Bed demand, hospital alerts, planning-area prioritization |

## Next steps
Demand–supply matching between districts and calibration with Rio de Janeiro's Municipal Health Department.
