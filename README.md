# Crohn’s Disease Protein Network Analysis

**Author:** Parv Pranjal Saxena  
**Institution:** Dev Bhoomi Uttarakhand University, Dehradun, India  
**Release:** v1.0.0 (2026-10-25)  
**License:** Non-Commercial Use License

## Overview

This repository documents an in-silico workflow for exploring protein association networks and pathway membership associated with Crohn’s disease. It combines literature-supported candidate genes, interaction databases, network analysis, pathway enrichment/mapping, and pathway crosstalk.

This is a computational validation and exploratory analysis. Network associations and pathway enrichment do **not** establish causality, clinical relevance, or a validated disease mechanism.

## Workflow

1. Identify Crohn’s disease-associated candidate genes via a PubMed literature search.
2. Map gene names to UniProt identifiers.
3. Retrieve high-confidence interactions from IntAct, retaining up to five interactions per primary gene at a minimum MI score of 0.65.
4. Expand and filter the network using STRING (confidence score 0.400; 5% FDR setting where applicable).
5. Inspect and analyse the network in Cytoscape, including topology metrics and a yFiles Organic layout.
6. Perform pathway over-representation analysis with Reactome.
7. Map genes to KEGG pathways and examine pathway overlap.
8. Construct a manual flowchart in MS PowerPoint to highlight hub proteins in a pathway-crosstalk.

Detailed methods are in [`methodology/`](methodology/); supporting documentation is in [`docs/`](docs/).

## Repository structure

```text
.
├── data/
├── docs/
├── figures/
├── methodology/
├── report/
├── results/
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── README.md
└── .gitignore
```

## Key interpretation notes

- The initial candidate set contains 13 primary genes.
- The workflow included 77 STRING input identifiers.
- STRING couldn't connect the node SIAE in the extended network. 
- The STRING output was reported as 125 proteins, while the Cytoscape network contained 110 nodes. These are counts from different workflow stages and should not be treated as interchangeable.
- Database contents and enrichment results can change over time. The versions/dates recorded in the methods are historical references from June–July 2026, not a claim that every tool version was independently verified at execution time.
- Results are hypothesis-generating. Evidence quality, identifier mapping, database coverage, selection thresholds, and network construction can influence the findings.

## Reproducibility

This repository documents the analysis choices and expected inputs/outputs. Where source data exports, Cytoscape sessions, or result tables are included, consult the relevant directory README for provenance and limitations. Do not assume a file exists merely because a workflow describes it.

## Contributing

Documentation improvements, corrections, and suggestions are welcome. See [`CONTRIBUTING.md`](CONTRIBUTING.md).

## License

Released under the Non-Commercial Use License. See [`LICENSE`](LICENSE).
