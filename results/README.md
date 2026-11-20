# Results

Output artefacts from the Crohn's disease protein-protein interaction network analysis pipeline.

---

<<<<<<< Updated upstream
## File Descriptions

### `cytoscape_network_analysis/`

| File | Description |
|------|-------------|
| `cytoscape_hub_proteins_table.tsv` | Tabular export of hub proteins identified by topological filtering. Columns include gene symbol and the centrality metrics used for hub classification. |
| `cytoscape_session.cys` | Native Cytoscape session file. Open in Cytoscape ≥ 3.9 to restore the full network with visual styles, edge weights, and node groupings intact. |
| `cytoscape_topology_scores.csv` | Network topology scores for all nodes: degree, betweenness centrality, closeness centrality, and clustering coefficient. Used as the basis for hub protein selection. |

### `potential_pathway_crosstalk/`

| File | Description |
|------|-------------|
| `potential_pathway_crosstalk.pptx` | Microsoft PowerPoint Presentation illustrating functional overlap and cross-talk among the top enriched pathways, annotated with shared hub proteins at pathway intersections. |

=======
## Directory Structure

results/
├── cytoscape_network_analysis/
│ ├── cytoscape_hub_proteins_table.tsv # Hub protein list with network centrality attributes
│ ├── cytoscape_session.cys # Cytoscape session (network layout, styles, node annotations)
│ └── cytoscape_topology_scores.csv # Per-node topology metrics (degree, betweenness, closeness, etc.)
├── potential_pathway_crosstalk/
│ └── potential_pathway_crosstalk.pptx # Curated figure summarising cross-talk between enriched pathways
├── reactome_pathway_enrichment/
│ └── reactome_pathway_enrichment.csv # Reactome ORA results (pathway ID, name, p-value, FDR, hit genes)
├── hub_kegg_crossref.tsv # Hub proteins cross-referenced against KEGG pathway annotations
└── README.md

---

## File Descriptions

### `cytoscape_network_analysis/`

| File | Description |
|------|-------------|
| `cytoscape_hub_proteins_table.tsv` | Tabular export of hub proteins identified by topological filtering. Columns include gene symbol, UniProt ID, and the centrality metrics used for hub classification. |
| `cytoscape_session.cys` | Native Cytoscape session file. Open in Cytoscape ≥ 3.9 to restore the full network with visual styles, edge weights, and node groupings intact. |
| `cytoscape_topology_scores.csv` | Network topology scores for all nodes: degree, betweenness centrality, closeness centrality, and clustering coefficient. Used as the basis for hub protein selection. |

### `potential_pathway_crosstalk/`

| File | Description |
|------|-------------|
| `potential_pathway_crosstalk.pptx` | Presentation-ready figure illustrating functional overlap and cross-talk among the top enriched pathways, annotated with shared hub proteins at pathway intersections. |

>>>>>>> Stashed changes
### `reactome_pathway_enrichment/`

| File | Description |
|------|-------------|
| `reactome_pathway_enrichment.csv` | Over-representation analysis results from Reactome. Columns: `Pathway ID`, `Pathway Name`, `Entities Found`, `Entities Total`, `p-value`, `FDR`, `Hit Genes`. Filtered at FDR < 0.05. |

### Root-level files

| File | Description |
|------|-------------|
<<<<<<< Updated upstream
| `hub_kegg_crossref.tsv` | Cross-reference table mapping Cytoscape hub proteins and KEGG pathway memberships. Enables combination of Cytoscape topological analysis results with KEGG annotations to identify the hub set. |
=======
| `hub_kegg_crossref.tsv` | Cross-reference table mapping hub proteins to their KEGG pathway memberships. Enables comparison of Reactome ORA results against KEGG annotations for the same hub set. |
>>>>>>> Stashed changes

---

## Reproduction Notes

- Network topology scores were computed in Cytoscape using the **NetworkAnalyzer** plugin.  
<<<<<<< Updated upstream
- Hub proteins were defined by degree and betweenness centrality thresholds (see `methods/` for exact cut-offs).  
- Reactome ORA was run via the Reactome Analysis Service (https://reactome.org/analyse) against the *Homo sapiens* reference proteome.  
- KEGG cross-referencing was performed using the KEGG Color, towards "hsa"; pathway assignments reflect the database state at the time of analysis.
=======
- Hub proteins were defined by degree and betweenness centrality thresholds (see `methods/` or dissertation text for exact cut-offs).  
- Reactome ORA was run via the Reactome Analysis Service (https://reactome.org/analyse) against the *Homo sapiens* reference proteome.  
- KEGG cross-referencing was performed using the KEGG REST API; pathway assignments reflect the database state at the time of analysis (see `logs/` for date stamps if available).
>>>>>>> Stashed changes
