# Experiment Log

This file summarizes the main experiments conducted during Kaggle Playground Series S6E4.

## Model Definitions

| Alias | Description |
|---|---|
| S | XGB seed42 original-domain model with low_more_0p030 bias adjustment |
| A | Ensemble of two reproduction models and XGB OTE model |
| xgb_domain | XGBoost model using domain-inspired features |

## Summary

| Model / Method | OOF | Public LB | Private LB | Notes |
|---|---:|---:|---:|---|
| LGB repro | 0.98002 | 0.98005 | 0.98022 | Strong baseline |
| XGB repro | 0.97989 | 0.97955 | 0.97981 | Different feature pipeline |
| XGB seed42 original-domain | 0.98016 | 0.98109 | 0.97996 | Public notebook reproduction |
| S: XGB seed42 low_more_0p030 | 0.98015 | 0.98111 | 0.97995 | Final submission 1: public-oriented single model |
| A: 2-repro + XGB OTE ensemble | 0.98017 | 0.98037 | - | Blend component used with S |
| XGB multiseed tunedavg | 0.97996 | 0.98052 | 0.98005 | Stable but not best |
| XGB multiseed rawavg logodds | 0.98023 | 0.97928 | 0.98027 | Best private candidate, not submitted |
| S + A blend: submission_blend_S0p980_A0p020 | 0.98017 | 0.98110 | 0.97999 | Final submission 2: blend candidate |
| S + xgb_domain blend | 0.98017 | 0.98110 | 0.98003 | Not selected as final submission; slightly better Private LB than final submissions |

## Notes

The strongest Public LB model was not the strongest Private LB model.
This became one of the most important lessons from this competition.
