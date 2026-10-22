# Feasibility: DEXSeq

## Alternatives audit

On 2026-10-22, searches for "Python DEXSeq native implementation exon usage" and the primary project documentation identified the following overlap. This is a scoped audit, not proof that no other implementation exists.

| Existing option | Relevant capability | Boundary |
| --- | --- | --- |
| [DEXSeq's Python scripts](https://bioconductor.org/packages/release/bioc/vignettes/DEXSeq/inst/doc/DEXSeq.html) | Annotation preparation and exon counting | Preprocessing does not supply the R inference pipeline |
| [PyDESeq2](https://pydeseq2.readthedocs.io/en/latest/) | DESeq2 differential expression | Must audit dispersion/model/testing APIs; gene-expression testing is not exon-usage testing |
| [SUPPA2](https://github.com/comprna/SUPPA) | Splicing and transcript-usage analysis | Alternative statistical question/representation; not DEXSeq parity |

## Scientific and engineering work

The [DEXSeq vignette](https://bioconductor.org/packages/release/bioc/vignettes/DEXSeq/inst/doc/DEXSeq.html) describes exon-versus-other-exons counts, design interactions, dispersion estimation and shrinkage, and a likelihood-ratio test. A prototype must reproduce the specified model and preprocessing contract, not simply run a gene-expression test on exon rows.

Anticipated differences include factor coding and rank checks, size-factor estimation, dispersion trends and shrinkage, optimizer stopping criteria, extreme-count likelihoods, and missing p-values. Annotation versions and strand/counting rules can create discrepancies before inference starts.

Effort is **high** for a scientifically reviewed inference subset, with further work for annotation/counting parity and visualization. First perform a component audit, then generate fixtures, then evaluate one narrow prototype. These are provisional effort categories, not schedules.

The upstream declaration is **GPL (>= 3)**. Any copied or translated components require a license and notice review; dependencies may use different licenses. Decide whether to contribute to an existing project before creating a standalone implementation. A go decision needs a domain reviewer, a bounded model specification, and documented rights.
