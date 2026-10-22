# sva: unwanted variation and surrogate variables

Status: **Research alpha available**

Evidence reviewed: **2026-10-22**

Implementation: **[surva 0.1.0a1](https://github.com/PyRverse/surva)**.

The bounded alpha implements iterative reweighted SVA, supervised SVA, the svaseq moderated-log path, and Buja–Eyuboglu permutation dimension estimation. It excludes ComBat and ComBat-seq. Genuine R-generated synthetic checks are documented in its [validation evidence](https://github.com/PyRverse/surva/blob/main/docs/validation.md); they do not establish general equivalence or production readiness.

The upstream **sva** package estimates surrogate variables for unmodeled variation and includes known-batch adjustment methods. These are different tasks: inferred nuisance covariates are not interchangeable with a corrected expression matrix. The [upstream package page](https://bioconductor.org/packages/release/bioc/html/sva.html) and [vignette](https://bioconductor.org/packages/release/bioc/vignettes/sva/inst/doc/sva.pdf) describe the distinction.

Native Python access could support reproducible analyses without an R runtime, particularly when researchers need nuisance-variable estimation inside a Python workflow. That value must be assessed against existing software.

**ComBat is already available in Python.** [Scanpy](https://scanpy.readthedocs.io/en/latest/api/generated/scanpy.pp.combat.html) exposes ComBat, and [InMoose](https://github.com/epigenelabs/inmoose) provides ComBat and ComBat-seq. A new repository duplicating those functions is not the default recommendation.

The initial proposal mapped function-level coverage of surrogate-variable estimation, including model handling and reference validation, and considered useful contributions to existing projects. No comprehensive gap or general Python/R equivalence has been established. A limited search cannot establish absence.

Next: extend independent biological and downstream validation of the supported subset, and keep the alternatives review current. The broader validation plan below remains research work; it is not a claim that every upstream method is implemented.

[Feasibility](feasibility.md) · [Validation plan](validation-plan.md) · [Upstream evidence](upstream.md)
