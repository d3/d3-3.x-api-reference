> [Wiki](Home) ▸ [[API Reference]] ▸ **Layouts**

A layout encapsulates a strategy for laying out data elements visually, relative to each other. It could be as simple as stacking bars in a chart (where the base of one bar depends on the height of any below it) or as complex as labeling a map (by shifting labels around until overlap with conflicting map features is minimized). Layouts take a set of input data, apply an algorithm or heuristic, and output the resulting positions/shapes for a cohesive display of the data.

Layouts are not unlike [[d3.svg path generators|SVG-Shapes#path-data-generators]], in that they facilitate the conversion of data to display form. However, layouts typically operate across a collection of data as a whole, rather than individually. Furthermore, the results of a layout could be used anywhere, not just with SVG. Some layouts are even dynamic through time: for example, you `.start()` a `d3.layout.force()` instance and then listen for layout updates on `'tick'` events.

Many layouts are built in to D3 itself:

* [[Bundle|Bundle-Layout]] - apply Holten's *hierarchical bundling algorithm* to edges.
* [[Chord|Chord-Layout]] - produce a chord diagram from a matrix of relationships.
* [[Cluster|Cluster-Layout]] - cluster entities into a dendrogram.
* [[Force|Force-Layout]] - position linked nodes using physical simulation.
* [[Hierarchy|Hierarchy-Layout]] - derive a custom hierarchical layout implementation.
* [[Histogram|Histogram-Layout]] - compute the distribution of data using quantized bins.
* [[Pack|Pack-Layout]] - produce a hierarchical layout using recursive circle-packing.
* [[Partition|Partition-Layout]] - recursively partition a node tree into a sunburst or icicle.
* [[Pie|Pie-Layout]] - compute the start and end angles for arcs in a pie or donut chart.
* [[Stack|Stack-Layout]] - compute the baseline for each series in a stacked bar or area chart.
* [[Tree|Tree-Layout]] - position a tree of nodes tidily.
* [[Treemap|Treemap-Layout]] - use recursive spatial subdivision to display a tree of nodes.

Layouts instances are sometimes functions (though not necessarily) that can be configured and then applied to a set of data. Other times, specific methods or event handlers are used for data input and position output. Please refer to the documentation of each particular layout for usage.