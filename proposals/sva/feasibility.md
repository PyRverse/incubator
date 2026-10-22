# Feasibility: sva

## Existing implementations

The 2026-10-22 review searched "Python surrogate variable analysis SVA implementations" and "pycombat inmoose combat seq sva", then inspected primary documentation.

| Project | Documented overlap | Review still needed |
| --- | --- | --- |
| [Scanpy ComBat](https://scanpy.readthedocs.io/en/latest/api/generated/scanpy.pp.combat.html) | ComBat with covariate adjustment and AnnData integration | Option-by-option and version-specific reference comparisons |
| [InMoose](https://github.com/epigenelabs/inmoose) | `pycombat_norm` and `pycombat_seq` | Supported options, edge cases, tests, and potential collaboration |

These sources establish substantial existing batch-correction functionality. They do not establish full coverage of every sva function. No claim of a missing whole-package capability follows from this audit.

## Proposed work

Start with a function inventory and executable fixtures, not a package-wide translation. If a distinct gap remains, scope one surrogate-variable estimator with explicit full/null design matrices and a fixed requested dimension before adding automated dimension estimation.

Anticipated numerical risks are rank decisions, singular-value degeneracy, iterative weighting, convergence thresholds, and random resampling. An estimated subspace can agree while individual basis vectors differ by sign or rotation. Biological and batch effects can be confounded; matching a reference cannot make an unidentifiable design informative. The [upstream vignette](https://bioconductor.org/packages/release/bioc/vignettes/sva/inst/doc/sva.pdf) is the starting scientific specification.

Effort is **moderate to high**, provisionally: an alternatives audit and fixtures are bounded tasks; validating latent-variable estimation requires statistical review and simulation work. No delivery date or maintainer commitment exists.

The upstream declaration is **Artistic-2.0**. Choose any implementation license only after reviewing reused source, notices, and dependencies; see [upstream.md](upstream.md). Proceed only if an unmet use case, reviewer, and maintained implementation path are identified.
