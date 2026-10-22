# DEXSeq: differential exon usage

Status: **Proposed — inference scope review**

Evidence reviewed: **2026-10-22**

Implementation owner: **unassigned**

**DEXSeq** tests changes in relative exon usage using negative-binomial models. This asks a different question from whether a gene's total expression changes. See the [package description](https://bioconductor.org/packages/release/bioc/html/DEXSeq.html) and [official workflow](https://bioconductor.org/packages/release/bioc/vignettes/DEXSeq/inst/doc/DEXSeq.html).

A native Python inference layer could help researchers keep exon-usage analysis in the same environment as preprocessing and downstream analysis. The useful scope must preserve the biological hypothesis and treatment of exon counts relative to other exons in the same gene.

Existing Python work matters: DEXSeq already distributes Python annotation/counting scripts, and [PyDESeq2](https://pydeseq2.readthedocs.io/en/latest/) implements DESeq2. Those are valuable starting points for an audit, but neither observation establishes a complete DEXSeq inference implementation. [SUPPA2](https://github.com/comprna/SUPPA) addresses related splicing and transcript-usage questions with a different method.

The proposed first scope is inference from an explicitly specified exon-count table, gene mapping, design and contrast. Alignment, annotation construction, plotting, and full DEXSeq API coverage would remain outside an initial prototype.

Next: identify reusable statistical components, specify the full/reduced exon-usage models, and generate intermediate R outputs on a small pasilla example. No port or parity result exists here.

[Feasibility](feasibility.md) · [Validation plan](validation-plan.md) · [Upstream evidence](upstream.md)
