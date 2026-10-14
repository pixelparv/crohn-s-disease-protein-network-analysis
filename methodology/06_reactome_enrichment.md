# 6. Reactome pathway enrichment

## Purpose

Identify pathways statistically over-represented among the submitted network proteins and provide functional context for the interaction network.

## Analysis parameters

| Parameter | Value |
|---|---|
| Organism | *Homo sapiens* |
| Analysis date | 17 June 2026 |
| Reactome version | 96 |
| Submitted identifiers | 110 (UniProt and Ensembl accessions corresponding to the Cytoscape network nodes) |
| Mapped identifiers | 100 / 110 (90.9%) |
| Mapped Reactome entities | 146 |
| Pathways hit | 623 |
| Analysis type | Over-representation analysis (ORA) |
| Background / universe | Reactome default (*Homo sapiens* proteome) |
| Multiple testing correction | Benjamini–Hochberg; FDR: 9.44e-15 to 7.39e-08, p-value: 1.11e-16 to 2.74e-09 |
| "Include Interactors" option | Not used (redundant with prior IntAct and STRING steps) |

## Approach

The 110 node identifiers exported from Cytoscape were submitted to the Reactome Pathway Knowledgebase over-representation analysis. Reactome mapped the submitted identifiers to internal entities and ranked enriched pathways by p-value and FDR-adjusted significance. The analysis summary examined the 25 most significantly enriched pathways.

## Key enriched pathways (top results)

The most statistically significant pathways from the Reactome report included immune-related signaling processes:

- Interleukin-20 family signaling
- Interleukin-6 signaling
- Interleukin-12 family signaling
- Interleukin-4 and Interleukin-13 signaling
- Interleukin-6 family signaling

These results provide functional context for interpreting the protein interaction network, particularly its immune regulation, cytokine signaling, and interferon response components.

## Output

The Reactome analysis produced a PDF report containing pathway names, entity counts, enrichment statistics, p-values, and FDR-adjusted values. This report is stored at `4_report/reactome_enrichment_report.pdf`. Do not reconstruct p-values or FDR values from visual inspection of the report; use the original export file.

## Interpretation

Pathway over-representation indicates that a pathway contains more submitted entities than expected by chance under the chosen background and statistical model. It does not prove that a pathway is activated, inhibited, or causally involved in Crohn's disease. Results depend on identifier mapping coverage, the submitted gene/protein set, the Reactome database version, and the correction method applied.

## Reference

Milacic M, et al. (2024). The Reactome Pathway Knowledgebase 2024. *Nucleic Acids Research*, 52(D1), D672–D678. https://doi.org/10.1093/nar/gkad1025
