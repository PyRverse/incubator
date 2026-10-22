# Contributing to the incubator

Start with a focused issue or a pull request. You do not need to promise an implementation to help evaluate a method. Follow the [PyRverse code of conduct](https://github.com/PyRverse/.github/blob/main/CODE_OF_CONDUCT.md).

## A useful proposal

Copy all four files in [templates/proposal](templates/proposal/) into a new proposal directory. Use the upstream package's exact name in prose and a stable lowercase directory slug. Mark new proposals `Proposed` and identify an owner only with that person's consent.

Describe the scientific estimand, intended data, target users, and the smallest useful scope. Search upstream documentation, PyPI, relevant scientific Python ecosystems, and source repositories for existing native implementations and wrappers. Record search terms, date, URLs, feature overlap, and uncertainty. A package with a related name is not evidence of equivalent statistics; a failed search is not proof that no implementation exists.

Read the upstream package metadata, manual, vignette, citations, and license. Credit original authors and method publications. Do not copy or translate code until the intended distribution and required notices have been reviewed. Review dependencies and datasets separately. Record the decision using [PROVENANCE.md](PROVENANCE.md).

## Reference and validation work

Specify the exact upstream version, options, input order, design matrix, contrasts, filtering, and outputs. Generate reference outputs by running R and retain the script, session information, seeds, input hashes, warnings, and failed fits. Never relabel Python output as an R reference. Synthetic fixtures are useful for invariants; public biological datasets require independent access and redistribution checks.

Choose tolerances per output from numerical scale and scientific consequences. Compare missingness, convergence, p-values, multiple-testing results, and decisions as well as coefficient errors. Changes to a tolerance need a reason and a reviewed report. Keep tiny deterministic cases in CI and larger biological benchmarks in explicitly triggered runs.

## Review and decisions

Keep documentation edits small enough to review. Check local links and attach primary sources for changed technical claims. A proposal review should address scientific scope, alternatives, licensing, maintainability, and an executable validation plan. Domain expertise is needed before a scientific implementation can be called validated. A maintainer records acceptance, deferral, or redirection with rationale; acceptance is not a release commitment.

Do not include credentials, private patient data, personal contact details, or unverifiable benchmarks. For vulnerability reports, follow the [organization security policy](https://github.com/PyRverse/.github/blob/main/SECURITY.md).
