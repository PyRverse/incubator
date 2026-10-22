# Validation plan: csaw

Status: **planned**. No csaw reference outputs or timing results have been produced here.

Validate each stage independently before a whole-workflow comparison:

1. **Counting:** generate tiny synthetic alignments with known fragment locations. Exercise chromosome edges, overlapping windows, reverse-strand reads, duplicates, mapping-quality thresholds, and the chosen single/paired-end rules. Require exact coordinates, ordering, integer counts, and filter masks after an explicit coordinate conversion.
2. **Statistics:** export reference count tables, library sizes, normalization factors or offsets, design/contrast matrices, dispersions, coefficients, convergence information, window-level p-values, and missingness. Compare each observable with a justified numerical tolerance.
3. **Regions:** export cluster membership, boundaries, aggregation inputs and region-level results. Require discrete membership agreement for identical windows and deterministic rules; explain any tie handling. Report changes in region calls near the significance threshold.
4. **Scientific behavior:** use simulated null and differential regions to assess region-level FDR and sensitivity under prespecified settings. Numerical agreement does not itself prove the statistical model is appropriate for all experimental designs.

Candidate biological fixtures come from **chipseqDBData** workflows in the [csaw Book](https://bioconductor.org/books/release/csawBook/), including its NF-YA example. Check accession, genome build, preprocessing and redistribution terms before storing a subset. Do not download full BAM collections into routine CI.

Pin R, csaw and statistical/I/O dependencies, retain session information and BLAS/platform metadata, and hash scripts and inputs. Use tiny deterministic fixtures in CI and explicit optional jobs for genome-scale runs. Set tolerance budgets after reference inspection; no universal threshold or performance target is asserted.
