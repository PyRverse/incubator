# sva: unwanted variation and surrogate variables

Status: **Proposed — alternatives and scope audit**

Evidence reviewed: **2026-10-22**

Implementation owner: **unassigned**

The upstream **sva** package estimates surrogate variables for unmodeled variation and includes known-batch adjustment methods. These are different tasks: inferred nuisance covariates are not interchangeable with a corrected expression matrix. The [upstream package page](https://bioconductor.org/packages/release/bioc/html/sva.html) and [vignette](https://bioconductor.org/packages/release/bioc/vignettes/sva/inst/doc/sva.pdf) describe the distinction.

Native Python access could support reproducible analyses without an R runtime, particularly when researchers need nuisance-variable estimation inside a Python workflow. That value must be assessed against existing software.

**ComBat is already available in Python.** [Scanpy](https://scanpy.readthedocs.io/en/latest/api/generated/scanpy.pp.combat.html) exposes ComBat, and [InMoose](https://github.com/epigenelabs/inmoose) provides ComBat and ComBat-seq. A new repository duplicating those functions is not the default recommendation.

The initial proposal is to map function-level coverage of surrogate-variable estimation, including model handling and reference validation, and to identify useful contributions to existing projects. No comprehensive gap or Python/R equivalence has been established. A limited search cannot establish absence.

Next: build a documented feature matrix covering `sva`, `svaseq`, surrogate-variable number estimation, ComBat options, and ComBat-seq. Select one scientifically useful gap only after that review.

[Feasibility](feasibility.md) · [Validation plan](validation-plan.md) · [Upstream evidence](upstream.md)
