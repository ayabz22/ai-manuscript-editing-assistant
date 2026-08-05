# Statistical Review

## Scientific Assessment

The reported effect sizes (AUC 0.84 → 0.88, continuous NRI 0.85) are presented without the statistical context needed to support them, and the concluding statement overstates what these metrics can establish.

> **Review Note:** The concerns below are based on the information provided in the excerpt. Missing statistical details are classified as clarification requests rather than confirmed flaws.

---

## Statistical Strengths

- Reports discrimination using AUC.
- Includes a reclassification metric (continuous NRI).
- Compares the biomarker-augmented model against the baseline clinical score.
- Attempts to quantify the incremental value of biomarker addition.

---

## Major Concerns

### 1. Clinical Utility Is Overstated

The statement:

> "The combined model demonstrated excellent clinical utility and should be adopted for clinical decision-making."

is not supported by the reported evidence.

Improved discrimination and reclassification demonstrate predictive performance—not clinical utility.

Clinical adoption typically requires additional evidence, including:

- decision-curve analysis or net benefit,
- external or prospective validation,
- and demonstration that model-guided decisions improve patient outcomes.

---

### 2. Statistical Uncertainty Is Not Reported

The excerpt does not report:

- confidence intervals,
- formal comparison of AUC values (e.g., DeLong's test),
- or confidence intervals for continuous NRI.

Without these, it cannot be determined whether the reported improvement exceeds expected sampling variability.

---

### 3. Continuous NRI Interpretation

A continuous NRI of 0.85 may appear large, but continuous NRI is known to overestimate improvement under certain conditions and should be interpreted cautiously.

To strengthen interpretation, consider reporting:

- confidence intervals,
- event and non-event NRI components,
- and, when clinically relevant, categorical NRI or complementary performance measures.

---

### 4. Validation Context

The excerpt does not specify whether these performance metrics were obtained through internal validation, external validation, or an independent test set.

Without this information, the strength of the conclusions cannot be fully assessed.

---

## Moderate Concerns

The excerpt does not specify:

- whether calibration results were evaluated before making claims about model performance,
- how sensitivity, specificity, PPV, and NPV were calculated,
- whether clinically meaningful probability thresholds were predefined,
- or whether multiple biomarker–severity score combinations were evaluated before selecting the final model.

---

## Recommended Revision

Consider revising the interpretation as follows:

> *The addition of sTREM-1 and IL-8 increased model discrimination from an AUC of 0.84 to 0.88. Formal statistical comparison and confidence intervals should be reported to assess the significance of this improvement. While the combined model demonstrated improved predictive performance, additional validation and clinical utility analyses are required before informing clinical decision-making.*

Also consider:

- reporting confidence intervals for all performance metrics,
- reporting the statistical comparison between AUCs,
- reporting calibration results,
- and presenting continuous NRI alongside complementary measures of model improvement.

---

## Remaining Concerns

The excerpt does not provide sufficient statistical detail to determine:

- whether the reported improvements are statistically significant,
- whether the model was externally validated,
- or whether improved discrimination translates into clinically meaningful benefit.

These are classified as clarification requests rather than confirmed methodological flaws.

---

## Reviewer Perspective

A statistical reviewer would likely question the statement that the model "should be adopted for clinical decision-making," as improvements in AUC and continuous NRI alone do not establish clinical utility.

The absence of confidence intervals and formal statistical comparisons would likely result in a request for revision before publication.

---

## Additional Observations

Outside the requested scope, if multiple biomarker–severity score combinations were evaluated before selecting the final model, clarify whether this comparison was prespecified or exploratory, as this influences interpretation of the reported performance improvements.
