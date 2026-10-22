# PyRverse incubator

**The R ecosystem, reimagined for Python.**

Explore, evaluate, and incubate native Python implementations of established scientific methods.

This is the entry point for method proposals. We investigate scientific value, existing implementations, licensing, and validation before committing to a new package. Contributing benchmarks or improvements to an existing Python project can be the best outcome.

## Initial candidates

All four candidates are **research proposals**. No implementation, numerical parity, release, or upstream endorsement is claimed.

| Proposal | Scientific question | Initial direction |
| --- | --- | --- |
| [sva](proposals/sva/) | How can unwanted variation be modeled or adjusted? | Audit surrogate-variable coverage; benchmark existing ComBat implementations. |
| [DEXSeq](proposals/dexseq/) | Does relative exon usage change between conditions? | Scope the exon-usage inference layer, accounting for existing Python preprocessing and DESeq2 implementations. |
| [csaw](proposals/csaw/) | Which genomic regions show differential ChIP-seq binding? | Evaluate window counting, statistical dependencies, and region-level error control separately. |
| [satuRn](proposals/saturn/) | Does transcript usage within a gene change between groups? | Evaluate quasi-binomial fitting and empirical-null calibration against existing DTU methods. |

The `saturn` directory is a URL-friendly slug. The upstream package is spelled **satuRn**.

## Propose a method

1. Read [CONTRIBUTING.md](CONTRIBUTING.md) and check existing proposals and issues.
2. Open a proposal issue with the scientific use case and links to upstream documentation.
3. Copy [the proposal template](templates/proposal/) into `proposals/<slug>/` and complete its four documents.
4. Review the evidence with maintainers and domain reviewers. Record unresolved questions rather than filling gaps with claims.

Statisticians, researchers, original package authors, Python developers, and documentation contributors are welcome. Useful first contributions include verifying one alternative's feature coverage, defining one edge-case fixture, or improving a source citation.

## From proposal to package

**Proposed → Evaluating → Ready for implementation → Graduated**

A proposal can also be deferred, declined, or redirected to an existing project. A maintainer records the decision and rationale in its README. Graduation requires a bounded scientific specification, an alternatives review, a recorded license decision, reproducible reference fixtures, and someone willing to maintain the implementation. The implementation then receives its own repository; this proposal keeps a link and decision history.

The [parity-benchmarks](https://github.com/PyRverse/parity-benchmarks) and [python-port-template](https://github.com/PyRverse/python-port-template) repositories provide shared infrastructure. Passing a generic array comparison does not establish statistical validity.

## Evidence and licensing

The initial review was performed on **2026-10-22**. Each proposal links to primary documentation, identifies known Python overlap, and separates observations from suggested work. Release URLs can change; a future reference run must pin exact package versions and save environment metadata.

Original repository text and templates use the [MIT License](LICENSE). This does **not** determine the license of a future port, grant rights to upstream code or datasets, or relicense linked material. See [PROVENANCE.md](PROVENANCE.md).

PyRverse is an independent community effort. Method names belong to their respective authors; inclusion here does not imply affiliation or endorsement.
