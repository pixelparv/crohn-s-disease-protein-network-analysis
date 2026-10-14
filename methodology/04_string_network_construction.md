# 4. STRING network construction

## Purpose

Expand the candidate interaction network using STRING association evidence.

## Input identifier derivation

The 77 identifiers submitted to STRING comprised the 13 primary candidate proteins together with their unique interaction partners retrieved from IntAct (up to five interactions per primary gene at MI score ≥ 0.65). Duplicate identifiers shared across primary genes were removed before submission, yielding 77 unique input identifiers including the primary proteins themselves.

## Parameters

| Parameter | Value |
|---|---|
| Organism | *Homo sapiens* |
| STRING version | v12.0 |
| Input identifiers | 77 |
| Minimum interaction confidence | 0.400 |
| Network type | Full STRING network (physical and functional associations) |
| Network expansion | None beyond submitted identifiers (Option 1 selected) |
| FDR setting | 5% (see note below) |
| Export format | Two `.tsv` files — node table and edge table |
| Retrieval date | 16 June 2026 |

**Evidence channels active:** experimentally determined, curated databases, co-expression, text-mining, gene-neighbourhood, gene fusion, gene co-occurrence and protein homology

**Note on FDR setting:** The 5% FDR figure applies to the PPI network retrieval itself.

## Output

| Metric | Value |
|---|---|
| Reported STRING output | 125 proteins |
| Edges | 1,621 |
| Connected primary genes | 12 of 13 |

The gene SIAE was absent from the connected output in the initial network.

## Note on output count versus Cytoscape node count

The STRING export reported 125 proteins. The Cytoscape network subsequently contained 110 nodes. These counts belong to different workflow stages and must not be treated as equivalent. The 15-node reduction likely reflects the removal of disconnected or low-confidence nodes during STRING export filtering or Cytoscape import, but the exact cause has not been confirmed from source files.
See `results/README.md` for reconciliation requirements.

## Interpretation

STRING edges represent protein associations that may combine evidence from co-expression, experimental data, curated databases, and text-mining sources; they do not uniformly represent direct physical interactions. The 5% FDR setting applies to a specific STRING function and should be confirmed before being reported as a network-level filter.

## Reproducibility checklist

- [ ] Record the 77 exact query identifiers and confirm their derivation
      (13 primary genes + unique IntAct partners).
- [ ] Record retrieval date and STRING version (v12.0).
- [ ] Document all active evidence channels.
- [ ] Confirm what the 5% FDR setting was applied to.
- [ ] Preserve the two `.tsv` exports under `data/raw/`.
- [ ] Identify which primary gene was absent from the connected output.
- [ ] Document the cause of the 125 → 110 node reduction.
