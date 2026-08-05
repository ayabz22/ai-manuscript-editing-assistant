# Reviewer Response Drafting

## Scientific Assessment

The reviewer's concern is scientifically valid.

The manuscript describes a two-stage biomarker selection process:

- **Stage 1:** A candidate biomarker panel was pre-specified based on literature review, expert consultation, and biological plausibility (endothelial injury, immune activation, and inflammation). This stage was completed independently of outcome data.
- **Stage 2:** Biomarkers were empirically narrowed based on univariate discrimination and subsequently evaluated in combination with the clinical severity score.

The reviewer's concern primarily relates to the second stage, where biomarker selection and model evaluation were performed on the same analytic dataset without internal validation of the selection process.

---

## Evaluation of the Reviewer's Concern

The reviewer correctly identifies a potential source of optimism bias.

Although the candidate biomarker panel was defined independently of the outcome, the empirical narrowing step (selection of the top-performing biomarkers) was data-driven. Because discrimination and decision-curve performance were subsequently evaluated within the same dataset, the reported performance estimates may be optimistic.

The manuscript already acknowledges optimism for the recursive-partitioning decision tree analysis but does not explicitly extend this limitation to the biomarker-selection process.

---

## Recommended Manuscript Revisions

### Methods

Clarify the two-stage feature selection strategy by explicitly stating:

- Stage 1 consisted of a pre-specified candidate biomarker panel based on literature review, expert consultation, and biological plausibility.
- Stage 2 consisted of empirical biomarker ranking using outcome data, followed by evaluation of the selected biomarkers within the analytic dataset.

---

### Discussion / Limitations

Extend the existing discussion of optimism bias to include the biomarker-selection workflow.

Explicitly acknowledge that discrimination and decision-curve estimates for the biomarker-combined models may be optimistic because feature selection and model evaluation were performed using the same dataset.

---

### Optional Strengthening

If feasible, perform bootstrap internal validation with the entire feature-selection process repeated within each bootstrap sample to estimate optimism-corrected AUC and decision-curve performance.

---

## Scientific Rationale

Selecting variables according to their observed association with the outcome and then evaluating model performance using those same observations can inflate apparent predictive performance.

The pre-specified candidate biomarker panel reduces this concern during the initial selection stage but does not eliminate optimism introduced during the subsequent empirical narrowing process.

Clarifying this distinction improves methodological transparency and better aligns the manuscript with prediction-model reporting standards.

---

## Remaining Concerns

Without bootstrap validation or an independent validation cohort, the magnitude of optimism in the reported discrimination and decision-curve estimates cannot be quantified.

The recommended revisions improve transparency but do not fully eliminate this source of uncertainty.

---

# Draft Reviewer Response

We thank the reviewer for this thoughtful comment.

Biomarker selection in our study followed two distinct stages.

First, a candidate biomarker panel was pre-specified based on literature review and expert consultation, prioritizing biomarkers representing pathogen-agnostic mechanisms associated with severe illness, including endothelial injury, immune activation, and inflammation. This stage was completed independently of outcome data.

Second, within this pre-specified panel, biomarkers demonstrating the strongest univariate discrimination were identified and subsequently evaluated in combination with the LqSOFA score.

We agree that this second, data-driven narrowing step was performed within the same analytic dataset used for subsequent model evaluation. We have revised the Methods section to clarify this analytical workflow and have expanded the Limitations section to acknowledge that the reported discrimination and decision-curve estimates may therefore be optimistic.

Future validation using bootstrap resampling or an independent external cohort will be important to confirm the robustness and generalizability of these findings.

---

## Reviewer Perspective

This is a moderate-to-major methodological concern.

If left unaddressed, reviewers may question the validity of the reported discrimination and decision-curve estimates.

However, transparent clarification of the analytical workflow, together with explicit acknowledgment of potential optimism bias, would likely address the concern without requiring substantial revision, assuming additional internal validation is not feasible.

---

## Additional Observations

Outside the requested review, if bootstrap validation or external validation becomes feasible in the future, reporting optimism-corrected performance estimates would substantially strengthen the manuscript and improve confidence in the reported predictive performance.
