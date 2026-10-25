# 3. IntAct Interaction Filtering

# Retrieval date: 14 June 2026
# Query terms: Primary gene names

## Purpose

Retrieve and filter curated binary molecular interaction evidence for the 13 primary candidate proteins using IntAct, selecting high-confidence interacting partners based on MI score.

## Selection rule

Each of the 13 primary proteins was queried individually in IntAct. A query returned multiple protein entries and a minimum MI score of **≥ 0.65** (0–1 scale) was applied to filter out the interactions. The **top five interacting proteins by MI score** were then retained per primary protein.

## Detection methods observed

1. Anti-tag co-immunoprecipitation
2. Tag co-immunoprecipitation
3. Co-immunoprecipitation
4. Cross-linking study
5. Pull down (affinity purification)
6. Validated two-hybrid
7. Two-hybrid array
8. Two-hybrid fragment pooling approach
9. Two-hybrid prey pooling approach
10. Two-hybrid pooling approach
11. Two-hybrid
12. Enzyme-linked immunosorbent assay
13. Isothermal titration calorimetry
14. Molecular sieving (size exclusion chromatography)
15. Co-sedimentation / analytical ultracentrifugation
16. Proximity-dependent biotin identification
17. Surface plasmon resonance
18. X-ray crystallography
19. Confocal microscopy
20. Ion exchange chromatography

## Interpretation

The MI score threshold is a workflow-specific selection criterion, not a universal probability of interaction validity. Scores reflect the cumulative weight and diversity of experimental evidence aggregated by IntAct and should be interpreted alongside the detection methods and publication records of each entry. Interaction records may reflect different evidence types and experimental contexts 

## Quality control

- Record the IntAct retrieval date, query term, interaction identifiers, detection methods, and the scoring field used.
- Confirm that the ≥ 0.65 MI score filter was applied *before* selection of the top five interacting proteins per primary     protein.
- Check for and resolve duplicate interaction records.
