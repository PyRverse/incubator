# Validation plan: satuRn

Status: **planned**. No satuRn reference outputs have been generated in this repository.

Use the small **Tasic** count and metadata objects documented in the [official vignette](https://bioconductor.org/packages/release/bioc/vignettes/satuRn/inst/doc/Vignette.html) as a candidate biological fixture. Check data and annotation terms before redistribution. Pin the transcript-to-gene mapping, retained transcript set, design, contrasts and reference version; the vignette contains historical version references, so record the environment actually executed.

Export and compare these layers separately:

- Input transcript/gene identifiers, gene totals, filter masks and model matrices.
- Fitted coefficients and usage estimates, residual degrees of freedom, dispersion estimates and fit status.
- Contrast estimates, standard errors, moderated test statistics and raw p-values.
- Empirical-null fit parameters, adjusted p-values, and each corresponding multiple-testing result.

Do not validate empirical calibration on a handful of transcripts: use a sufficiently large, documented fixture or simulation because the null fit depends on the test-statistic distribution. Test rank changes as well as numerical errors.

Synthetic tests should include unchanged usage with changing gene totals, genuine isoform shifts, zero totals, rare transcripts, single-isoform genes, near-boundary proportions, imbalanced groups, and invalid contrasts. Verify which cases are filtered, rejected, or reported as missing by the selected reference. Include nested/donor designs only within an explicitly supported statistical specification.

Retain R session metadata, dependency versions, seeds, hashes, warnings and convergence failures. Define scale-aware tolerances for each output after investigating numerical stability, and report decision changes around a prespecified threshold. Use simulation repetitions to assess null calibration and FDR, with tiny deterministic checks in CI and larger optional runs. Neither array closeness nor one dataset establishes general scientific validity.
