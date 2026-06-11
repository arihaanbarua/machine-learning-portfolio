# STAT 380 Portfolio

A [Quarto book](https://quarto.org/docs/books/) collecting my work for **STAT 380 — Data Science** at Penn State. It combines three problem sets and five machine-learning assignments into a single navigable book, with every figure rebuilt as an interactive [plotly](https://plotly.com/) visualization and a plain-language explanation of the analysis.

📖 **Live book:** https://arihaanbarua.github.io/stat380-portfolio/

## Contents

### Part I — Regression & Statistics (R)
- **Problem Set 3** — Lahman baseball career records (`dplyr` aggregation)
- **Problem Set 4** — Insurance charges, used-car pricing, NOVA housing EDA & multiple regression
- **Problem Set 6** — MLB salary (LASSO & backward elimination), linear regression vs kNN, NOVA housing kNN

### Part II — Machine Learning (Python)
- **Gaussian Naïve Bayes** — Iris classification implemented from scratch
- **Neural Network** — Dry Bean classification with `MLPClassifier`
- **Random Forest** — Gini impurity & feature-importance comparison
- **ROC & K-Fold** — Taiwanese bankruptcy prediction with cross-validation
- **Decision Trees** — Breast-cancer diagnosis & information gain

## Project structure

```
.
├── _quarto.yml            # Book configuration
├── index.qmd              # Landing page / overview
├── chapters/              # One self-contained chapter per assignment
│   ├── 01-ps3-baseball.qmd
│   ├── 02-ps4-regression.qmd
│   ├── 03-ps6-models.qmd
│   ├── 04-naive-bayes.qmd
│   ├── 05-neural-network.qmd
│   ├── 06-random-forest.qmd
│   ├── 07-roc-kfold.qmd
│   └── 08-decision-trees.qmd
├── Files/                 # Datasets + original problem-set submissions (notebooks, PDFs)
└── _book/                 # Rendered HTML output (git-ignored)
```

## Building locally

This book mixes **R** (via the knitr engine) and **Python** (via [reticulate](https://rstudio.github.io/reticulate/)). You'll need:

- **Quarto** ≥ 1.4
- **R** with: `dplyr`, `tidyr`, `Lahman`, `glmnet`, `MASS`, `FNN`, `ggplot2`, `plotly`, `scales`, `reticulate`
- **Python** with: `numpy`, `pandas`, `scikit-learn`, `plotly`, `statistics`, and optionally `ucimlrepo`

Render the whole book:

```bash
quarto render
```

Preview with live reload:

```bash
quarto preview
```

The machine-learning chapters pull benchmark datasets from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/); each includes a `scikit-learn` or direct-download fallback so the book still renders if the UCI API is unreachable.

## Author

**Arihaan Barua** — Penn State, STAT 380
