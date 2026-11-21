# README.md

# Crohn's Disease Protein Network Analysis

**Author:** Parv Pranjal Saxena  
**Institution:** Dev Bhoomi Uttarakhand University, Dehradun, India  
**Release:** v1.0.0 — 2026-11-22  
**License:** Non-Commercial Use License

---

## Overview

An in-silico workflow exploring protein association networks and pathway membership associated with Crohn's disease. The analysis integrates literature derived candidate genes, molecular interaction databases, network topology, pathway enrichment, and pathway crosstalk visualisation.

**This is a hypothesis-generating computational analysis.** Network associations and pathway enrichment do not establish causality, clinical relevance, or a validated disease mechanism.

---

## Repository structure

```text
.
├── data/
│   ├── primary/          # Raw inputs: gene lists, UniProt IDs, IntAct interactions
│   └── secondary/        # Processed: STRING TSV exports, 110-node gene list
├── docs/                 # Interpretation, data dictionary, reproducibility checklist
├── figures/              # Publication/portfolio figures
├── methodology/          # Step-by-step method files (01–09)
├── report/               # Reactome ORA PDF report
├── results/
│   ├── cytoscape_network_analysis/
│   ├── hub_KEGG_crossref/
│   ├── potential_pathway_crosstalk/
│   └── reactome_pathway_enrichment/
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

---

## Workflow

| Step | Tool / Resource | Key parameters |
|------|----------------|---------------|
| 1. Candidate gene selection | PubMed | Search date: 13 Jun 2026; articles 2011–2021; 13 primary genes |
| 2. Identifier mapping | UniProt | 13 accessions; mapping date: 13 Jun 2026 |
| 3. Interaction retrieval | IntAct | MI score ≥ 0.65; top 5 partners per gene; retrieval date: 14 Jun 2026 |
| 4. Network expansion | STRING v12.0 | 77 input identifiers; confidence ≥ 0.400; iterative expansion to 125 proteins; retrieval date: 16 Jun 2026 |
| 5. Network analysis | Cytoscape v3.9.0 | 110-node network; yFiles Organic layout; NetworkAnalyzer topology metrics |
| 6. Pathway enrichment | Reactome v96 | 110 identifiers submitted; 100 mapped (90.9%); 623 pathways hit; date: 17 Jun 2026 |
| 7. Pathway mapping | KEGG Mapper Color | Organism: *Homo sapiens* (hsa); 8 pathway maps; date: 19 Jun 2026 |
| 8. Pathway crosstalk | Microsoft PowerPoint | Manual flowchart; hub proteins from Cytoscape TSV |

Detailed methods are in [`methodology/`](methodology/); supporting documentation is in
[`docs/`](docs/).

---

## Key results

**Network**
- 13 primary genes → 77 unique STRING inputs (primary genes + unique IntAct partners)
- STRING output: 125 proteins, 1,621 edges; 12/13 primary genes connected (SIAE absent)
- Cytoscape working network: 110 nodes (15-node reduction from STRING export; cause
  unconfirmed — reconcile before final submission)

**Hub classification (Cytoscape NetworkAnalyzer — directed network)**

| Tier | Proteins |
|------|----------|
| T1 — Triple-metric (Degree, Betweenness, Stress) | IL6, STAT1, STAT3, JAK1, IL4 |
| T2 — Dual-metric | IFNG, NOD2, IL13, IL22, IL10, IFNB1, IL18, IL10RA |
| T3 — KEGG pathway only (not topology hubs) | RELA, IL12B |
| Anomaly — verify | TYK2 (degree 59; betweenness, closeness, stress all zero) |

**Reactome enrichment (top pathways)**  
Interleukin-20 family signalling · IL-6 signalling · IL-6 family signalling ·
IL-12 family signalling · IL-4 and IL-13 signalling

**KEGG cross-reference**  
IL6 and STAT1 appear in 6/8 maps each (broadest coverage among topology-supported
hubs). Autophagy map: no hub-protein overlap detected.

---

## Interpretation notes

- Results are hypothesis-generating; they do not establish causation or clinical validity.
- STRING edges represent heterogeneous association evidence, not exclusively direct
  physical interactions.
- Hub and centrality rankings are network- and parameter-specific.
- The TYK2 centrality anomaly must be resolved before reporting topology-based
  conclusions for that protein.
- Database contents and enrichment results change over time; dates recorded in the
  methods are historical references, not verification timestamps.

---

## Reproducibility

Source data exports, Cytoscape sessions, and result tables are included where available;
consult the relevant directory README for provenance and known limitations. Do not assume
a file exists solely because the workflow describes it. See
[`docs/reproducibility.md`](docs/reproducibility.md) for the full checklist.

---

## Contributing

Documentation corrections and methodological suggestions are welcome.
See [`CONTRIBUTING.md`](CONTRIBUTING.md).

---

## License

Released under the Non-Commercial Use License. See [`LICENSE`](LICENSE).
