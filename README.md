# 🕊️ Conflict Resolution Thesis
### Peace Treaties, Armed Conflict Termination & Resolution Success Rates (1950s–2020s)

> **Research Repository** — Quantitative & Qualitative Analysis of Peace Agreement Trends, Conflict Termination, and Treaty Durability  
> **Primary Datasets**: UCDP · PRIO · PA-X · PAM · UN Peacemaker

---

## 📊 Key Statistical Findings & Calculated Decadal Trends

Data synthesized from the **Uppsala Conflict Data Program (UCDP)** Conflict Termination Dataset (v3-2021), Peace Agreement Dataset (v22.1), **Peace Research Institute Oslo (PRIO)**, the **Institute for Economics and Peace (IEP)** Global Peace Index 2024, and **USIP** (*Peacemaking in Crisis*, 2025).

### 1. Conflict Termination Share by Decade

| Decade | Peace Agreement % | Decisive Victory % | Low Activity / Frozen % |
|:------:|:-----------------:|:------------------:|:-----------------------:|
| 1950s  | ~8.0%             | ~55.0%             | ~25.0%                  |
| 1970s  | **15.0%** *(peak)*| **49.0%**          | ~35.0%                  |
| 1990s  | ~24.0% *(post-CW)*| ~28.0%             | ~42.0%                  |
| 2010s  | **5.0%**          | **9.0%**           | **65.0%**               |

### 2. Calculated Percentage Trend Changes across Decades

All trend changes were calculated using standard decadal baseline comparison formulas: `((Value_end - Value_baseline) / Value_baseline) * 100`:

| Indicator / Metric | Baseline Period | Recent Period (2010s) | Percentage Change |
|:-------------------|:---------------:|:---------------------:|:-----------------:|
| **Peace Agreements as % of Conflict Endings** | 15.0% (1970s peak) | 5.0% | **−66.67%** |
| **Peace Agreements (Long-Run GPI Share)** | 23.0% (1970s) | 4.0% | **−82.61%** |
| **Decisive Military Victories (Overall)** | 49.0% (1970s) | 9.0% | **−81.63%** |
| **Decisive Victories (Combined Baseline)** | 55.0% (1950s) | 15.0% | **−72.73%** |
| **Government Military Victories** | 30.0% (Cold War) | 10.0% | **−66.67%** |
| **Rebel / Non-State Actor Victories** | 35.0% (Cold War) | 5.0% | **−85.71%** |
| **Low-Activity / Frozen Conflict Outcomes** | 25.0% (1950s) | 65.0% | **+160.00%** |
| **Post-Cold War Peace Agreement Surge** | 8.0% (Cold War avg) | 24.0% (Early 1990s) | **+200.00%** |

---

## 🗄️ Primary Datasets & Sources

| Dataset | Provider / Citation | Coverage | Focus & Link |
|:--------|:--------------------|:--------:|:-------------|
| **UCDP/PRIO Armed Conflict Dataset** (v23.1) | Uppsala University & PRIO (Gleditsch et al.) | 1946–present | Conflicts with ≥25 battle-related deaths/yr; [ucdp.uu.se](https://ucdp.uu.se/downloads/) |
| **UCDP Conflict Termination Dataset** (v3-2021) | Joakim Kreutz, *Journal of Peace Research* | 1946–2021 | Precise start/end dates and termination modes (victory, agreement, ceasefire, low activity) |
| **UCDP Peace Agreement Dataset** (v22.1) | UCDP (Högbladh) | 1975–2021 | Full dyadic agreement texts, provisions, and actor signatures |
| **PA-X Peace Agreements Database** (v9) | PeaceRep, Univ. of Edinburgh (Bell et al.) | 1990–2024 | 2,144+ agreements across 170+ peace processes coded for 200+ substantive provisions |
| **Peace Accords Matrix (PAM)** | Kroc Institute, Notre Dame (Joshi et al. 2025) | 1989–2021 | Quantitative longitudinal implementation monitoring of 51 comprehensive agreements |
| **PRIO-GRID** | Peace Research Institute Oslo (Tollefsen et al.) | 1946–present | Gridded spatial-temporal data (0.5° × 0.5°) for conflict location analysis |
| **UN Peacemaker Database** | United Nations Department of Political Affairs | 1945–present | Over 1,300 full peace agreement legal documents & mediation guidance |

---

## 🔧 Recommended Open-Source GitHub Repositories & Tooling

| Repository | Focus & Description | Language | Link |
|:-----------|:--------------------|:--------:|:-----|
| **`svmiller/peacesciencer`** | Premier R package for quantitative peace science: builds dyad-year and state-year panel frames; merges UCDP, PRIO, and COW conflict data. | R | [GitHub](https://github.com/svmiller/peacesciencer) |
| **`tlscherer/UCDPtools`** | Direct R wrapper for programmatic retrieval of UCDP datasets (`getUCDP("Agreement")`, `getUCDP("ArmedConflict")`) and codebooks. | R | [GitHub](https://github.com/tlscherer/UCDPtools) |
| **`guyschvitz/ucdp.api`** | R client providing seamless API queries directly into the Uppsala Conflict Data Program REST API. | R | [GitHub](https://github.com/guyschvitz/ucdp.api) |
| **`jsks/fc-onset`** | Research replication repository modeling frozen civil conflicts using UCDP Termination Data and Bayesian survival analysis in Stan. | R / Stan | [GitHub](https://github.com/jsks/fc-onset) |
| **`tdballesteros/conflict-relapse`** | Empirical replication analyzing armed conflict relapse hazards following peace settlements using UCDP survival pipelines. | R | [GitHub](https://github.com/tdballesteros/conflict-relapse) |
| **`peacerep/pax-map`** | Interactive spatial visualization tool for the PA-X Peace Agreements Database. | JavaScript | [GitHub](https://github.com/peacerep/pax-map) |

---

## 📋 Research Task Tracker (Issues)

- **Phase 1: Literature Review** — Issue #1: Theoretical foundations (bargaining theory, credible commitment, frozen conflicts)
- **Phase 2: Data Acquisition & Pipeline** — Issue #2: Scraping, cleaning, merging UCDP, PA-X, PAM, and PRIO datasets
- **Phase 3: Exploratory Analysis & Visualization** — Issue #3: Decadal trend statistics, termination distributions, Kaplan-Meier curves
- **Phase 4: Statistical Modeling** — Issue #4: Multinomial logit termination models, Cox PH survival analysis, provision efficacy
- **Phase 4: Qualitative Case Studies** — Issue #5: Comparative case studies (Colombia 2016, Syrian stalemate, Northern Ireland 1998)
- **Phase 5: Thesis Writing & Assembly** — Issue #6: Drafting Chapters 1–7, formatting, and submission

---

## 📁 Repository Directory Structure

```text
conflict-resolution-thesis/
├── README.md                          # Thesis overview, datasets, statistics, roadmap
├── data/
│   ├── raw/                           # Raw downloads (UCDP, PA-X, PAM)
│   ├── processed/                     # Merged analysis-ready panel datasets
│   └── codebook.md                    # Variable operationalization and definitions
├── scripts/
│   ├── 01_data_acquisition.R          # API fetching & downloading scripts
│   ├── 02_data_cleaning.R             # Peacesciencer dyad-year merging & filtering
│   ├── 03_exploratory_analysis.R      # Decadal calculations & visualization generation
│   ├── 04_survival_models.R           # Cox PH and Weibull peace duration models
│   └── 05_multinomial_logit.R         # Conflict termination choice models
├── figures/                           # High-resolution publication plots (PDF/PNG)
├── tables/                            # Regression LaTeX tables and CSV summaries
├── cases/                             # Qualitative case study notes and process-tracing
│   ├── colombia_farc_2016.md
│   ├── northern_ireland_1998.md
│   └── syria_frozen_conflict.md
├── literature/                        # Annotated bibliography and synthesis notes
└── chapters/                          # Draft chapters (Ch. 1 to Ch. 7)
```
