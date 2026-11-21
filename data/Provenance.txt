# Data provenance

Record of primary data sources used in this workflow. STRING-derived outputs are
secondary processed data and are documented in methodology/04_string_network_construction.md.

| Step | Source | Query / access route | Retrieval date | Identifier type | Species | Methodology reference |
|---|---|---|---|---|---|---|
| Literature search | PubMed | "Crohn's Disease", "IBD", "Inflammatory Bowel Disease", "Proteins"; articles 2011–2021 | 13 June 2026 | PMIDs | Homo sapiens | methodology/01_pubmed_literature_review.md |
| Identifier mapping | UniProt | Manual accession lookup per candidate gene symbol | 13 June 2026 | UniProt accessions | Homo sapiens | methodology/02_uniprot_protein_identification.md |
| Interaction retrieval | IntAct | Primary gene names; MI score ≥ 0.65; top five per protein | 14 June 2026 | UniProt accessions | Homo sapiens | methodology/03_intact_interaction_filtering.md |
| Pathway enrichment | Reactome v96 | 110 gene names from Cytoscape network node table | 17 June 2026 | Gene names | Homo sapiens | methodology/06_reactome_enrichment.md |
| Pathway mapping | KEGG Mapper Color | Hub proteins; hsa (Homo sapiens) | 19 June 2026 | Gene symbols | Homo sapiens | methodology/07_kegg_pathway_mapping.md |
