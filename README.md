# Kaggle PS6E4 - Irrigation Need Prediction

This repository summarizes my solution development process for Kaggle Playground Series S6E4: Irrigation Need Prediction.

## Competition

- Competition: Playground Series - Season 6, Episode 4
- Task: 3-class classification
- Target: Irrigation_Need
- Classes: Low, Medium, High
- Metric: Balanced Accuracy

## Result

- Final rank: 524 / 4315
- Best submitted Private LB: 0.97999
- Best private candidate not submitted: 0.98027

## Key Techniques

- Domain-inspired feature engineering
- External original dataset integration
- Target encoding inside cross-validation folds
- Numerical rounding, digit, bin, and interaction features
- Multi-seed XGBoost training
- Log-odds bias calibration
- Ensemble analysis
- OOF / Public LB / Private LB gap analysis

## Main Learning

The most important lesson was that Public LB can be misleading.

| Model | OOF | Public LB | Private LB | Final Submission |
|---|---:|---:|---:|---|
| seed42 low_more_0p030 | 0.980147 | 0.98111 | 0.97995 | Yes |
| S + A blend | 0.980165 | 0.98110 | 0.97999 | Yes |
| multiseed rawavg logodds | 0.980229 | 0.97928 | 0.98027 | No |

The model with the best Private LB had a much lower Public LB and was not selected as a final submission.

For future competitions, I will compare:

- OOF score
- fold-wise variance
- seed-wise stability
- Public - OOF gap
- prediction distribution
- model diversity

## Repository Structure

```text
ps6e4-irrigation-need/

├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   ├── README.md
│   ├── 01_eda_and_feature_inspection.ipynb
│   ├── 02_xgb_domain_features_single_model.ipynb
│   ├── 03_xgb_reproduction_and_bias_tuning.ipynb
│   └── 04_ensemble_and_submission_analysis.ipynb
│
├── reports/
│   ├── experiment_log.md
│   ├── final_submission_review.md
│   └── lessons_learned.md
│
├── src/
│   └── README.md
│
└── outputs/
    └── summary_tables/
        └── README.md

```

## Reports

- [Experiment Log](reports/experiment_log.md)
- [Final Submission Review](reports/final_submission_review.md)
- [Lessons Learned](reports/lessons_learned.md)

## Notebooks

- [Notebook Overview](notebooks/README.md)
- [EDA and Feature Inspection](notebooks/01_eda_and_feature_inspection.ipynb)
- [XGBoost Domain Features Single Model](notebooks/02_xgb_domain_features_single_model.ipynb)
- [XGBoost Reproduction and Bias Tuning](notebooks/03_xgb_reproduction_and_bias_tuning.ipynb)
- [Ensemble and Submission Analysis](notebooks/04_ensemble_and_submission_analysis.ipynb)