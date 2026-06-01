# Contributors & Work Split

## Team

| Person | Scope | Notebooks |
|--------|-------|-----------|
| rayyan ahemad | Data loading + Cleaning | 01, 02 |
| [Person 2 name] | EDA 1D + EDA 2D | 03, 04 |
| [Person 3 name] | Feature Engineering | 05 |

---

## Setup (everyone does this first)

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/valeurs-foncieres-project.git
cd valeurs-foncieres-project
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Get the data files

Download the 5 yearly files from:
https://www.data.gouv.fr/datasets/demandes-de-valeurs-foncieres

Place them in the `data/` folder:
```
data/ValeursFoncieres-2021.txt
data/ValeursFoncieres-2022.txt
data/ValeursFoncieres-2023.txt
data/ValeursFoncieres-2024.txt
data/ValeursFoncieres-2025.txt
```

> Note: data files are gitignored (too large). Each person needs their own local copy.

---

## Person 1 — rayyan ahemad (Loading + Cleaning)

**Notebooks to run and commit:**
- `notebooks/01_load_and_explore.ipynb`
- `notebooks/02_cleaning.ipynb`

**What this produces:**
- `data/cleaned.parquet` — the cleaned dataset used by everyone else

**After running notebook 02**, share `cleaned.parquet` with persons 2 and 3
(via USB, Google Drive, or any file transfer — it's 348MB, not in git).

**Push when done:**
```bash
git add notebooks/01_load_and_explore.ipynb notebooks/02_cleaning.ipynb outputs/plots/valeur_distribution.png
git commit -m "your message"
git push origin main
```

---

## Person 2 — [Name] (EDA)

**Before starting:** get `cleaned.parquet` from person 1, put it in `data/`

**Notebooks to run and commit:**
- `notebooks/03_eda_1d.ipynb`
- `notebooks/04_eda_2d.ipynb`

**Pull first, then push:**
```bash
git pull origin main
# run the notebooks
git add notebooks/03_eda_1d.ipynb notebooks/04_eda_2d.ipynb outputs/plots/
git commit -m "your message"
git push origin main
```

---

## Person 3 — [Name] (Feature Engineering)

**Before starting:** get `cleaned.parquet` from person 1, put it in `data/`

**Notebooks to run and commit:**
- `notebooks/05_feature_engineering.ipynb`

**Pull first, then push:**
```bash
git pull origin main
# run the notebook
git add notebooks/05_feature_engineering.ipynb outputs/plots/15_saisonnalite.png outputs/plots/15b_jour_semaine.png outputs/plots/16_prix_m2_region.png
git commit -m "your message"
git push origin main
```

---

## Important rules

- Always `git pull` before you start working
- Never push directly if someone else is working at the same time — coordinate
- Do NOT add the `data/` folder to git (files are too large)
- One notebook = one commit minimum, don't batch everything together
