# NeuraFutures Viz

NeuraFutures Viz is a visualization tool allows users to explore connections betewen pieces of BCI-Fi media. The tool casts the rich statical and semantic data collected in the Neurafutures database into an embedding space and allows users to explore dimensions along which they want to visualize connections.

### Embedding Space Dimensions

* Semantics
* Form factor
* Medium
* BCI-Fi category
* Date
* Utopia / Dystopia
* Invasiveness
* Metrics
  * Neurafictionality
  * Reality factor
  * Neuroptimism
  * BCI forecast

### Data Processing

The NeuraFutures database contains 438 works and their associated data. NeuraFutures Viz queries from the Notion database and processes the data to a consistent schema for visualization.

### Software Architecture

NeuraFutures Viz was built with NetworkX, Dash, and Plotly. 