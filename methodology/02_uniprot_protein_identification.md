# 2. UniProt protein identification

## Purpose

Map candidate gene symbols to stable protein identifiers for interaction retrieval.

## Approach

Candidate gene names were mapped to UniProt identifiers. The workflow recorded UniProt IDs for the 13 primary genes and used mapped identifiers in downstream interaction analysis.

## Quality control

- Confirm organism/species for every mapping.
- Check for ambiguous symbols, aliases, one-to-many mappings, and missing identifiers.
- Preserve both the original gene symbol and the mapped accession.
- Record the mapping date and UniProt release/version when available.
- Do not treat gene symbols and protein accessions as interchangeable identifiers.

The exact mapping table should be stored under `data/` or `results/`, with its provenance documented.
