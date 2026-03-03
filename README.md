# Obscenity Trade Networks (c. 1800–1900)

An interactive network visualization of interpersonal connections among individuals involved in the pornography trade in nineteenth- and early twentieth-century Europe.

## Date Created

2026-02-21

## Author

Sarah Bull

Toronto Metropolitan University

sarah.bull@torontomu.ca

## About the Project

This dataset maps interpersonal connections among individuals involved in the production, distribution, and sale of pornography in nineteenth- and early twentieth-century Europe, or who were defendants in obscenity trials in Britain during that period. It currently documents 306 connections among 205 individuals, drawing on two dataset-creation projects forthcoming or in progress that Bull is leading as well as published research by several other scholars. It is an evolving project and is subject to updates as new information becomes available.

Key clusters in the network include the Dugdale family and their successors; Edward Avery and the Nichols-Smithers "Erotika Biblion Society" circle; the Belgian publisher Auguste Brancart and his Paris agents; and the interconnected continental publishers Aimé Duringe, Jules Eugène Gauché, and Charles Hirsch. The aim of this project is to make visible the social infrastructure of a trade that was often clandestine.

## Files

| File | Description |
|------|-------------|
| `Obscenity_Trade_Networks.html` | Self-contained interactive network visualization (D3.js). |
| `Obscenity_Trade_Networks_All_Connections.csv` | All 306 connections with descriptions and sources. |
| `Obscenity_Trade_Networks_Sources.csv` | Full citations for all sources that inform the connections. |
| `Obscenity_Trade_Networks_Summary.csv` | Aggregate statistics for the network, including Louvain community breakdown. |
| `README.md` | This file. |

## Data

The dataset is distributed as three CSV files.

**Obscenity_Trade_Networks_All_Connections.csv** contains 306 records with the following variables:

| Variable | Type | Description |
|----------|------|-------------|
| `Person 1` | string | First individual in the connection |
| `Person 2` | string | Second individual in the connection |
| `Relevant Dates` | string/number | Date(s) associated with the connection |
| `Connection Type` | string | Nature of the relationship (e.g., "Business connection," "Husband/wife," "Co-defendants," "Shared address") |
| `Category` | string | One of five groupings: Shared Address (90), Business (88), Family (83), Co-defendants (42), Other (3) |
| `Details` | string | Prose description of the connection with supporting evidence |
| `Source` | string | Dataset or publication from which the connection was drawn |

**Obscenity_Trade_Networks_Sources.csv** lists full citations for all secondary and newspaper sources that inform the connections.

**Obscenity_Trade_Networks_Summary.csv** provides aggregate statistics for the network, including a breakdown of communities detected by the Louvain algorithm with the hub (most connected individual) in each community.

Some connections are marked "Inferred" where they have been deduced from overlapping evidence across sources rather than explicitly documented in any single source. These are typically family connections.

## Interactive Visualization: `Obscenity_Trade_Networks.html`

The visualization is a single self-contained HTML file with all data embedded as JSON. It requires no server — open it locally in a browser or host it as a static file.

Features:

- Force-directed network graph with draggable nodes
- Node sizing by betweenness centrality (Brandes' algorithm), highlighting individuals who bridge different parts of the network
- Community detection (Louvain modularity clustering) with toggle to recolour nodes by detected community and display convex hull outlines around clusters
- Searchable dropdown for finding individuals by name
- Category filters (Business, Family, Co-defendants, Shared Address, Other)
- Dual-handle timeline slider for filtering connections by date range (1800–1910)
- Detail panel displaying all connections for a selected individual, with centrality score and community membership
- Live network statistics (visible nodes, edges)
- Zoom and pan controls

### Dependencies (loaded from CDN)

- [D3.js](https://d3js.org/) 7.8.5
- [Google Fonts](https://fonts.google.com/): Jost

## Sources

See Obscenity_Trade_Networks_Sources.csv

## Licence

CC-BY 4.0

## Citation

Bull, Sarah. 2026. Obscenity Trade Networks (c. 1800–1900). https://github.com/sarahebull/obscenity_trade_networks
