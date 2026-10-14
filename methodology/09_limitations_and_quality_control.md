# 9. Limitations and quality control

## Main limitations

- **Literature selection bias:** candidate genes depend on search terms, publication coverage, and inclusion decisions.
- **Identifier ambiguity:** aliases and one-to-many mappings can alter network membership.
- **Database coverage:** interaction and pathway databases are incomplete and updated over time.
- **Mixed evidence:** STRING associations do not all represent direct physical interactions.
- **Threshold dependence:** IntAct and STRING thresholds affect which edges and nodes are retained.
- **Network dependence:** hub and centrality rankings depend on the constructed graph.
- **Enrichment interpretation:** statistical over-representation is not proof of activation, inhibition, causality, or clinical relevance.
- **Stage-specific counts:** 125 STRING proteins and 110 Cytoscape nodes must be documented separately; the discrepancy should not be silently resolved without checking the actual files and filters.
- **No experimental validation implied:** computational findings require independent evidence before biological or clinical claims can be made.

## Quality-control checklist

- Verify species and identifier mappings.
- Keep raw exports and processed tables separate.
- Record dates, database releases, parameters, and software versions.
- Track all filtering and duplicate-removal steps.
- Reconcile counts at each workflow stage from source files.
- Use cautious language for hubs, enriched pathways, and inferred crosstalk.
