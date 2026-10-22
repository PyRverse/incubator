# Feasibility: satuRn

## Existing options

On 2026-10-22, searches for "satuRn Python implementation" and "satuRn python differential transcript usage" were followed by inspection of [upstream documentation](https://github.com/statOmics/satuRn) and [SUPPA2's repository](https://github.com/comprna/SUPPA).

SUPPA2 documents Python workflows for differential transcript usage based on transcript inclusion proportions and expression information. It is a related-method alternative, not evidence that satuRn's quasi-binomial modeling and empirical calibration are already reproduced. An extension to existing software may be preferable to a new package. No comprehensive ecosystem survey or equivalence test has been completed.

## Numerical and statistical work

The [satuRn vignette](https://bioconductor.org/packages/release/bioc/vignettes/satuRn/inst/doc/Vignette.html) documents quasi-binomial fitting, moderated inference, and empirical-null adjustment, with raw and empirically adjusted results. Matching an ordinary binomial GLM alone would not reproduce that inference pipeline.

Anticipated risks include transcript-to-gene mapping, zero gene totals, proportions on boundaries, insufficient residual degrees of freedom, separated or rank-deficient designs, dispersion moderation, and empirical-null fitting. Contrast coding, filtering, and the set of tested transcripts can affect final results. Single cells from one donor should not automatically be treated as independent biological replicates; define the supported design and sampling unit before validation.

Effort is **high**, provisionally. Model fitting is one work package; moderated testing and null calibration are separate research tasks. First specify and fixture one design, audit reusable numerical components, then prototype and review calibration. No calendar estimate is justified until those dependencies are understood.

Upstream declares **Artistic-2.0**. Audit any source translation and the licenses of reused statistical routines independently. Advance only with a domain reviewer, a named maintenance owner, a bounded input contract, and an evidence-backed reason to add this method alongside existing DTU tools.
