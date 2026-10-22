# Upstream evidence: satuRn

Reviewed: **2026-10-22**.

| Field | Observed evidence |
| --- | --- |
| Package | **satuRn**, version **1.20.0** on the [Bioconductor release page](https://bioconductor.org/packages/release/bioc/html/satuRn.html) |
| Credit | Jeroen Gilis; contributors Kristoffer Vitting-Seerup, Koen Van den Berge, and Lieven Clement |
| License | **Artistic-2.0**, package-level declaration |
| Sources | [statOmics/satuRn](https://github.com/statOmics/satuRn) and `https://git.bioconductor.org/packages/satuRn`; a benchmark revision is not yet pinned |
| Citation | [Package DOI](https://doi.org/10.18129/B9.bioc.satuRn); run `citation("satuRn")` in the pinned environment and retain the relevant method publication |

The [vignette](https://bioconductor.org/packages/release/bioc/vignettes/satuRn/inst/doc/Vignette.html) was inspected for quasi-binomial fitting, contrasts, the Tasic example, empirical p-values, and optional stageR postprocessing. It includes historical version text: the release-page version above is an observation, not a claim that every vignette output was generated with that version.

[SUPPA2](https://github.com/comprna/SUPPA) was inspected for existing Python DTU functionality. Its presence prevents a broad "no Python DTU method" claim, while its different method does not establish satuRn parity.

Inspect the exact source archive and notices before adaptation. Review licenses and provenance for any reused limma or locfdr-related routines as well as dataset terms; dependencies are not covered automatically by a package's top-level declaration. No upstream source, reference outputs, or data are included. The incubator's MIT license applies to original proposal text only. Use [PROVENANCE.md](../../PROVENANCE.md) for an implementation's rights and source record.
