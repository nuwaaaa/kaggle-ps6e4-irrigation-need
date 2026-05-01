# Lessons Learned

## 1. Feature engineering was highly valuable

This competition was especially useful for learning feature engineering and preprocessing techniques.

Important techniques included:

- Domain-inspired features
- Formula-like features
- External original dataset integration
- Categorical interactions
- Numerical rounding features
- Digit-based features
- Binning features
- Target encoding inside CV folds

## 2. Public LB can be misleading

The final best private candidate had a much lower Public LB than the submitted model.

| Model | OOF | Public LB | Private LB |
|---|---:|---:|---:|
| seed42 low_more_0p030 | 0.980147 | 0.98111 | 0.97999 |
| multiseed rawavg logodds | 0.980229 | 0.97928 | 0.98027 |

This showed that a high Public LB should not be treated as the only signal.

## 3. OOF should not be ignored

OOF was not perfectly aligned with the Public LB, but in this case it was more consistent with the Private LB for some models.

## 4. Fold-wise stability should be checked

For future competitions, I will compare:

- OOF score
- fold mean
- fold standard deviation
- fold minimum and maximum
- seed-wise variance
- Public - OOF gap
- prediction distribution
- model diversity

## 5. Final submissions should have different roles

For future competitions, I will use final submissions as:

- Public-best candidate
- Private-oriented candidate based on OOF, fold stability, seed stability, and model diversity

This should reduce the risk of overfitting to the Public LB.