# satuRn: differential transcript usage

Status: **Research alpha available**

Evidence reviewed: **2026-10-22**

Implementation: **[saturna 0.1.0a1](https://github.com/PyRverse/saturna)**.

The bounded alpha implements independent bulk DTU fitting, nonrobust moderation without a trend, and empirical-null correction with an independently written optimizer. Genuine R-generated synthetic checks are documented in its [provenance](https://github.com/PyRverse/saturna/blob/main/docs/provenance.md) and [numerical report](https://github.com/PyRverse/saturna/blob/main/reports/validated/parity.md); they do not establish general equivalence or production readiness.

The upstream package is **satuRn**; `saturn` is only this directory's slug. It models differential transcript usage in bulk and single-cell RNA sequencing with quasi-binomial generalized linear models. The [package page](https://bioconductor.org/packages/release/bioc/html/satuRn.html) describes fitting, testing, and visualization; the [vignette](https://bioconductor.org/packages/release/bioc/vignettes/satuRn/inst/doc/Vignette.html) details the workflow.

A native Python implementation could make within-gene isoform usage analysis easier to integrate with Python transcriptomics workflows. The statistical target is relative usage within a gene, not just differential transcript abundance.

There is existing Python functionality in this area. [SUPPA2](https://github.com/comprna/SUPPA) supports differential transcript usage and splicing using a different approach. A potential satuRn implementation must demonstrate why its particular modeling and calibration are needed rather than claiming that Python has no DTU tools. No complete Python satuRn implementation was established in the sources inspected; this is not an exhaustive absence claim.

The implemented first scope is fitting and testing on a supplied transcript count matrix with fixed gene mapping, numeric design and contrast. Empirical-null correction is included. Single-cell inference, repeated-measure correlation, visualization, stageR, and full upstream API coverage remain outside this alpha.

Next: extend independent biological and null-calibration validation within the bulk contract. Single-cell validation is separate future work. The broader plan below includes work beyond the current synthetic checks; no speed claim is made.

[Feasibility](feasibility.md) · [Validation plan](validation-plan.md) · [Upstream evidence](upstream.md)
