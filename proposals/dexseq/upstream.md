# Upstream evidence: DEXSeq

Reviewed: **2026-10-22**.

| Field | Observed evidence |
| --- | --- |
| Package | **DEXSeq**, version **1.58.0** on the [Bioconductor release page](https://bioconductor.org/packages/release/bioc/html/DEXSeq.html) |
| Credit | Simon Anders and Alejandro Reyes; Hugo Gruson is listed as maintainer in the observed metadata |
| License | **GPL (>= 3)**, package-level declaration |
| Canonical source | `https://git.bioconductor.org/packages/DEXSeq`; exact revision remains to be selected |
| Citation | [Package DOI](https://doi.org/10.18129/B9.bioc.DEXSeq); the [vignette](https://bioconductor.org/packages/release/bioc/vignettes/DEXSeq/inst/doc/DEXSeq.html) cites Anders, Reyes and Huber (2012) and relevant DESeq2 work |

The official vignette was inspected for exon counting, the pasilla example, design interactions, dispersion estimation and likelihood-ratio testing. It documents both R preprocessing and the supplied Python scripts. [PyDESeq2 documentation](https://pydeseq2.readthedocs.io/en/latest/) was inspected to distinguish its DESeq2 scope from DEXSeq. [SUPPA2](https://github.com/comprna/SUPPA) provides a related-method comparison.

Preserve source-file notices if adapting the Python scripts or translating R code. Inspect the exact archive and dependencies before choosing a port license; the repository's MIT license cannot relicense GPL-covered material. A newly written implementation still needs a provenance record and a considered license decision.

No upstream code, pasilla data, or reference outputs are included. Before implementation, record `citation("DEXSeq")`, dependency citations, source hashes, and the reuse decision using [PROVENANCE.md](../../PROVENANCE.md).
