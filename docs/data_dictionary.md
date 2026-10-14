# Data dictionary

Use this guide when naming and documenting columns in project tables. Adapt it to the fields actually present in each export.

| Field | Meaning |
|---|---|
| `gene_symbol` | Gene symbol used in the analysis |
| `uniprot_accession` | UniProt protein accession |
| `protein_id` | Protein identifier from a source database |
| `interactor_a`, `interactor_b` | Identifiers for the two interaction participants |
| `interaction_id` | Source database interaction record identifier |
| `mi_score` | IntAct molecular interaction score, if present |
| `string_score` | STRING association confidence score, if present |
| `node_id` | Node identifier used in the network |
| `degree` | Number of incident edges under the graph definition used |
| `betweenness` | Betweenness centrality value |
| `closeness` | Closeness centrality value |
| `clustering_coefficient` | Local clustering coefficient |
| `pathway_id` | Pathway identifier |
| `pathway_name` | Pathway name |
| `p_value` | Unadjusted enrichment p-value |
| `fdr` | False discovery rate/adjusted value as defined by the source output |
| `found_ratio` | Ratio reported by the pathway-analysis tool; preserve its original definition |

Do not add a column definition unless the underlying file uses that field or its meaning has been confirmed. Preserve source column names in raw exports.
