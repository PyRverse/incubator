# satuRn: differential transcript usage

Status: **Proposed — model and calibration review**

Evidence reviewed: **2026-10-22**

Implementation owner: **unassigned**

The upstream package is **satuRn**; `saturn` is only this directory's slug. It models differential transcript usage in bulk and single-cell RNA sequencing with quasi-binomial generalized linear models. The [package page](https://bioconductor.org/packages/release/bioc/html/satuRn.html) describes fitting, testing, and visualization; the [vignette](https://bioconductor.org/packages/release/bioc/vignettes/satuRn/inst/doc/Vignette.html) details the workflow.

A native Python implementation could make within-gene isoform usage analysis easier to integrate with Python transcriptomics workflows. The statistical target is relative usage within a gene, not just differential transcript abundance.

There is existing Python functionality in this area. [SUPPA2](https://github.com/comprna/SUPPA) supports differential transcript usage and splicing using a different approach. A potential satuRn implementation must demonstrate why its particular modeling and calibration are needed rather than claiming that Python has no DTU tools. No complete Python satuRn implementation was established in the sources inspected; this is not an exhaustive absence claim.

The proposed first scope is fitting and testing on a supplied transcript count matrix with fixed gene mapping, design, contrast and filtering. Empirical-null adjustment must be evaluated as part of inference; visualization and optional downstream testing are separate scope decisions.

Next: export intermediate fitting and testing results from the small upstream Tasic example, then assess which numerical components can be reused responsibly. No port, speed result, or parity evidence exists here.

[Feasibility](feasibility.md) · [Validation plan](validation-plan.md) · [Upstream evidence](upstream.md)
