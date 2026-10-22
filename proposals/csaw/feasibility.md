# Feasibility: csaw

## Alternatives audit

The 2026-10-22 review searched "csaw python ChIP-seq differential binding native software" and inspected upstream and component documentation.

| Option | Documented role | Boundary to investigate |
| --- | --- | --- |
| [pysam](https://pysam.readthedocs.io/en/latest/api.html) | SAM/BAM/CRAM access through HTSlib | Alignment access alone does not reproduce csaw counting/filtering semantics |
| [InMoose](https://github.com/epigenelabs/inmoose) | Python implementations of edgeR/limma functionality | Exact algorithm versions, supported options, and end-to-end compatibility |
| [InMoose `glmQLFit` documentation](https://inmoose.readthedocs.io/en/v0.6.0/generated/inmoose.edgepy.glmQLFit.html) | Quasi-likelihood negative-binomial fitting | This inspected page is explicitly version 0.6.0; audit the chosen current version before depending on it |
| [MACS3 bdgdiff](https://macs3-project.github.io/MACS/docs/bdgdiff.html) | Differential peaks from treatment/control tracks | Its documented one-replicate-per-condition limitation differs from replicate-aware csaw inference |

These findings do not establish a complete csaw implementation or rule one out elsewhere.

## Scope and risks

The [csaw Book](https://bioconductor.org/books/release/csawBook/) provides a workflow to decompose into counting, filtering, normalization, modeling, and region summaries. Audit each stage before making a dependency decision.

Anticipated risks include coordinate conventions, read/fragment filtering, paired-end handling, duplicate flags, windows at chromosome boundaries, offset calculation, dispersion moderation, window clustering, and combined p-values. Correct window-level p-values alone do not demonstrate region-level FDR control.

Effort is **high** for a useful subset and **very high** for broad workflow coverage. Begin with synthetic read fixtures and one count-table workflow. Genome-scale I/O and peak memory need separate measurement after correctness. These estimates are qualitative and assume no committed team.

Upstream declares **GPL-3**. Source translation, compiled components, and dependency reuse need an explicit license review. Reusing a Python component requires its own attribution and terms review. Proceed only when a bounded workflow, dependency plan, scientific reviewer, and maintenance owner are identified.
