# Octetful Notes - Graphs - Visualisation

This section contains details on different visualisation tools and techniques used for graphs.

## Graphviz

[Graphviz](https://graphviz.gitlab.io/) is open source graph visualization software. Graph visualization is a way of representing structural information as diagrams of abstract graphs and networks.

### The DOT Language
> DOT is a graph description language. DOT graphs are typically files with the filename extension gv or dot. The extension gv is preferred, to avoid confusion with the extension dot used by versions of Microsoft Word before 2007.
> Various programs can process DOT files. Some, such as dot, neato, twopi, circo, fdp, and sfdp, can read a DOT file and render it in graphical form. Others, such as gvpr, gc, acyclic, ccomps, sccmap, and tred, read DOT files and perform calculations on the represented graph. Finally, others, such as lefty, dotty, and grappa, provide an interactive interface. The GVedit tool combines a text editor with noninteractive image viewer. Most programs are part of the Graphviz package or use it internally.
>           -- [Wikipedia](https://en.wikipedia.org/wiki/DOT_(graph_description_language))

You can find the the abstract grammar defining the graph language [**here**](https://graphviz.org/doc/info/lang.html).

There is also an active **Reddit** thread of discussions for [more graph visualisation libraries](https://www.reddit.com/r/java/comments/6ogiwx/library_for_graph_visualization/).

### GraphViz React
[**`graphviz-react`**](https://www.npmjs.com/package/graphviz-react) provides a simple to use component for rendering Graphviz objects in React.

You can find the source code for `graphviz-react` on [**Github**](https://github.com/DomParfitt/graphviz-react).

### IntelliJ IDEA Plugin
There is a plugin that can provide basic editing support for dot language files (`*.dot` and `*.gv`) in IntelliJ IDEA called the [**dotPlugin**](https://plugins.jetbrains.com/plugin/10312-dotplugin).



## Visualising Tinkerpop/Gremlin Graphs
There are potentially multiple visualisation options for Tinkerpop or Gremlin graphs, some of which we tried as noted below:

### [Using Neo4J embedded mode browser](https://graphaware.com/neo4j/2014/11/21/neo4j-browser-with-embedded.html)
This is also linked under Neo4J notes section, and is deprecated and only applicable when using Neo4J embedded provider in Tinkerpop. Still untested, but the UI for neo4j works like a charm.

### [Using graphexp](https://github.com/bricaud/graphexp)
This method would require a Tinkerpop server to connect to. You would need to change the configurations in the `scripts/graphConf.js` file.

### Using a custom visualization component
You could for example write a translator to translate a Gremlin Graph to Graphviz dot file usign the [Graphviz Java library](https://github.com/nidi3/graphviz-java).


