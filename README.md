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

-------------

class Graph:
    """
    Implementação de um grafo usando lista de adjacência
    
    Atributos:
        adj_list (dict): Dicionário que armazena os vértices e suas conexões
    """
    
    def __init__(self):
        """Inicializa um grafo vazio"""
        self.adj_list = {}
    
    def print_graph(self):
        """Imprime a estrutura do grafo no formato vértice : [vizinhos]"""
        for vertex in self.adj_list:
            print(f"{vertex} : {self.adj_list[vertex]}")
    
    def add_vertex(self, vertex):
        """
        Adiciona um novo vértice ao grafo
        
        Parâmetros:
            vertex: Vértice a ser adicionado (qualquer tipo hashable)
            
        Retorna:
            bool: True se foi adicionado, False se já existia
        """
        if vertex not in self.adj_list:
            self.adj_list[vertex] = []
            return True
        return False

# Exemplo de uso
if __name__ == "__main__":
    grafo = Graph()
    grafo.add_vertex("A")
    grafo.add_vertex("B")
    grafo.add_vertex("C")
    grafo.print_graph()