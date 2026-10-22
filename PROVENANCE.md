# Provenance and license decisions

This launch contains original research summaries, proposal templates, and contribution guidance. No upstream statistical source code, dataset, or generated reference output has been imported. Linked documents retain their own terms. The repository's MIT license applies to the original material here; it is not a license recommendation for all future implementations.

## Initial upstream inventory

Metadata checked 2026-10-22. These observations identify review obligations, not a determination that any particular implementation is legally independent.

| Upstream | Version observed on release page | Declared license | Evidence |
| --- | --- | --- | --- |
| sva | 3.60.0 | Artistic-2.0 | [Bioconductor metadata](https://bioconductor.org/packages/release/bioc/html/sva.html) |
| DEXSeq | 1.58.0 | GPL (>= 3) | [Bioconductor metadata](https://bioconductor.org/packages/release/bioc/html/DEXSeq.html) |
| csaw | 1.46.0 | GPL-3 | [Bioconductor metadata](https://bioconductor.org/packages/release/bioc/html/csaw.html) |
| satuRn | 1.20.0 | Artistic-2.0 | [Bioconductor metadata](https://bioconductor.org/packages/release/bioc/html/satuRn.html) |

Inspect the exact source archive and file headers when selecting a reference version. Package-level metadata does not settle every dependency, bundled file, dataset, or publication license. GPL-3 and GPL (>= 3) must not be silently treated as identical declarations.

## Record for an actual port

Create a `PROVENANCE.md` in the implementation repository containing:

- The reference package/version, source URL and commit or archive hash; papers and required citations.
- An algorithm and function inventory mapped to original authors and source files consulted.
- Whether each component is newly implemented from a specification, adapted, copied, or translated; source exposure and any independently authored specifications.
- The applicable license and notices for each reused component and dependency, the proposed repository license, the reviewer, date, and compatibility rationale.
- Dataset access, consent and redistribution terms; transformations, hashes, and references.
- Reference-generation scripts and environments, numerical acceptance criteria, known deviations, and release evidence.

Calling work a "clean-room implementation" is not enough. Document the actual separation between specification and implementation, who saw source, and what was reused; do not retroactively assert separation that did not occur. Resolve uncertain rights before distributing affected material. Scientific attribution remains necessary even where no source code is reused.
