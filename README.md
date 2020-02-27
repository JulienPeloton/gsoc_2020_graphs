# GSoC 2020: Evaluation

This repository contains a small evaluation for the GSoC 2020 project, _Manipulation of massive astronomical data using graphs_. We propose a little set of tests related to basic graph problems. We will take into consideration the following points:

- Completion of the exercises
- Code quality (clarity, documentation, comments)
- Suggestion for improvements

We would like also to evaluate your understanding of the Git workflow and code production. You are expected to create a repo on your GitHub account, and push the solutions to exercises to it through a series of Pull Request.

## Before starting

You will need to install (local) the latest versions of [JanusGraph](https://janusgraph.org/), and [Apache HBase](http://hbase.apache.org/) (for the storage backend). 

JanusGraph can be queried from all languages for which a TinkerPop driver exists (using the Gremlin graph query language), and you are free to choose the programming language among Groovy, Python, or Scala.

## Exercise 1: building the graph

The folder `data/` contains a CSV file with graph information. Each row is an entry of the graph, and there are three columns (string type) corresponding to vertices used to build the graph with the following relationships (edges): 

- `column2` -> `is` -> `column1`
- `column3` -> `is` -> `column1`
- `column2` -> `knows` -> `column3`

Exercice: build the graph based on the `data/alerts.csv` data.

## Exercise 2: manipulation of the graph

Query the graph to

- compute the vertex degree (in, out, and overall),
- find the longest chain in the graph,
- count how many vertices are connected to ztf4 (in/out),
- extract the sub-graph containing only vertices pointing to the vertex `unknown`.

## Exercise 3: visualisation of the graph

Display the graph using your favourite tool (you can easily play with [Gephi](https://gephi.org/) if you do not have one), and upload the picture on the repository.