# 1. PubMed literature review

## Purpose

Identify candidate genes with reported relevance to Crohn's disease and define a primary gene set for downstream interaction analysis.

## Search approach

PubMed was queried for literature relevant to Crohn's disease genetics, immune pathology, and associated protein functions.

**Search date:** 13 June 2026.
**Search terms:** Combinations of "Crohn's Disease", "IBD", "Inflammatory Bowel Disease" and "Proteins".
**Inclusion criteria:** Articles published between 2011 and 2021 (5–15 years prior to the June 2026 search date). 

## Primary candidate gene set (13 genes)

| # | Gene symbol | UniProt accession | Reported role / rationale | Key reference |
|---|---|---|---|---|
| 1 | NOD2 | Q9HC29 | Bacterial pattern recognition receptor; most replicated CD susceptibility gene | PMID: 11385576 DOI: 10.1038/35079107 |
| 2 | ATG16L1 | Q676U5 | Autophagy scaffold protein; CD risk variant T300A associated with impaired xenophagy | PMID: 17200669 DOI: 10.1038/ng1954 |
| 3 | IRGM | A1A4Y4 | Autophagy regulator; selective mitophagy in innate immunity; CD GWAS locus | PMID: 17554261 PMCID: PMC2628541 DOI: 10.1038/ng2061 |
| 4 | CARD10 | Q9BWT7 | NF-κB signalling adaptor; scaffolding component of the CBM signalosome | PMID: 32238915 PMCID: PMC7331643 DOI: 10.1038/s41423-020-0423-x |
| 5 | SIAE | Q9HAT2 | Sialic acid acetylesterase; reported in IBD susceptibility studies | PMID: 20555325 PMCID: PMC2900412 DOI: 10.1038/nature09115 |
| 6 | IL23R | Q5VWK5 | IL-23 receptor subunit; major CD GWAS risk locus; regulates Th17 differentiation | PMID: 17804789 PMCID: PMC1965486 DOI: 10.1073/pnas.0706645104 |
| 7 | IRF5 | Q13568 | Interferon regulatory factor; innate immune signalling; macrophage polarisation | PMID: 17881657 DOI: 10.1093/hmg/ddm259 |
| 8 | ABCB1 | P08183 | P-glycoprotein; intestinal epithelial barrier integrity and xenobiotic efflux | OMIM: 612244 |
| 9 | CARD8 | Q9Y2G2 | NLRP3 inflammasome regulator; NF-κB signalling adaptor | PMID: 17030188 DOI: 10.1053/j.gastro.2006.08.008 |
| 10 | IL10RB | Q08334 | IL-10 receptor beta subunit; shared receptor chain for IL-10, IL-22, IL-26, and IL-28 family cytokines | PMID: 19890111 PMCID: PMC2787406 DOI: 10.1056/NEJMoa0907206 |
| 11 | IL10RA | Q13651 | IL-10 receptor alpha subunit; IL-10 anti-inflammatory signalling | PMID: 23839161 DOI: 10.1097/MEG.0b013e328361a4f9 |
| 12 | IL37 | Q9NZH6 | Anti-inflammatory cytokine; negative regulator of innate immunity and IL-1 family signalling | PMID: 33674380 PMCID: PMC7958356 DOI: 10.1073/pnas.2009217118 |
| 13 | INAVA | Q3KP66 | Innate immune adaptor; early IBD susceptibility variant; implicated in NF-κB and autophagy crosstalk | PMID: 21983784 PMCID: PMC3378381 DOI: 10.1038/ng.952 |

## Reporting requirements

- Inclusion of a gene reflects literature-reported association with Crohn's disease;
  it does not establish causality, direct pathway membership, or therapeutic relevance.
- Record the PubMed search query, date, and a supporting reference (PMID or DOI)
  for each gene above.
- The complete mapping table (gene symbol → UniProt accession) is stored under `data/`.
- Do not infer missing gene names from this table; the 13 genes listed above constitute
  the complete primary candidate set used in this workflow.
