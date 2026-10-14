## Hub Protein × KEGG Pathway Cross-Reference

### Method

Each hub protein was matched against the eight KEGG pathway maps used in crosstalk analysis. A hub protein was scored as present (✓) in a pathway if it appeared as a highlighted node in the corresponding KEGG Mapper output image.

Pathway abbreviations: IBD = Inflammatory Bowel Disease (hsa05321); JAK-STAT = JAK-STAT Signaling Pathway (hsa04630); TLR = Toll-Like Receptor Signaling
Pathway (hsa04620); NLR = NOD-Like Receptor Signaling Pathway (hsa04621); Th17 = Th17 Cell Differentiation (hsa04659); Th1/Th2 = Th1 and Th2 Cell
Differentiation (hsa04658); Cyt-R = Cytokine-Cytokine Receptor Interaction (hsa04060); Auto = Autophagy – Animal (hsa04140).

Hub proteins are proteins meeting topology ranking criteria (Degree, Betweenness Centrality, Stress Centrality) in Cytoscape network analysis: T1 = triple-metric (all three); T2 = dual-metric (two of three); Anomaly = high degree but unresolved zero-centrality metrics. RELA and IL12B did not meet topology hub criteria and are documented separately under **Pathway-prominent non-hub proteins** below.

---

### Hub × Pathway Presence Matrix

| Hub | Tier | IBD | JAK-STAT | TLR | NLR | Th17 | Th1/Th2 | Cyt-R | Auto | Count |
|---|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **IL6** | T1 | ✓ | ✓ | ✓ | ✓ | ✓ | — | ✓ | — | **6** |
| **STAT1** | T1 | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | **6** |
| **STAT3** | T1 | ✓ | ✓ | — | — | ✓ | — | — | — | **3** |
| **JAK1** | T1 | — | ✓ | ✓ | ✓ | — | ✓ | — | — | **4** |
| **IL4** | T1 | ✓ | — | — | — | ✓ | ✓ | ✓ | — | **4** |
| **IFNG** | T2 | ✓ | ✓ | — | — | ✓ | ✓ | ✓ | — | **5** |
| **IL13** | T2 | ✓ | — | — | — | — | ✓ | ✓ | — | **3** |
| **IL22** | T2 | — | — | — | — | ✓ | — | ✓ | — | **2** |
| **IL10** | T2 | ✓ | ✓ | — | — | — | — | ✓ | — | **3** |
| **IFNB1** | T2 | — | ✓ | ✓ | ✓ | — | — | ✓ | — | **4** |
| **NOD2** | T2 | ✓ | — | — | ✓ | — | — | — | — | **2** |
| **IL18** | T2 | ✓ | — | — | ✓ | — | — | ✓ | — | **3** |
| **IL10RA** | T2 | — | — | — | — | — | — | ✓ | — | **1** |
| **TYK2** | Anomaly | — | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | **5** |

---

### Key Observations

**IL6 and STAT1 — Dual-method, cross-pathway validated hubs (6/8 pathways each)**
Both proteins appear in 6 of 8 KEGG pathways and meet all three topology ranking criteria, providing the strongest cross-method evidence in this analysis. IL6 is present across innate (TLR, NLR), adaptive (Th17, IBD), and cytokine-receptor interaction pathways, consistent with its role as a pleiotropic inflammatory mediator. STAT1 bridges innate IFN signalling (TLR, NLR autocrine loop) with adaptive T cell polarisation (Th17, Th1/Th2, IBD), consistent with its dual role as a JAK-STAT effector and IFN-stimulated gene regulator.

**IFNG — Tier 2 topology, 5/8 pathway coverage**
Despite meeting only two topology ranking criteria, IFNG achieves broader pathway coverage than STAT3 or JAK1, appearing in IBD, JAK-STAT, Th17, Th1/Th2, and Cytokine-Cytokine Receptor interaction. This supports IFNG as a biologically central node whose network influence is distributed across functional modules rather than concentrated in interactome connectivity metrics.

**TYK2 — 5/8 pathway coverage, topology anomaly**
TYK2 appears in 5 of 8 KEGG pathways but carries an unresolved zero-centrality anomaly: betweenness centrality, closeness centrality, average shortest path length, eccentricity, and stress all read as zero in Cytoscape despite a degree of 59. The most likely cause is a directed graph configuration during metric computation. TYK2 is excluded from T1/T2 tier rankings pending verification; its KEGG pathway coverage is reported as independent cross-method evidence of biological relevance, with the topology caveat noted.

**JAK1 and IFNB1 — Innate immunity axis (4/8 pathways each)**
JAK1 and IFNB1 co-occur in TLR and NLR pathways, consistent with their roles in the autocrine/paracrine IFN signalling loop: TLR/NLR activation → IRF3/IRF7 → IFN-β (IFNB1) → IFNαβR → JAK1/TYK2 → STAT1. This mechanistic co-occurrence supports their joint classification as innate signalling hubs.

**NOD2 — Disease-specific bottleneck (2/8 pathways, high betweenness centrality)**
NOD2 appears only in the IBD and NLR pathways but has high betweenness centrality (BC = 0.50), identifying it as a critical connector between the
NOD/NLR innate sensing module and broader inflammatory signalling. Its limited KEGG pathway coverage reflects its specialised role in bacterial pattern recognition rather than broad cytokine biology.

**Autophagy — No hub protein overlap**
None of the 13 topology-classified hub proteins appear in the Autophagy pathway. The autophagy-highlighted nodes (ATG5, ATG12, ATG16L1) are primary CD associated genes present in the network but did not meet topology hub criteria. This confirms autophagy as a mechanistically distinct arm of CD pathology in this network — driven by primary susceptibility genes rather than network hubs.

**IL10RA — Single-pathway (Cytokine-Cytokine Receptor only)**
IL10RA qualifies by dual topology criteria but appears in only one KEGG pathway. Its hub status reflects receptor-level connectivity in the PPI network rather than pathway centrality, and should be reported with that caveat.

---

### Pathway-prominent non-hub proteins

RELA and IL12B did not meet topology ranking criteria for T1 or T2 hub classification and are excluded from the hub matrix above. They are retained in KEGG pathway mapping results and the pathway crosstalk diagram as pathway members, not as network hubs.

| Protein | KEGG pathways | Count | Note |
|---|---|:---:|---|
| RELA | IBD, TLR, NLR, Th17, Th1/Th2 | 5 | NF-κB p65; broad downstream effector role; not topology-supported as hub |
| IL12B | IBD, TLR, Th1/Th2 | 3 | IL-12p40; Th1 polarisation and TLR output; not topology-supported as hub |

These proteins should not be described as network hubs or topology-derived hub candidates in any reporting derived from this analysis.

---

### Pathway Coverage Summary

| Pathway | Hub proteins present | Count |
|---|---|:---:|
| Inflammatory Bowel Disease | IL6, STAT1, STAT3, IL4, IFNG, IL13, IL10, IL18, NOD2 | 9 |
| JAK-STAT Signaling | IL6, STAT1, STAT3, JAK1, IFNG, IL10, IFNB1, TYK2 | 8 |
| Toll-like Receptor | IL6, STAT1, JAK1, IFNB1, TYK2 | 5 |
| NOD-like Receptor | IL6, STAT1, JAK1, IFNB1, NOD2, IL18, TYK2 | 7 |
| Th17 Cell Differentiation | IL6, STAT1, STAT3, IL4, IFNG, IL22, TYK2 | 7 |
| Th1/Th2 Cell Differentiation | STAT1, JAK1, IL4, IFNG, IL13, TYK2 | 6 |
| Cytokine-Cytokine Receptor | IL6, IL4, IL13, IL10, IL10RA, IL22, IFNG, IFNB1, IL18 | 9 |
| Autophagy – Animal | *(none)* | 0 |

*RELA (5 pathways) and IL12B (3 pathways) are present in KEGG pathway maps as non-hub members; their pathway membership is documented in the section above.*

---

### Discussion

Cross-referencing the 13 topology-classified hub proteins against eight KEGG pathway maps confirmed differential pathway coverage consistent with their centrality profiles. IL6 and STAT1, both Tier 1 triple-metric hubs, each appeared in 6 of 8 pathways — the broadest coverage of any hub — providing cross method validation of their central role in the Crohn's disease-associated network. IFNG, despite meeting only dual topology criteria, showed the second widest coverage at 5 pathways, spanning innate IFN signalling, T helper cell differentiation, and cytokine-receptor interaction, suggesting that its network influence is distributed across functional modules rather than reflected in raw connectivity. JAK1 and IFNB1 co-occurred specifically within the TLR and NLR innate signalling arms, consistent with their role in the autocrine IFN-β/JAK1/STAT1 amplification loop downstream of pattern recognition receptor activation. TYK2 also appeared in 5 pathways but carries an unresolved centrality anomaly in Cytoscape; its topology tier remains uncertain pending verification, and its pathway coverage is reported as independent cross-method evidence of biological relevance. NOD2, a primary Crohn's disease susceptibility gene, appeared in only the IBD and NLR pathways but exhibited high betweenness centrality, consistent with its role as a connector between the innate sensing module and downstream inflammatory signalling. Notably, no hub protein was present in the Autophagy pathway; autophagy-associated nodes (ATG5, ATG12, ATG16L1) are primary CD-associated genes in the network but did not meet topology hub criteria, indicating that the autophagy arm of Crohn's disease pathology operates through a mechanistically distinct module within this interactome.
