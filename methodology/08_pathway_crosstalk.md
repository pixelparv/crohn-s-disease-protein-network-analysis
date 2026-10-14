# 08. Pathway Crosstalk

## Objective

Visualize relationships among KEGG pathways associated with Crohn’s disease/inflammatory bowel disease (IBD), highlighting shared genes/proteins and hub proteins identified through Cytoscape network analysis.

## Approach

A pathway-crosstalk flowchart was manually assembled in Microsoft PowerPoint using KEGG pathway mappings and hub-protein information selected from the Cytoscape `.tsv` results file.

The flowchart:
- Presents Crohn’s disease/IBD as the biological context for exploring pathway relationships.
- Connects pathways based on shared genes/proteins and selected hub proteins.
- Labels and visually highlights hub proteins to make their involvement across mapped pathways easier to inspect.
- Summarizes pathway overlap and potential connections in one visual representation.

Hub proteins were selected from the Cytoscape results table. Record the exact selection criteria alongside the source table or figure legend if a specific ranking, metric, or threshold was used.

## Interpreting pathway connections

Connections represent relationships inferred from shared gene/protein membership and highlighted hub proteins. Shared membership can indicate overlap between pathway annotations; it does not, by itself, demonstrate direct molecular interaction, directional signalling, or functional crosstalk.

A highlighted hub is a protein ranked as important by the topology measures and network structure used in Cytoscape. Its hub status is specific to the constructed network and does not automatically establish that it is a causal driver of Crohn’s disease or a validated therapeutic target.

The flowchart is therefore a **hypothesis-generating visualization** of pathway relationships in the analysed dataset.

## Figure documentation

The accompanying PowerPoint flowchart was prepared manually. For reproducibility, retain or document:
- The KEGG pathway list and pathway-to-gene/protein mapping table used.
- The Cytoscape `.tsv` file from which hub proteins were selected.
- The hub-selection metric(s) and cutoff or ranking rule, if applicable.
- The rule used to draw each pathway connection (shared gene/protein, shared hub, or both).
- A legend explaining node colours, labels, arrows/lines, and other visual encodings.
- The date of KEGG mapping and the source/version of the Cytoscape results.

## Limitations

- KEGG pathway annotations and pathway membership can change over time.
- Shared genes/proteins may arise from broad or overlapping pathway annotations.
- Hub rankings depend on the input network, filtering thresholds, and topology metric used.
- A manually drawn connection is an analytical representation; it should not be interpreted as a confirmed direct interaction unless supported by independent evidence.
- The diagram does not establish pathway activation or inhibition, nor does it demonstrate causal relationships among pathways.

## Recommended reporting language

Describe the figure as showing **potential pathway crosstalk inferred from shared genes/proteins and Cytoscape-derived hub proteins**. Avoid claims of confirmed pathway activation, causal direction, or clinical significance unless supported by independent evidence.
