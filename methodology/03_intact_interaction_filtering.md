# 3. IntAct interaction filtering

## Purpose

Retrieve curated molecular interaction evidence associated with the primary candidate proteins.

## Selection rule

Interactions were obtained from IntAct, retaining up to the top five interactions per primary gene and applying a minimum MI score of **0.65** on a 0–1 scale.

## Interpretation

The MI score threshold is a selection criterion for this workflow; it should not be described as a universal probability that an interaction is true. Interaction records may reflect different experimental methods and evidence types.

## Quality control

Record the IntAct retrieval date, query, interaction identifiers, participant accessions, detection methods, publication references, and scoring field used. Check duplicate interactions and ensure that the primary-gene-to-interaction selection is applied consistently. Preserve the unfiltered export if available.
