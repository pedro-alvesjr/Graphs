# Graph Class Implementation

## Overview
This Python implementation provides a basic Graph data structure using an adjacency list representation. The current version supports vertex addition and graph visualization.

## Features
- **Adjacency List Storage**: Uses a dictionary to store vertices and their connections
- **Vertex Management**: Add new vertices to the graph
- **Graph Visualization**: Print the current graph structure

## Class Methods

### `__init__(self)`
- Initializes an empty adjacency list dictionary

### `print_graph(self)`
- Prints the graph structure in the format:  
  `vertex : [adjacent_vertex1, adjacent_vertex2, ...]`

### `add_vertex(self, vertex)`
- Adds a new vertex to the graph
- Parameters:
  - `vertex`: The vertex to add (any hashable type)
- Returns:
  - `True` if vertex was added
  - `False` if vertex already exists

## Example Usage
```python
graph = Graph()
graph.add_vertex("A")
graph.add_vertex("B")
graph.add_vertex("C")
graph.print_graph()