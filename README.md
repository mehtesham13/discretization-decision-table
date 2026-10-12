# Discretization and the DecisionTable Classifier (WEKA)

Does binning continuous attributes help a rule-based classifier? This project tests four versions of the Pima Indians Diabetes dataset with WEKA's DecisionTable classifier and compares their accuracy.

## Setup

- **Tool:** WEKA
- **Data:** `diabetes.arff` (Pima Indians Diabetes, 768 patients, 8 attributes)
- **Classifier:** DecisionTable
- **Evaluation:** 10-fold cross-validation

Discretization methods compared:

1. None (baseline)
2. Unsupervised discretization (equal-width bins, ignores the class label)
3. Supervised discretization (cut points chosen with the class label)
4. PKIDiscretize (proportional k-interval)

## Results

| Dataset version | Correct | Incorrect | Accuracy |
|---|---:|---:|---:|
| Original | 547 | 221 | 71.22% |
| Unsupervised discretize | 556 | 212 | 72.39% |
| Supervised discretize | 585 | 183 | **76.17%** |
| PKIDiscretize | 568 | 200 | 73.95% |

- Supervised discretization gave the best accuracy, five points above the baseline, because its cut points are chosen to separate the classes.
- Every discretized version beat the raw continuous data. DecisionTable builds rules from attribute values, so fewer distinct values make its rules more general.

## Files

| File | Contents |
|---|---|
| `DATA MINING CS619.pptx` | Presentation with WEKA screenshots and results |

## Team

Muhammad Ehtesham, Arifa Farhath, Bhavesh, Shivam, Nitish, Yogesh
