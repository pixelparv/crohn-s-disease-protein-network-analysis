# Report

## Overview

This directory contains the PDF report of Reactome pathway over-representation analysis performed as part of the Crohn’s disease in-silico validation project.

The analysis was conducted to identify biological pathways statistically over-represented among the submitted protein and gene identifiers and to provide functional context for the protein interaction network constructed during the validation workflow.

### Analysis Details

- **Organism:** *Homo sapiens*
- **Analysis Date:** 18 June 2026
- **Reactome Version:** 96
- **Submitted Identifiers:** 110 gene names (from the Cytoscape network node table)
- **Mapped Identifiers:** 100/110 (90.9%)
- **Mapped Reactome Entities:** 146
- **Pathways Hit:** 623

## Methodology

The 110 submitted identifiers correspond to the nodes exported from the Cytoscape network.

The submitted identifiers were analysed using the Reactome Pathway Knowledgebase’s over-representation analysis. Identifier mapping associated the submitted identifiers with Reactome entities, and the resulting pathways were ranked using statistical enrichment results.

The report includes pathway-level statistics, including p-values and false discovery rate (FDR)-adjusted values, to assess the over-representation of submitted entities in curated biological pathways.

The enrichment results were examined to characterize biological processes represented in the network, particularly immune regulation, cytokine signalling, interleukin signalling, and interferon responses.

## Key Findings

The most statistically significant pathways included immune-related signalling processes, with prominent examples such as:

- Interleukin-20 family signalling.
- Interleukin-6 signalling.
- Interleukin-12 family signalling.
- Interleukin-4 and interleukin-13 signalling.
- Other cytokine-mediated and immune-regulatory pathways reported in the enrichment results.

These findings provide functional context for interpreting the protein interaction network and identifying biological processes represented among the analysed proteins.

The Reactome analysis complements the network topology analysis performed in Cytoscape and the separate KEGG pathway mapping and pathway-crosstalk visualization documented elsewhere in the repository.

**Interpretation:** Pathway over-representation indicates statistical enrichment, not proof of pathway activation, inhibition, causal relationships, or Crohn’s disease-specific mechanisms. Results depend on identifier mapping, the submitted gene/protein set, the reference database, and the statistical methods used.

## Report Contents

The PDF contains Reactome pathway enrichment results, including pathway names, entity counts, enrichment statistics, p-values, and FDR-adjusted significance values, as provided by the analysis output.

## Reference

Milacic M, et al. (2024). The Reactome Pathway Knowledgebase 2024. Nucleic Acids Research, 52(D1), D672–D678.

**Database:** [Reactome Pathway Knowledgebase](https://reactome.org/)
