# csaw: differential binding with genomic windows

Status: **Research alpha available**

Evidence reviewed: **2026-10-22**

Implementation: **[csawpy 0.1.0a1](https://github.com/PyRverse/csawpy)**.

The bounded alpha covers prepared fragment/window counts, normalization, edgeR legacy QL tests with `robust=FALSE` and `abundance.trend=FALSE`, and region aggregation. Genuine R-generated synthetic checks are documented in its [validation evidence](https://github.com/PyRverse/csawpy/blob/main/docs/validation.md); they do not establish general equivalence or production readiness.

**csaw** detects differential binding in ChIP-seq using sliding windows, with normalization and region-level statistical error control. The [official package](https://bioconductor.org/packages/release/bioc/html/csaw.html), [csaw Book](https://bioconductor.org/books/release/csawBook/), and [method paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC4797262/) describe a workflow spanning read counts, statistical tests, and consolidated genomic regions.

A native Python workflow could integrate genomic interval processing and statistical modeling without an R runtime. Its scientific value depends on retaining replicate-aware inference and the correct unit of false-discovery control, rather than merely reproducing a window counter.

Python already supplies relevant components. [pysam](https://pysam.readthedocs.io/en/latest/api.html) reads alignment data; [InMoose](https://github.com/epigenelabs/inmoose) provides edgeR-derived statistics; [MACS3 bdgdiff](https://macs3-project.github.io/MACS/docs/bdgdiff.html) offers a different differential peak workflow. These are component or alternative-method comparisons, not evidence of csaw equivalence.

The alpha has a counting contract and reference fixtures for its specified statistical and regional workflow. It does not cover BAM parsing, the edgeR v4 default QL method, robust or abundance-trended moderation, or all csaw counting and filtering modes. A complete upstream workflow port remains a larger undertaking.

Next: extend independent region-level calibration and biological validation, and assess the omitted counting/statistical modes separately. The broader plan below includes work beyond the alpha's current coverage; no performance claim is made.

[Feasibility](feasibility.md) · [Validation plan](validation-plan.md) · [Upstream evidence](upstream.md)
