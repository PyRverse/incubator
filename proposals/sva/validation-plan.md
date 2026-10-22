# Validation plan: sva

Status: **planned**. No sva benchmarks or reference outputs have been generated here.

1. Pin the reference R/sva environment and record the exact estimator, full/null design, requested dimension, options, seed, feature filtering, and matrix orientation. Export session information, data hashes, warnings, and failure states.
2. Begin with synthetic matrices containing known covariates and latent factors. Include no unwanted variation, correlated biological and batch effects, constant features, duplicated covariates, small batches, and nonfinite inputs. Distinguish invalid-input behavior from valid numerical results.
3. Evaluate a lawful subset of **bladderbatch**, used by the [sva vignette](https://bioconductor.org/packages/release/bioc/vignettes/sva/inst/doc/sva.pdf), after checking dataset redistribution terms. Keep public accession and preprocessing records; synthetic tests do not replace biological validation.
4. Compare estimated dimension, fitted nuisance subspaces, residualized projections, and downstream inference. Use principal angles or projection-matrix errors for subspaces, with explicit handling of rank differences; raw singular-vector equality is inappropriate under sign/rotation ambiguity.
5. For existing ComBat implementations, audit a separate matrix of options and compare adjusted values, missingness and variance behavior. ComBat-seq needs separate count and biological-model checks; it is not validated by a continuous-data ComBat test.
6. Assess downstream effect estimates, null calibration, FDR, and retained biological signal in simulations with known truth. Retain discrepancies even when final significance calls match.

Set thresholds per observable after examining conditioning and reference variability. Use deterministic tiny cases in CI, and seeded simulation repetitions plus public-data studies in optional benchmark runs. A domain reviewer must approve a bounded validation claim.
