# DEXSeq: differential exon usage

Status: **Research alpha available**

Evidence reviewed: **2026-10-22**

Implementation: **[exonara 0.1.0a1](https://github.com/PyRverse/exonara)**.

The bounded alpha implements two-condition exon-usage inference from prepared counts, including normalization, dispersion estimation and shrinkage with `fitType="mean"`, and likelihood-ratio tests. Genuine R-generated synthetic checks are documented in its [validation evidence](https://github.com/PyRverse/exonara/blob/main/docs/validation.md); they do not establish general equivalence or production readiness.

**DEXSeq** tests changes in relative exon usage using negative-binomial models. This asks a different question from whether a gene's total expression changes. See the [package description](https://bioconductor.org/packages/release/bioc/html/DEXSeq.html) and [official workflow](https://bioconductor.org/packages/release/bioc/vignettes/DEXSeq/inst/doc/DEXSeq.html).

A native Python inference layer could help researchers keep exon-usage analysis in the same environment as preprocessing and downstream analysis. The useful scope must preserve the biological hypothesis and treatment of exon counts relative to other exons in the same gene.

Existing Python work matters: DEXSeq already distributes Python annotation/counting scripts, and [PyDESeq2](https://pydeseq2.readthedocs.io/en/latest/) implements DESeq2. Those are valuable starting points for an audit, but neither observation establishes a complete DEXSeq inference implementation. [SUPPA2](https://github.com/comprna/SUPPA) addresses related splicing and transcript-usage questions with a different method.

The implemented first scope is inference from an explicitly specified exon-count table, gene mapping, and two-condition assignment. Arbitrary designs, default parametric/local dispersion trends, alignment, annotation construction, plotting, and full DEXSeq API coverage remain outside this alpha.

Next: evaluate permitted biological fixtures such as pasilla and broaden independent scientific validation. The synthetic reference checks live with Exonara; the broader plan below includes work beyond current coverage.

[Feasibility](feasibility.md) · [Validation plan](validation-plan.md) · [Upstream evidence](upstream.md)
