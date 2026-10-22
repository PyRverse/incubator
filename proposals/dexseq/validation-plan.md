# Validation plan: DEXSeq

Status: **Synthetic R checks available in the research alpha.** See [Exonara's validation evidence](https://github.com/PyRverse/exonara/blob/main/docs/validation.md). Current coverage is two-condition inference with `fitType="mean"`; the broader plan below includes remaining work beyond that subset.

Use the [official vignette](https://bioconductor.org/packages/release/bioc/vignettes/DEXSeq/inst/doc/DEXSeq.html) to define an explicit versioned analysis; do not mix historical Python-counting defaults with a newer R preprocessing workflow without checking semantics.

| Layer | Planned comparison |
| --- | --- |
| Input contract | Exon and gene IDs, ordering, exon/other counts, sample metadata, factor levels, design matrices |
| Normalization and dispersion | Size factors, raw estimates, fitted trends, final dispersions, fit diagnostics |
| Model inference | Full/reduced log likelihoods, coefficients where identifiable, convergence, test statistics and degrees of freedom |
| Results | Raw/adjusted p-values, missing-value masks, ranks, effect summaries and threshold-sensitive decisions |

Begin with hand-checkable synthetic genes having two or three exon bins, balanced replicates, and controlled changes in total expression versus usage. Add all-zero exons, one-bin genes, low counts, extreme counts, rank-deficient designs, and a nuisance covariate. Record the reference's actual behavior rather than inventing expected error handling.

The **pasilla** example in the vignette is a biological validation candidate. Review its data terms before redistribution, and store exact annotation and count provenance. Keep a small permitted subset for CI; preserve a script for a fuller optional run.

Pin R, DEXSeq, DESeq2 and dependencies, and retain scripts, session metadata, input hashes, options, warnings and failures. Specify separate tolerance budgets for likelihoods, dispersions and probabilities after inspecting numerical scale. Include p-values near zero and around a prespecified decision threshold. Evaluate null calibration and power on simulations in addition to agreement with one reference dataset. Exonara records tolerances for its existing fixtures; extensions require separate justification.
