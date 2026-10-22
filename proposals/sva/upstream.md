# Upstream evidence: sva

Reviewed: **2026-10-22**.

| Field | Observed evidence |
| --- | --- |
| Package | **sva**, version **3.60.0** on the [Bioconductor release page](https://bioconductor.org/packages/release/bioc/html/sva.html) |
| Authorship | Jeffrey T. Leek, W. Evan Johnson, Hilary S. Parker, Elana J. Fertig, Andrew E. Jaffe, Yuqing Zhang, John D. Storey, Leonardo Collado Torres, as listed in package metadata |
| License | **Artistic-2.0**, package-level declaration |
| Canonical source | `https://git.bioconductor.org/packages/sva`; choose and record an exact reference revision before implementation |
| Citation | [Package DOI](https://doi.org/10.18129/B9.bioc.sva); also run `citation("sva")` in the pinned environment and cite the relevant SVA, ComBat, or ComBat-seq method paper |

The [official vignette](https://bioconductor.org/packages/release/bioc/vignettes/sva/inst/doc/sva.pdf) was inspected for workflows, model specification, the bladderbatch example, and the distinction between nuisance covariates and direct adjustment. [Scanpy's API](https://scanpy.readthedocs.io/en/latest/api/generated/scanpy.pp.combat.html) and [InMoose's repository](https://github.com/epigenelabs/inmoose) were inspected for existing Python coverage.

Before reuse, inspect the selected archive's license text and file headers and inventory dependency licenses, including routines inherited from other statistical packages. Artistic-2.0 has conditions; the incubator's MIT license does not replace them. Data terms require a separate review.

No upstream source code or data is included in this proposal. No source-independent implementation or clean-room process is claimed. Use [PROVENANCE.md](../../PROVENANCE.md) as guidance when opening an implementation project.
