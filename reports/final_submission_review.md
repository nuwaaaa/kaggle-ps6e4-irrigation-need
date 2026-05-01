# Final Submission Review

## Final Result

- Final rank: 524 / 4315
- Best submitted Private LB: 0.97999
- Best private candidate not submitted: 0.98027

## Submitted Main Model

The final submitted model was based on a seed42 XGBoost model with a low-bias adjustment.

| Model | OOF | Public LB | Private LB |
|---|---:|---:|---:|
| seed42 low_more_0p030 | 0.980147 | 0.98111 | 0.97999 |

This model had a strong Public LB, but its Private LB was lower than expected.

## Best Private Candidate Not Submitted

| Model | OOF | Public LB | Private LB |
|---|---:|---:|---:|
| multiseed rawavg logodds | 0.980229 | 0.97928 | 0.98027 |

This model had a much lower Public LB, but its Private LB was the best among my candidates.

## Reflection

I noticed that the Public LB score of the submitted model was unusually high compared to its OOF score.
However, I did not fully account for this gap when selecting final submissions.

In future competitions, I will separate final submissions into:

1. Public LB oriented candidate
2. Private-oriented candidate selected by OOF, fold stability, seed stability, and model diversity