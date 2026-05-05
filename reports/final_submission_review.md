# Final Submission Review

## Final Result

- Final rank: 524 / 4315
- Best submitted Private LB: 0.97999
- Best private candidate not submitted: 0.98027

## Final Submissions

My two final submissions were selected mainly based on strong Public LB scores.

| Final Submission | Model | OOF | Public LB | Private LB | Notes |
|---|---|---:|---:|---:|---|
| 1 | seed42 low_more_0p030 | 0.980147 | 0.98111 | 0.97995 | Public-oriented single model |
| 2 | S + A blend: submission_blend_S0p980_A0p020 | 0.980165 | 0.98110 | 0.97999 | Blend candidate; best submitted Private LB |

The single seed42 model had the strongest Public LB among my own candidates, but its Private LB was lower than expected.

The S + A blend slightly improved the submitted Private LB, but it still did not outperform the best private candidate found after the competition.

## Best Private Candidate Not Submitted

| Model | OOF | Public LB | Private LB |
|---|---:|---:|---:|
| multiseed rawavg logodds | 0.980229 | 0.97928 | 0.98027 |

This model had a much lower Public LB, but its Private LB was the best among my candidates.

## Reflection

I noticed that the Public LB score of the seed42 model was unusually high compared to its OOF score.
However, I did not fully account for this gap when selecting final submissions.

The best Private LB candidate, `multiseed rawavg logodds`, had a much lower Public LB and was not selected as a final submission.
This was a clear example where relying too much on Public LB led to a weaker final selection.

In future competitions, I will separate final submissions into:

1. Public LB oriented candidate
2. Private-oriented candidate selected by OOF, fold stability, seed stability, Public-OOF gap, and model diversity