# Upstream evidence: csaw

Reviewed: **2026-10-22**.

| Field | Observed evidence |
| --- | --- |
| Package | **csaw**, version **1.46.0** on the [Bioconductor release page](https://bioconductor.org/packages/release/bioc/html/csaw.html) |
| Authors | Aaron Lun and Gordon Smyth |
| License | **GPL-3**, package-level declaration |
| Canonical source | `https://git.bioconductor.org/packages/csaw`; choose an exact archive/revision before development |
| Citation | [Package DOI](https://doi.org/10.18129/B9.bioc.csaw) and [Lun and Smyth, csaw method paper](https://pmc.ncbi.nlm.nih.gov/articles/PMC4797262/) |

The [csaw Book](https://bioconductor.org/books/release/csawBook/) was inspected for the workflow, reference data, citations, and use of edgeR. The metadata lists dependencies including edgeR, limma, metapod and alignment/range infrastructure. Inventory the actual functions and exact versions required by the chosen workflow; a dependency's presence does not mean its entire API must be ported.

Primary Python evidence: [pysam API](https://pysam.readthedocs.io/en/latest/api.html), [InMoose repository](https://github.com/epigenelabs/inmoose), and [MACS3 bdgdiff manual](https://macs3-project.github.io/MACS/docs/bdgdiff.html). MACS3 is an alternative-method comparison, not a statistical reference for csaw parity.

Inspect file-level notices, compiled code, dependency licenses, and data terms before reuse. GPL-3 is the observed declaration, not an automatic "or later" grant. The incubator MIT license does not override upstream conditions. No code, BAM files, or generated outputs are included. Record future decisions using [PROVENANCE.md](../../PROVENANCE.md).
