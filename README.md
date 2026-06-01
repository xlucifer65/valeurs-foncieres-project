# Valeurs Foncières — Data Science Project

French real estate transaction data (2021–2025) from data.gouv.fr  
**~20 million rows across 5 years**

## Data source
https://www.data.gouv.fr/datasets/demandes-de-valeurs-foncieres

## Team
See [CONTRIBUTORS.md](CONTRIBUTORS.md) for setup instructions and work split.

## Notebooks (click to view)

> GitHub sometimes fails to render notebooks — use the nbviewer links below.

| Notebook | Description | Author | View |
|----------|-------------|--------|------|
| 01_load_and_explore | Load 5 years, first look | rayyan | [nbviewer](https://nbviewer.org/github/xlucifer65/valeurs-foncieres-project/blob/main/notebooks/01_load_and_explore.ipynb) |
| 02_cleaning | Missing values, types, outliers | rayyan | [nbviewer](https://nbviewer.org/github/xlucifer65/valeurs-foncieres-project/blob/main/notebooks/02_cleaning.ipynb) |
| 03_eda_1d | 1D distributions per column | person 2 | — |
| 04_eda_2d | 2D relationships between columns | person 2 | — |
| 05_feature_engineering | New features for modeling | person 3 | — |

## Project structure

```
notebooks/    ← analysis notebooks
outputs/plots/← all generated plots (PNG)
data/         ← raw + intermediate files (gitignored, too large)
```

## Roadmap

- [x] Setup + repo
- [x] Load 5 years of data, merge, first look
- [x] Cleaning — nulls, types, outliers, duplicates
- [x] EDA 1D — distributions
- [x] EDA 2D — relationships, correlations
- [x] Feature engineering

## Key findings

- **20.1M rows** after removing null valeur_fonciere (195k dropped)
- **12.7M unique transactions** — DVF format generates avg 1.59 rows per transaction
- Price outliers: flagged with 3x IQR (1.5x was too aggressive, removes 9.4% including valid commercial sales)
- Transaction volume peaked in 2021–2022, clear drop from 2023 (interest rate hikes)
- `nature_culture` (land type) affects price more than expected: AG land median 270k€ vs S (constructible) 185k€
- `jour_semaine` tested and dropped — day of week affects volume but not price
- IDF region is 2–3x more expensive per m² than other regions

## Environment

```bash
pip install -r requirements.txt
```

Python 3.9+, tested with miniconda3.
