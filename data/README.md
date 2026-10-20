# Data

This directory is intended for input data, identifier mappings, and source-database exports used by the workflow.

## Provenance

Record the following for every data file that is added:

- Source database and exact query or access route.
- Retrieval date.
- File name and format.
- Identifier type and species, where relevant.
- Filters or transformations applied.
- Citation or source URL.

## Handling rules

- Preserve raw exports separately from processed files as primary and secondary, respectively.
- Do not silently overwrite source data.
- Keep gene symbols, UniProt accessions, and protein identifiers clearly distinguished.
- Do not commit private, licensed, or otherwise restricted data without permission.
- The workflow documentation does not imply that source exports are present in this directory.
