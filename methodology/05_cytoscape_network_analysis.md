# 5. Cytoscape network analysis

## Purpose

Visualize the protein association network, calculate topology measures, and classify hub proteins by centrality profile.

## Software

**Cytoscape version:** 3.9.0

## Network import and node count

The STRING `.tsv` exports (node table and edge table) were imported into Cytoscape. The working network contained **110 nodes**. The difference between the STRING-reported 125 proteins and the 110 Cytoscape nodes likely reflects the removal of disconnected nodes or low-confidence entries during STRING export filtering or Cytoscape import. The exact cause has not been confirmed from source files and should be reconciled before final submission.

## Layout

**yFiles Organic** layout was applied for visualization. Layout is a visual arrangement only; it does not alter the underlying edge table or biological evidence. Proximity in the layout does not imply stronger interaction or greater biological significance.

## Topology metrics computed

The following metrics were calculated using Cytoscape's built-in Network Analyzer:

| Metric | Definition |
|---|---|
| Average Shortest Path Length | Mean shortest path length across all node pairs |
| Betweenness Centrality | Fraction of all pairwise shortest paths passing through a node; marks bottlenecks | 
| Closeness Centrality | Reciprocal of mean shortest path distance to all other nodes; higher = more central | 
| Clustering Coefficient | Proportion of a node's neighbours that are mutually connected; measures local density | 
| Degree | Total edges incident to a node (indegree + outdegree in directed networks) | 
| Eccentricity | Maximum shortest path length from a node to any other node | 
| Edge Count | Total edges at a node (local) or in the network (global) | 
| Indegree | Number of edges directed *into* a node | 
| Neighbourhood Connectivity | Mean degree of a node's immediate neighbours | 
| Number of Undirected Edges | Count of unique node pairs connected by an edge, ignoring direction | 
| Outdegree | Number of edges directed *out of* a node | 
| Radiality | Normalised measure of how easily a node reaches all others relative to network diameter; higher = more globally accessible | 
| Topological Coefficient | Extent to which a node shares neighbours with its neighbours; higher = embedded in overlapping modules | 

The network was treated as **directed** for topology calculations. 

## Hub protein classification

Proteins were classified as hubs using a two-method approach: Cytoscape topology ranking and KEGG pathway coverage. Topology was the primary classification criterion; KEGG pathway coverage provided cross-method validation.

### Topology ranking approach

Three centrality metrics were used to assess hub status: **Degree**, **Betweenness Centrality**, and **Stress Centrality**, as computed by Cytoscape's NetworkAnalyzer. Hub classification was based on relative ranking within the 110-node network: proteins ranking prominently in the upper distribution of the network for a given metric were considered to meet that metric's criterion. No fixed absolute threshold was applied; classification reflects the observed centrality distribution of this specific network.

- A protein meeting all three ranking criteria was classified as **Tier 1 (T1 — Triple-metric)**.
- A protein meeting two criteria was classified as **Tier 2 (T2 — Dual-metric)**.
- Proteins not meeting topology ranking criteria are not classified as topology hubs, regardless of KEGG pathway coverage.

### Hub tier classification

| Tier | Definition | Proteins |
|---|---|---|
| T1 — Triple-metric | Ranked prominently across Degree, Betweenness Centrality, and Stress Centrality | IL6, STAT1, STAT3, JAK1, IL4 |
| T2 — Dual-metric | Ranked prominently across two of the three metrics | IFNG, NOD2, IL13, IL22, IL10, IFNB1, IL18, IL10RA |
| Anomaly | High degree but multiple reachability-based metrics read as zero; topology tier unresolved | TYK2 |

### TYK2 anomaly

**TYK2 anomaly:** TYK2 showed zero values for betweenness centrality, closeness centrality, average shortest path length, eccentricity, and stress despite having a degree of 59. The anomaly was not resolved in Cytoscape and remains flagged for verification. Since the network was analyzed as directed, edge orientation may have affected reachability-dependent metrics; however, this has not been confirmed as the cause. TYK2's topology tier cannot be reliably assigned from these values and is excluded from T1/T2 groupings pending verification. Its presence in 5 of 8 KEGG pathways provides additional evidence of pathway representation, but does not independently establish its topological importance.

### Pathway-prominent proteins (not classified as topology hubs)

RELA (NF-κB p65) and IL12B did not meet the topology ranking criteria for hub classification under any tier. They are retained in KEGG pathway mapping results and appear in the pathway crosstalk analysis, but are not reported as network hubs.

- **RELA:** present in 5/8 KEGG pathways (IBD, TLR, NLR, Th17, Th1/Th2). Pathway coverage reflects the broad role of NF-κB as a downstream effector across innate and adaptive immune pathways, but this was not supported by network topology in this analysis.
- **IL12B:** present in 3/8 KEGG pathways (IBD, TLR, Th1/Th2). Its pathway membership reflects IL-12p40's role in Th1 polarisation and TLR output, but topology analysis did not identify it as a network hub.

Both proteins should be described as pathway members in the KEGG results, not as network hubs or topology-derived hub candidates.

## Interpretation cautions

- Hub status is specific to this network under these parameters; it does not generalize to other networks, datasets, or biological contexts.
- A high-degree or high-centrality node in this network is not automatically a disease driver or validated therapeutic target.
- Centrality values depend on network composition, edge definitions, and directionality settings.
- Layout (yFiles Organic) has no effect on computed metric values.

## Reproducibility checklist

- [ ] Record Cytoscape version (3.9.0) and NetworkAnalyzer settings.
- [ ] Document what caused the node reduction, if any (125 → 110 in this case).
- [ ] Confirm whether the network was treated as directed or undirected for all metric calculations.
- [ ] Preserve the Cytoscape session file (`.cys`), topology scores (`.csv`), and exported node/edge tables (`.tsv`).
- [ ] Resolve and document any anomaly before final submission (the TYK2 centrality in this case).
- [ ] Record the centrality distributions used as the basis for T1/T2 ranking criteria (e.g., export the full node table showing all metric values).
