# CHANGELOG.md

## [1.0.0] — 2026-10-25

### Initial public release

- Documented full in-silico workflow: PubMed literature search → UniProt mapping →
  IntAct interaction filtering → STRING network construction → Cytoscape network
  analysis → Reactome pathway enrichment → KEGG pathway mapping → PowerPoint
  pathway-crosstalk visualization.
- Primary candidate set: 13 genes; 77 unique identifiers submitted to STRING.
- STRING v12.0 output: 125 proteins, 1,621 edges; SIAE failed to connect.
- Cytoscape v3.9.0 working network: 110 nodes; topology analysed with NetworkAnalyzer.
- Hub classification: 5 Tier-1 (triple-metric), 8 Tier-2 (dual-metric), 1 unresolved
  anomaly (TYK2 — degree 59, centrality metrics zero).
- Reactome v96 ORA: 100/110 identifiers mapped; 623 pathways hit (top results:
  IL-20 family, IL-6, IL-6 family, IL-12 family, IL-4/IL-13 signalling).
- KEGG Mapper Color cross-reference across 8 pathway maps (hsa).
- Added methodology notes, interpretation limits, reproducibility checklist, and
  contribution guidance.
