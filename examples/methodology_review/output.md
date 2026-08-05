# Methodology Review

## Scientific Assessment

The overall pipeline (univariate screening → ML-based importance cross-check → combination with severity scores → multivariable evaluation) is a reasonable general strategy. However, several methodological details require clarification to fully assess validity and reproducibility. The description also raises a potential data leakage concern that would be a major issue if not addressed in the underlying analysis.

> **Review Note:** The concerns below are classified based on the information provided in the excerpt. Missing reporting should not be interpreted as evidence that a method was or was not performed.

---

## Methodological Strengths

- Uses a structured, multi-stage feature selection strategy rather than relying on a single algorithm.
- Combines traditional statistical modeling with machine learning–based feature ranking.
- Evaluates multiple aspects of model performance, including discrimination, calibration, and classification metrics.
- Retains an interpretable final prediction model through logistic regression.

---

## Major Concerns

### 1. Feature Selection and Model Evaluation

It is not stated whether feature selection (univariate logistic regression, Random Forest, and XGBoost importance) was performed independently from final model evaluation.

If biomarkers were selected using the full dataset and then evaluated on the same observations, performance estimates (AUC, calibration, NRI) may be optimistically biased due to data leakage.

**Clarification Needed**

- Was feature selection nested within cross-validation?
- Was a separate training/test split or external validation cohort used?

---

### 2. Undefined Selection Criteria

Terms such as:

- "highest individual discrimination"
- "consistently ranked highly"
- "top three biomarkers"

are not quantitatively defined.

Without prespecified selection criteria, the pipeline is difficult to reproduce and may be vulnerable to data-driven selection.

---

### 3. Sample Size and Model Stability

The excerpt does not report:

- sample size
- number of outcome events
- events per variable (EPV)

These values are important for assessing the stability of the final multivariable logistic regression models.

---

### 4. Validation Strategy

The excerpt describes 5-fold cross-validation for biomarker screening but does not specify how the final multivariable models were internally or externally validated.

Clarifying the validation strategy would strengthen confidence in reported model performance.

---

## Moderate Concerns

The excerpt does not specify:

- which Random Forest/XGBoost importance metric was used (e.g., impurity-based vs. permutation importance)
- whether multicollinearity among biomarkers was assessed
- how missing data were handled
- how probability thresholds for sensitivity and specificity were selected
- which calibration method was used
- whether multiple candidate biomarker–severity score combinations were evaluated and, if so, how the final model was selected

---

## Minor Considerations

- Continuous NRI has recognized statistical limitations and should ideally be interpreted alongside complementary performance metrics.
- As a clinical prediction model, compliance with the TRIPOD reporting guideline should be verified before submission.

---

## Recommended Revisions

To improve transparency and reproducibility, consider:

- describing the feature selection and validation workflow in greater detail
- defining quantitative biomarker selection criteria
- reporting sample size and outcome event count
- specifying feature importance metrics
- describing calibration and threshold-selection methods
- documenting missing-data handling

---

## Remaining Uncertainty

Several methodological details are not described in the provided excerpt.

These are classified as **clarification requests** rather than confirmed methodological flaws. Additional information would be required to determine whether the concerns identified represent true analytical limitations or simply incomplete reporting.

---

## Reviewer Perspective

A statistical reviewer would likely focus first on whether feature selection was performed independently from model evaluation, as this directly affects confidence in reported performance metrics.

The remaining concerns are primarily related to reporting transparency and reproducibility and would likely be addressed through methodological clarification during peer review.

---

## Additional Observations

Outside the requested scope, consider clarifying whether LODS, qSOFA, and SICK were modeled as continuous or dichotomized variables, as this affects both model interpretation and the calculation of NRI.
