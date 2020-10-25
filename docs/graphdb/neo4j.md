# Octetful Notes - Graphs - Neo4J

This section covers details on the neo4j graph database.

* [Neo4j cypher manual v4.1](https://neo4j.com/docs/cypher-manual/current/) authored by the Neo4j team.
* [Using Neo4j Browser with Embedded Neo4j](https://graphaware.com/neo4j/2014/11/21/neo4j-browser-with-embedded.html)

## Subgraphs
- [Expand to subgraph procedure](https://neo4j.com/labs/apoc/4.1/graph-querying/expand-subgraph/)
- [Analytical Subgraph Overlays in Neo4j](https://neo4j.com/blog/analytical-subgraph-overlays-in-neo4j/)
- [The `with` clause](https://neo4j.com/docs/cypher-manual/current/clauses/with/)

## Data Import Guides
- [Importing CSV Data into Neo4j](https://neo4j.com/developer/guide-import-csv/)

---
** Dynamic Relationship Loading **

To create [dynamic relationship](https://community.neo4j.com/t/how-to-create-dynamic-relations-from-csv-with-apoc/4081) labels in Neo4j, you could call a stored proc as follows:
```sql
LOAD CSV WITH HEADERS FROM "file:///relations.csv" AS row
MATCH (f:Node), (s:Node)
WHERE f.Name = row.FromNode
AND s.Name = row.ToNode
CALL apoc.create.relationship(f, row.RelationType,{}, s) YIELD rel
REMOVE rel.noOp
```

---