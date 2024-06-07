# Bellman-Ford Algorithm 

## Overview

The Bellman-Ford Algorithm is used to find the shortest paths from a single source vertex to all other vertices in a weighted graph. It can handle graphs with negative weight edges and is capable of detecting negative weight cycles.

## Problem Definition

Given:

- A weighted graph represented by vertices \( V \) and edges \( E \), where each edge \( (u, v) \) has a weight \( w \).
- A source vertex \( s \) from which to calculate the shortest paths.

Objective:

- Compute the shortest path from the source vertex \( s \) to all other vertices in the graph.
- Detect if there are any negative weight cycles in the graph.


## Implementation

The implementation involves the following steps:

1. **Initialization**: Set initial distances from the source to all vertices as infinite, except for the source vertex which is set to zero.
2. **Relaxation**: Update the distance for each vertex by considering all edges, repeating this for \( |V| - 1 \) times.
3. **Cycle Detection**: Check for negative weight cycles by verifying if any distance can still be reduced.

## Input Format

The input consists of a list of edges, where each edge has three attributes: source vertex, destination vertex, and weight. These can be provided as follows:

- **Edge Class**: Each edge is represented as an instance of the Edge class.
- **List of Edges**: A list of Edge objects.
- **Source Vertex**: The vertex from which to start the shortest path calculation.

## Output Format

The output will consist of:

- **Distances**: A list of shortest distances from the source vertex to each vertex.
- **Cycle Detection**: A message indicating whether a negative weight cycle exists.
