# TiGraph: Build a Graph Database on TiKV

## What is Graph Database?

Hundreds of years ago, the city of Königsberg in Prussia devided into four parts by the Pregel River and connected with
seven bridges made Euler thinking about the Seven Bridges of Königsberg problem. After that, people started to concern
about the connection between *things*, and finally established Graph Theory.

There is always a connection, or relationship, to be common, between two arbitrary things in the world. We can use graph
 theory to analyze the relationships and learn from them, a good example is the Six Degrees of Seperation.

Graph Database is the tool for us to analyze relationships with computer.

With a Graph Database, we can store our data modeled in graph, and perform graph query on it.

## Graph Model

As we know, a graph is a set of nodes and relationships between nodes. Naturally, we represent data entity with node,
and represent connection between entities with relationship.

For example, let's say we have a data set of movies as follow:
- Wolf Warriors, directed by Jing Wu
- Wolf Warriors II, directed by Jing Wu
- The Wandering Earth, directed by Fan Guo

We can easily build a *Movie Grapg* graph with the principle we mentioned above.

> TODO: Image

This graph can represent the *direct* relationship between director and movies. However, we can notice that *Jing Wu* is
 not only director of *Wolf Warriors* and *Wolf Warriors II*, but also actor of both three movies.

To represent these relationships in *Movie Graph*, we introduce a concept of *Relationship Type*, or *Labeled Relationship*.

We can combine every relationship in the graph with a *Label*, to indicate which kind the relationship belongs to.

Take the actor relationship as example, we can add two kinds of labels: *Direct* and *Act*. And the graph will look like:

> TODO: Image

Now we have a graph with labeled relationships, this model is called *Edge-labeled Graph*.

We see that *Edge-labeled Graph* makes relationships more semantic, thus more information can be stored.

*Edge-labeled Graph* is the basis of semantic network, it provides a way to modeling connective data.

In real world, data 