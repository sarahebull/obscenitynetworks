# Obscenity Trade Networks (c. 1800–1900)

An interactive network visualization of interpersonal connections among individuals involved in the pornography trade in nineteenth- and early twentieth-century Europe.

## Date Created

2026-02-21

## Author

Sarah Bull

Toronto Metropolitan University

sarah.bull@torontomu.ca

## About the Project

This dataset maps interpersonal connections among individuals involved in the production, distribution, and sale of pornography in nineteenth- and early twentieth-century Europe, or who were defendants in obscenity trials in Britain during that period. It currently documents 273 connections among 195 individuals, drawing on two dataset-creation projects forthcoming or in progress that Bull is leading as well as published research by several other scholars. It is an evolving project and is subject to updates as new information becomes available.

Key clusters in the network include the Dugdale family and their successors; Edward Avery and the Nichols-Smithers "Erotika Biblion Society" circle; the Belgian publisher Auguste Brancart and his Paris agents; and the interconnected continental publishers Aimé Duringe, Jules Eugène Gauché, and Charles Hirsch. The goal is to make visible the social infrastructure of a trade that was often clandestine.

## Files

| File | Description |
|------|-------------|
| `Obscenity_Trade_Networks.html` | Self-contained interactive network visualization (D3.js). |
| `Obscenity_Trade_Networks_All_Connections.csv` | All 273 connections with descriptions and sources. |
| `Obscenity_Trade_Networks_Sources.csv` | Full citations for all sources that inform the connections. |
| `Obscenity_Trade_Networks_Summary.csv` | Aggregate statistics for the network. |
| `README.md` | This file. |

## Data

The dataset is distributed as three CSV files.

**Obscenity_Trade_Networks_All_Connections.csv** contains 273 records with the following variables:

| Variable | Type | Description |
|----------|------|-------------|
| `Person 1` | string | First individual in the connection |
| `Person 2` | string | Second individual in the connection |
| `Relevant Dates` | string/number | Date(s) associated with the connection |
| `Connection Type` | string | Nature of the relationship (e.g., "Business connection," "Husband/wife," "Co-defendants," "Shared address") |
| `Category` | string | One of five groupings: Business (87), Family (78), Shared Address (64), Co-defendants (41), Other (3) |
| `Details` | string | Prose description of the connection with supporting evidence |
| `Source` | string | Dataset or publication from which the connection was drawn |

**Obscenity_Trade_Networks_Sources.csv** lists full citations for all secondary and newspaper sources that inform the connections.

**Obscenity_Trade_Networks_Summary.csv** provides aggregate statistics for the network.

Some connections are marked "Inferred" where they have been deduced from overlapping evidence across sources rather than explicitly documented in any single source. These are typically family connections.

## Interactive Visualization: `Obscenity_Trade_Networks.html`

The visualization is a single self-contained HTML file with all data embedded as JSON. It requires no server — open it locally in a browser or host it as a static file.

Features:

- Force-directed network graph with draggable nodes
- Node sizing by betweenness centrality (Brandes' algorithm), highlighting individuals who bridge different parts of the network
- Searchable dropdown for finding individuals by name
- Category filters (Business, Family, Co-defendants, Shared Address, Other)
- Detail panel displaying all connections for a selected individual, with centrality score
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

Bull, Sarah. 2026. Obscenity Trade Connections Network (c. 1800–1900). https://github.com/sarahebull/obscenity_trade_networks
