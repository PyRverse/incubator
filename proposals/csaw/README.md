# csaw: differential binding with genomic windows

Status: **Proposed — staged feasibility review**

Evidence reviewed: **2026-10-22**

Implementation owner: **unassigned**

**csaw** detects differential binding in ChIP-seq using sliding windows, with normalization and region-level statistical error control. The [official package](https://bioconductor.org/packages/release/bioc/html/csaw.html), [csaw Book](https://bioconductor.org/books/release/csawBook/), and [method paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC4797262/) describe a workflow spanning read counts, statistical tests, and consolidated genomic regions.

A native Python workflow could integrate genomic interval processing and statistical modeling without an R runtime. Its scientific value depends on retaining replicate-aware inference and the correct unit of false-discovery control, rather than merely reproducing a window counter.

Python already supplies relevant components. [pysam](https://pysam.readthedocs.io/en/latest/api.html) reads alignment data; [InMoose](https://github.com/epigenelabs/inmoose) provides edgeR-derived statistics; [MACS3 bdgdiff](https://macs3-project.github.io/MACS/docs/bdgdiff.html) offers a different differential peak workflow. These are component or alternative-method comparisons, not evidence of csaw equivalence.

The first proposed milestone is a counting contract and tiny reference fixtures, followed by an audit of statistical dependencies and region aggregation. A whole-workflow port is a larger research and engineering undertaking.

Next: compare one counting mode exactly, inventory the edgeR/limma/metapod operations needed by one reference workflow, and decide whether existing Python projects can host the missing components. No implementation or benchmark is provided here.

[Feasibility](feasibility.md) · [Validation plan](validation-plan.md) · [Upstream evidence](upstream.md)
