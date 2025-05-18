# Graph Class Implementation

class Graph:
    """
    A graph implementation using adjacency list representation.
    
    Attributes:
        adj_list (dict): Stores the adjacency list where keys are vertices 
                         and values are lists of adjacent vertices.
    """
    
    def __init__(self):
        """Initialize an empty adjacency list dictionary."""
        self.adj_list = {}
    
    def print_graph(self):
        """Print the graph structure showing each vertex and its neighbors."""
        for vertex in self.adj_list:
            print(vertex, ':', self.adj_list[vertex])
    
    def add_vertex(self, vertex):
        """
        Add a vertex to the graph if it doesn't exist.
        
        Args:
            vertex: The vertex to be added to the graph
            
        Returns:
            bool: True if vertex was added, False if it already exists
        """
        if vertex not in self.adj_list:
            self.adj_list[vertex] = []
            return True
        return False


# Usage Example
if __name__ == "__main__":
    # Create a new graph
    graph = Graph()

    # Add vertices
    graph.add_vertex("A")
    graph.add_vertex("B")
    graph.add_vertex("C")

    # Print the graph
    print("Graph Structure:")
    graph.print_graph()

"""
README:
This Graph class implements a basic adjacency list representation of a graph.
Current functionality includes:
- Adding vertices
- Printing the graph structure

The adjacency list is stored as a dictionary where:
- Keys are vertices
- Values are lists of adjacent vertices

Example Output:
A : []
B : []
C : []

Note: This is a basic implementation that currently only handles vertices.
Edge functionality can be added to connect vertices.
"""