# Predicting Pollutant Emissions Under Canada’s 2030 Coal Phase-Out Policy

## Project Overview

This project investigates how pollutant emissions from Canada’s fossil-fuel electricity sector may evolve under the federal **2030 coal phase-out policy**.

Using data from Canada’s **National Pollutant Release Inventory (NPRI)**, the project combines exploratory data analysis, time-series feature engineering, and scenario-based modeling to produce **policy-aware emission forecasts**.

Rather than focusing purely on predictive accuracy, the emphasis is on **interpretability, realism, and alignment with regulatory decision-making**.

---

## Policy Context

Coal-fired electricity facilities represent a small fraction of Canada’s reporting facilities, yet they historically contribute a disproportionately large share of air pollutant emissions, particularly SO₂ and NOₓ.

While the coal phase-out policy aims to eliminate coal generation by 2030, emissions do not simply disappear. Capacity is replaced by a mix of lower-emission sources and fossil alternatives, creating transitional dynamics that must be explicitly modeled.

This project explores those dynamics.

---

## Research Questions

- How have emissions from fossil-fuel electricity generation evolved historically?
- How strongly are SO₂ and NOₓ emissions linked to coal-based generation?
- Under a coal phase-out scenario, how might total emissions change over time?
- What assumptions are required to model replacement energy sources transparently?

---

## Data Source

- **National Pollutant Release Inventory (NPRI)**
- Years covered: **2000–2022** (with extended historical context)
- Sector focus: **Fossil-fuel electric power generation**
- Data scope: Facility-level annual pollutant releases

No raw data files are included in this repository at this stage.

---

## Methodology Summary

The analytical workflow follows these high-level steps:

1. **Data preparation and validation**
   - Cleaning and filtering NPRI records
   - Facility and sector-level aggregation
   - Handling missing values and reporting inconsistencies

2. **Exploratory data analysis**
   - Long-term emission trends
   - Coal vs non-coal facility comparisons
   - Pollutant-specific behavior (SO₂, NOₓ)

3. **Time-series feature engineering**
   - Lagged emissions
   - Rolling averages and volatility
   - Year-over-year change and momentum features
   - Policy markers (pre/post policy periods)

4. **Scenario-based modeling**
   - Business-as-usual baseline
   - Manual coal phase-out trajectory
   - Replacement emissions estimation using transparent assumptions

5. **Interpretation and communication**
   - Focus on explainability for non-technical stakeholders
   - Clear articulation of assumptions and limitations

---

## Notebooks

The core analysis is documented in the following notebooks:

- `EDA_Model.ipynb`  
  Exploratory data analysis, trend assessment, and initial modeling experiments.

- `Extra_years_NPRI_Dataset.ipynb`  
  Dataset preparation and extension to support longer-term historical analysis.

These notebooks are intended to be read sequentially.

---

## Assets and Presentations

The `assets/` folder contains visual materials used in multiple academic and stakeholder presentations, including charts and slides derived from the analysis.

Presentation materials are organized chronologically:

```text
assets/
└── slides/
├── presentation_01/
├── presentation_02/
└── presentation_03/
```

Each presentation folder contains exported figures (`.png`) used to communicate findings. These images are shared for illustrative and portfolio purposes only.

---

## Limitations

- Replacement energy sources must be modeled using assumptions rather than direct observations
- Facility reporting practices change over time
- Emissions reductions are influenced by factors beyond coal phase-out alone
- Forecasts represent **scenarios**, not predictions of exact future outcomes

All limitations are explicitly acknowledged in the analysis.

---

## Ethics and Transparency

- No confidential or proprietary data is included
- All assumptions are documented and motivated
- The project prioritizes clarity over model complexity
- Results are framed to support understanding, not overclaim certainty

---

## Repository Structure

```text
npri-coal-phaseout-forecast/
├── README.md
├── assets/
│   └── slides/
│       ├── presentation_01/
│       ├── presentation_02/
│       └── presentation_03/
├── data/
│   └── README.md
├── notebooks/
│   ├── EDA_Model.ipynb
│   └── Extra_years_NPRI_Dataset.ipynb
└── .gitignore

```

## About This Repository

This repository supports a portfolio case study and academic coursework.
It demonstrates analytical reasoning, policy-aware modeling, and data storytelling rather than serving as a production forecasting system.

For a narrative walkthrough of the project and selected visual outputs, see the corresponding portfolio entry on [datascienceportfol.io/paulafrossard/projects](https://www.datascienceportfol.io/paulafrossard/projects/1)
