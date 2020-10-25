# Octetful Notes - Graphs - Apache Tinkerpop

This section covers the Apache Tinkerpop framework.

- [Getting Started Guide](https://tinkerpop.apache.org/docs/current/tutorials/getting-started/)
- [Recipes](https://tinkerpop.apache.org/docs/current/recipes/)
- [Reference](https://tinkerpop.apache.org/docs/current/reference/)
- [Javadoc (full)](https://tinkerpop.apache.org/javadocs/3.4.8/full/)

## Tinkerpop Tools
- [Gremlify](https://gremlify.com/) - An online gremlin console that **"mostly"** works. Doesn't support many common operations like subgraphs, or even proper `addE()` operations.
- [Kryo](https://github.com/EsotericSoftware/kryo) - a fast and efficient binary object graph serialization framework for Java.
- [Graphexp](https://github.com/bricaud/graphexp) - Graphexp is a lightweight web interface to explore and display a graph stored in a Gremlin graph database, via the Gremlin server (version 3.2.x, 3.3.x or 3.4.x).
- [Dockerized Gremlin Console](https://hub.docker.com/r/tinkerpop/gremlin-console) - A docker container image for gremlin console. See notes below for more information on usage.
- [Dockerized Gremlin Server](https://hub.docker.com/r/tinkerpop/gremlin-server) - A docker container image for gremlin server.


---
** Starting Containerized Gremlin Console **

To start a containerized gremlin console use the following commands:
```bash
docker pull tinkerpop/gremlin-console
docker run -it tinkerpop/gremlin-console
```

---
