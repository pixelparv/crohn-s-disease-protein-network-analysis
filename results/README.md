# Results

Store tabular outputs and exported analysis results here, with a clear distinction between raw tool output and processed summaries.

## Recommended organization

- `raw/`: unmodified exports from databases and analysis tools.
- `processed/`: filtered, mapped, or reformatted tables.
- `summary/`: tables used in the report or figures.

Create these subdirectories only when needed.

## Required metadata

Each result should identify its source step, retrieval or analysis date, software/database version where known, parameters, and any filtering or conversion applied.

## Count interpretation

The workflow reports 125 proteins in the STRING output and 110 nodes in the Cytoscape network. Document the exact filtering, identifier handling, and export stage behind each count before attempting to reconcile them. Do not assume that they represent the same set.
