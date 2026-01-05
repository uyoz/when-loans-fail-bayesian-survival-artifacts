# When Loans Fail — Bayesian Discrete-Time Survival Artifacts

This repository contains **derived tabular artifacts** associated with the study:

**_When Loans Fail: Interpretable Bayesian Discrete-Time Survival Modelling with Calibration via Posterior Predictive Checks_**

The materials document the model specification, posterior summaries, covariate effects, and posterior predictive calibration metrics for a Bayesian discrete-time survival analysis of loan default timing.

---

## Contents

The repository includes the following derived artifacts:

- **`model_run_config_public.json`**  
  Public-facing description of the model specification, estimation setup, and reported evaluation metrics.

- **`bayes_discrete_time_summary_full.csv`**  
  Full posterior summary for all model parameters, including baseline month effects, grade-level random effects, variance components, and covariate coefficients.

- **`bayes_top_coefficients_or.csv`**  
  Odds ratios and uncertainty intervals for covariates with the largest absolute posterior mean effects.

- **`bayes_discrete_time_features_used.csv`**  
  List of covariates retained in the reduced feature set used for estimation.

- **`bayes_discrete_time_ppc.csv`**  
  Posterior predictive outputs on a subsample of person-month observations.

- **`table_ppc_metrics.csv`**  
  Summary metrics from posterior predictive checks, including event rates, calibration gaps, and proper scoring rules.

- **`INDEX.yaml`**  
  Machine-readable manifest of repository contents.

---

## Scope

The artifacts support the **Methods, Results, and Discussion** sections of the study by enabling inspection of:

- the discrete-time survival specification,
- posterior uncertainty for baseline hazards, covariate effects, and grade-level heterogeneity,
- and calibration of monthly default probabilities via posterior predictive checks.

The analysis is presented as an **interpretable baseline** for modelling default timing and uncertainty.

---

## Notes on use

- All quantities are reported on the **person-month scale**, consistent with the discrete-time hazard formulation.
- Posterior predictive checks are computed on a capped horizon (t ≤ 36) and a fixed-size subsample for evaluation.
- Reported effects and calibration metrics are intended for interpretation of relative patterns, uncertainty, and time dependence.

---

## Citation

If referencing these artifacts, please cite the associated manuscript.
