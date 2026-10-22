# Validation plan

Status: planned; no reference outputs or benchmark results exist for this proposal yet.

1. Pin R, Bioconductor, package and dependency versions; retain session information, platform, BLAS, RNG settings, warnings, scripts, hashes, and input/output identifiers.
2. Define deterministic synthetic cases and biologically relevant datasets with access and redistribution terms.
3. Export both intermediate and final outputs, including failures and missing values. Define orientation, types, ordering, contrasts, and preprocessing.
4. Choose output-specific tolerances and justify them empirically. Define exact comparisons for discrete outputs and appropriate invariances for nonidentifiable parameters.
5. Evaluate convergence, calibration, effect estimates, p-values, multiple testing, and decisions in addition to numeric error.
6. Separate small CI fixtures from larger optional experiments. Document expected resources and acceptance criteria before interpreting results.

Include degenerate inputs, invalid designs, near-boundary cases, and reproducibility across supported platforms. Record discrepancies and expert review before making a validation claim.
