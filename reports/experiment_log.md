# Experiment Log

This file summarizes the main experiments conducted during Kaggle Playground Series S6E4.

## Summary

| Model / Method | OOF | Public LB | Private LB | Notes |
|---|---:|---:|---:|---|
| LGB repro | 0.98002 | 0.98005 | - | Strong baseline |
| XGB repro | 0.97989 | 0.97955 | - | Different feature pipeline |
| XGB seed42 original-domain | 0.98016 | 0.98109 | - | Public notebook reproduction |
| XGB seed42 low_more_0p030 | 0.98015 | 0.98111 | 0.97999 | Final submitted model |
| XGB multiseed tunedavg | 0.97996 | 0.98052 | - | Stable but not best |
| XGB multiseed rawavg logodds | 0.98023 | 0.97928 | 0.98027 | Best private candidate, not submitted |
| S + A blend | 0.98017 | 0.98110 | - | Did not improve |
| S + xgb_domain blend | 0.98017 | 0.98110 | - | Did not improve |

## Notes

The strongest Public LB model was not the strongest Private LB model.
This became one of the most important lessons from this competition.