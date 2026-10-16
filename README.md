# ML-enabled discovery of refractory high-entropy alloys

This repository contains the curated dataset, Jupyter notebooks, trained-model analyses, and generated outputs associated with the manuscript **“Machine learning-enabled discovery of refractory high entropy alloys on curated data.”**

## Repository contents

- `Dataset.csv` — curated dataset containing 675 records and 18 columns.
- `SPSS/` — notebooks for predicting single-phase solid solutions using AdaBoost (ADB), decision tree (DT), extra trees (ETC), Gaussian process classification (GPC), gradient boosting (GB), k-nearest neighbours (KNN), logistic regression (LR), random forest (RFC), support vector machine (SVM), and XGBoost (XGB).
- `SS/GB/` — gradient-boosting analysis for the solid-solution target.
- `Laves/GB/` — gradient-boosting analysis for the Laves-phase target.
- `requirements.txt` — Python packages used for the verification environment.

## Environment

The notebooks were checked with Python 3.11.7 and the package versions recorded in `requirements.txt`.

```bash
python -m venv .venv
python -m pip install -r requirements.txt
jupyter lab
```

Open a notebook from its model directory and run the cells in order. Each directory contains its own `data_process.py`; that helper resolves `Dataset.csv` from the repository root.

## Reproducibility note

The repository preserves the submitted analysis files without changing model outputs. In a verification run using the environment above, the SPSS gradient-boosting notebook produced an F1 score of `0.895809` (0.896 at three decimals), while Fig. 4(a) of the manuscript reports `0.894`. The other checked SPSS model values agreed with the figure at three decimals. This small discrepancy should be reconciled when the final manuscript figure or analysis is updated.

