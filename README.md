# How Honest Is Your Accuracy? Cross-Validation on Brain Data

BMDE 520, McGill University — Challenge 6.

The same model can look better or worse depending only on how it is evaluated. This challenge measures that effect directly by re-scoring one pipeline under five validation schemes.

Every challenge in this series uses the same setup: 100 OASIS-1 subjects,
gray-matter density averaged inside brain-atlas regions, **Part A** predicting
sex (classification) and **Part B** predicting age (regression, Craddock
parcellations at up to 43 resolutions).

## What's here

**Part A — sex classification (tasks 1–5)**
- Logistic regression across atlas resolutions, evaluated with a single hold-out split, **leave-one-out**, **Monte Carlo** (shuffle-split), **stratified Monte Carlo**, and **nested cross-validation** with an inner hyperparameter search (`GridSearchCV`).

**Part B — age regression (tasks 6–10)**
- The same five schemes for **ridge regression** on age, measured with R².

## Files

- `challenge6_andrea_gomez.ipynb` — the full notebook with outputs and plots.

## Data (not included)

Uses **OASIS-1** voxel-based morphometry gray-matter maps (fetched with
`nilearn.datasets.fetch_oasis_vbm`, subject to OASIS's
[data usage agreement](https://sites.wustl.edu/oasisbrains/)), the
**Schaefer 2018** atlas (`fetch_atlas_schaefer_2018`) and the **Craddock
2011/2012** parcellations. None of them are redistributed here; the notebook's
first cells show how each is fetched.

## Author

Andrea Paola Gómez Jaime
