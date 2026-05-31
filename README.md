# Valeurs Foncières - Data Science Project

French real estate transaction data (2021-2025) from data.gouv.fr

## What this project does
- Load and merge 5 years of property transaction data
- Clean: missing values, nulls, outliers
- EDA: 1D and 2D exploration
- Feature engineering

## Data source
https://www.data.gouv.fr/datasets/demandes-de-valeurs-foncieres

Data files go in `/data/` (not committed — too big, ~2.6GB total)

## Structure
```
notebooks/   - jupyter notebooks, one per step
outputs/     - saved plots and exports
data/        - raw txt files (gitignored)
```

## Steps / roadmap
- [x] Setup project
- [ ] Load data + quick look
- [ ] Cleaning (nulls, types, outliers)
- [ ] EDA 1D (distributions per column)
- [ ] EDA 2D (correlations, relationships)
- [ ] Feature engineering
