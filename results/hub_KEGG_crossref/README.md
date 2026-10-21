## Hub Protein × KEGG Pathway Cross-Reference

### Method

Each protein was cross-referenced against the eight KEGG pathway maps used in the crosstalk analysis. Presence (`✓`) indicates that the protein appeared as a highlighted node in the corresponding KEGG Mapper output.

Pathway abbreviations: IBD = Inflammatory Bowel Disease (hsa05321); JAK-STAT = JAK-STAT Signaling Pathway (hsa04630); TLR = Toll-like Receptor Signaling Pathway (hsa04620); NLR = NOD-like Receptor Signaling Pathway (hsa04621); Th17 = Th17 Cell Differentiation (hsa04659); Th1/Th2 = Th1 and Th2 Cell Differentiation (hsa04658); Cyt-R = Cytokine-Cytokine Receptor Interaction (hsa04060); Auto = Autophagy – Animal (hsa04140).

Tier labels follow the TSV: **Tier 1** = triple-metric topology candidates; **Tier 2** = dual-metric topology candidates; **Tier 3 – KEGG only** = pathway-mapped proteins not supported as topology-prominent hubs; **Anomaly – verify** = TYK2, whose high degree is accompanied by unresolved zero centrality metrics.

---

### Protein × Pathway Presence Matrix

| Protein | Tier | IBD | JAK-STAT | TLR | NLR | Th17 | Th1/Th2 | Cyt-R | Auto | Count |
|---|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **IL6** | Tier 1 – Triple metric | ✓ | ✓ | ✓ | ✓ | ✓ | — | ✓ | — | **6** |
| **STAT1** | Tier 1 – Triple metric | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | **6** |
| **STAT3** | Tier 1 – Triple metric | ✓ | ✓ | — | — | ✓ | — | — | — | **3** |
| **JAK1** | Tier 1 – Triple metric | — | ✓ | ✓ | ✓ | — | ✓ | — | — | **4** |
| **IL4** | Tier 1 – Triple metric | ✓ | — | — | — | ✓ | ✓ | ✓ | — | **4** |
| **IFNG** | Tier 2 – Dual metric | ✓ | ✓ | — | — | ✓ | ✓ | ✓ | — | **5** |
| **IL13** | Tier 2 – Dual metric | ✓ | — | — | — | — | ✓ | ✓ | — | **3** |
| **IL22** | Tier 2 – Dual metric | — | — | — | — | ✓ | — | ✓ | — | **2** |
| **IL10** | Tier 2 – Dual metric | ✓ | ✓ | — | — | — | — | ✓ | — | **3** |
| **IFNB1** | Tier 2 – Dual metric | — | ✓ | ✓ | ✓ | — | — | ✓ | — | **4** |
| **NOD2** | Tier 2 – Dual metric | ✓ | — | — | ✓ | — | — | — | — | **2** |
| **IL18** | Tier 2 – Dual metric | ✓ | — | — | ✓ | — | — | ✓ | — | **3** |
| **IL10RA** | Tier 2 – Dual metric | — | — | — | — | — | — | ✓ | — | **1** |
| **RELA** | Tier 3 – KEGG only | ✓ | — | ✓ | ✓ | ✓ | ✓ | — | — | **5** |
| **IL12B** | Tier 3 – KEGG only | ✓ | — | ✓ | — | — | ✓ | — | — | **3** |
| **TYK2** | Anomaly – verify | — | ✓ | ✓ | ✓ | ✓ | ✓ | — | — | **5** |

---

### Key Observations

**IL6 and STAT1 — Broadest coverage among topology-supported candidates (6/8 pathways each)**  
Both are Tier 1 triple-metric candidates and appear in six pathways. IL6 spans IBD, JAK-STAT, TLR, NLR, Th17, and cytokine-receptor interaction; STAT1 spans IBD, JAK-STAT, TLR, NLR, Th17, and Th1/Th2. Their pathway coverage provides cross-method support for their prominence in this network.

**IFNG — Tier 2 candidate with broad pathway coverage (5/8)**  
IFNG appears in IBD, JAK-STAT, Th17, Th1/Th2, and cytokine-receptor interaction, connecting several inflammatory and T-cell-related pathway maps.

**TYK2 — Pathway coverage with unresolved topology anomaly (5/8)**  
TYK2 appears in JAK-STAT, TLR, NLR, Th17, and Th1/Th2. The TSV records degree 59 with zero centrality metrics and flags it for verification in Cytoscape. Its pathway coverage should be treated as separate evidence from the unresolved topology result; do not assign it a confirmed Tier 1 or Tier 2 status until the metrics are checked.

**JAK1 and IFNB1 — Shared innate-signalling pathway membership**  
JAK1 and IFNB1 both appear in the TLR and NLR maps. This overlap is consistent with their involvement in interferon-associated signalling, although pathway co-occurrence alone does not establish a causal sequence.

**NOD2 — IBD/NLR-associated candidate (2/8)**  
NOD2 appears in the IBD and NLR maps. The TSV describes it as a primary Crohn’s disease-associated gene involved in NLR pattern recognition.

**IL10RA — Restricted pathway coverage (1/8)**  
IL10RA appears only in Cytokine-Cytokine Receptor Interaction. Its Tier 2 label reflects the supplied topology classification, not broad KEGG pathway coverage.

**Autophagy — No listed protein overlap**  
None of the proteins in the TSV are marked present in the Autophagy – Animal map. This describes the cross-reference results only; it does not establish that autophagy is absent from Crohn’s disease biology or from the wider network.

---

### Pathway Coverage Summary

The counts below include all proteins listed in the TSV, including RELA and IL12B (Tier 3 – KEGG only) and TYK2 (Anomaly – verify).

| Pathway | Proteins marked present | Count |
|---|---|:---:|
| Inflammatory Bowel Disease | IL6, STAT1, STAT3, IL4, IFNG, IL13, IL10, NOD2, IL18, RELA, IL12B | 11 |
| JAK-STAT Signaling | IL6, STAT1, STAT3, JAK1, IFNG, IL10, IFNB1, TYK2 | 8 |
| Toll-like Receptor | IL6, STAT1, JAK1, IFNB1, RELA, IL12B, TYK2 | 7 |
| NOD-like Receptor | IL6, STAT1, JAK1, IFNB1, NOD2, IL18, RELA, TYK2 | 8 |
| Th17 Cell Differentiation | IL6, STAT1, STAT3, IL4, IFNG, IL22, RELA, TYK2 | 8 |
| Th1/Th2 Cell Differentiation | STAT1, JAK1, IL4, IFNG, IL13, RELA, IL12B, TYK2 | 8 |
| Cytokine-Cytokine Receptor | IL6, IL4, IFNG, IL13, IL22, IL10, IFNB1, IL18, IL10RA | 9 |
| Autophagy – Animal | *(none)* | 0 |

---

### Discussion

The TSV cross-reference shows differential pathway coverage across the topology-classified proteins. IL6 and STAT1 have the highest coverage among the Tier 1/Tier 2 topology candidates, appearing in six of eight maps each. IFNG and TYK2 each appear in five maps, but their interpretation differs: IFNG is Tier 2, whereas TYK2 remains an unresolved topology anomaly because its degree is 59 while its centrality metrics are reported as zero. JAK1 and IFNB1 share TLR and NLR pathway membership. NOD2 appears in IBD and NLR maps, while IL10RA appears only in the cytokine-receptor interaction map. RELA and IL12B are included in the TSV as Tier 3 – KEGG only, with five and three pathway matches respectively; they should not be represented as topology-supported hubs. No listed protein is marked present in the autophagy map. These observations describe the supplied cross-reference and should not be interpreted as independent experimental validation or proof of pathway causality.
