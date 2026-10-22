# PyRverse incubator

**The R ecosystem, reimagined for Python.**

Explore, evaluate, and incubate native Python implementations of established scientific methods.

This is the entry point for method proposals. We investigate scientific value, existing implementations, licensing, and validation before committing to a new package. Contributing benchmarks or improvements to an existing Python project can be the best outcome.

## Research alpha implementations

Four bounded **0.1.0a1 research alpha implementations** are available. Each includes genuine R-generated synthetic reference checks. These checks do not establish general scientific equivalence, production readiness, or upstream endorsement.

| Proposal | Implementation | Tested scope |
| --- | --- | --- |
| [sva](proposals/sva/) | [surva](https://github.com/PyRverse/surva) | Iterative reweighted and supervised SVA, svaseq, and Buja–Eyuboglu dimension estimation; no ComBat |
| [DEXSeq](proposals/dexseq/) | [exonara](https://github.com/PyRverse/exonara) | Two-condition exon-usage inference with `fitType="mean"` |
| [csaw](proposals/csaw/) | [csawpy](https://github.com/PyRverse/csawpy) | Window counts, normalization, legacy nonrobust QL tests without an abundance trend, and region aggregation |
| [satuRn](proposals/saturn/) | [saturna](https://github.com/PyRverse/saturna) | Independent bulk DTU fitting, moderation, and empirical-null correction |

The proposal records retain the initial alternatives reviews and broader validation plans; the implementation documents define current coverage. The `saturn` directory is a URL-friendly slug. The upstream package is spelled **satuRn**.

## Propose a method

1. Read [CONTRIBUTING.md](CONTRIBUTING.md) and check existing proposals and issues.
2. Open a proposal issue with the scientific use case and links to upstream documentation.
3. Copy [the proposal template](templates/proposal/) into `proposals/<slug>/` and complete its four documents.
4. Review the evidence with maintainers and domain reviewers. Record unresolved questions rather than filling gaps with claims.

Statisticians, researchers, original package authors, Python developers, and documentation contributors are welcome. Use [Discussions](https://github.com/PyRverse/incubator/discussions) for ideas and questions, and issues for concrete proposals or evidence corrections. Useful first contributions include verifying one alternative's feature coverage, defining one edge-case fixture, or improving a source citation.

## From proposal to package

**Proposed → Evaluating → Ready for implementation → Graduated**

A proposal can also be deferred, declined, or redirected to an existing project. A maintainer records the decision and rationale in its README. Graduation requires a bounded scientific specification, an alternatives review, a recorded license decision, reproducible reference fixtures, and someone willing to maintain the implementation. The implementation then receives its own repository; this proposal keeps a link and decision history.

The [parity-benchmarks](https://github.com/PyRverse/parity-benchmarks) and [python-port-template](https://github.com/PyRverse/python-port-template) repositories provide shared infrastructure. Passing a generic array comparison does not establish statistical validity.

## Evidence and licensing

The initial review was performed on **2026-10-22**. Each proposal links to primary documentation, identifies known Python overlap, and separates observations from suggested work. Release URLs can change; a future reference run must pin exact package versions and save environment metadata.

Original repository text and templates use the [MIT License](LICENSE). This does **not** determine the license of a future port, grant rights to upstream code or datasets, or relicense linked material. See [PROVENANCE.md](PROVENANCE.md).

PyRverse is an independent community effort. Method names belong to their respective authors; inclusion here does not imply affiliation or endorsement.
