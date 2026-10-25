# Results

Output artefacts from the Crohn's disease protein-protein interaction network analysis pipeline.

---

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

### `reactome_pathway_enrichment/`

| File | Description |
|------|-------------|
| `reactome_pathway_enrichment.csv` | Over-representation analysis results from Reactome. Columns: `Pathway ID`, `Pathway Name`, `Entities Found`, `Entities Total`, `p-value`, `FDR`, `Hit Genes`. Filtered at FDR < 0.05. |

### Root-level files

| File | Description |
|------|-------------|
| `hub_kegg_crossref.tsv` | Cross-reference table mapping Cytoscape hub proteins and KEGG pathway memberships. Enables combination of Cytoscape topological analysis results with KEGG annotations to identify the hub set. |

---

## Reproduction Notes

- Network topology scores were computed in Cytoscape using the **NetworkAnalyzer** plugin.  
- Hub proteins were defined by degree and betweenness centrality thresholds (see `methods/` for exact cut-offs).  
- Reactome ORA was run via the Reactome Analysis Service (https://reactome.org/analyse) against the *Homo sapiens* reference proteome.  
- KEGG cross-referencing was performed using the KEGG Color, towards "hsa"; pathway assignments reflect the database state at the time of analysis.
