# Ex.No: 1  Implementation of Breadth First Search 
### DATE:  07/3/2025                                                                          
### REGISTER NUMBER : 212222220044
### AIM: 
To write a python program to implement Breadth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function bfs and take the set “visited” is empty and “queue” is empty
4. Search start with initial node and add the node to visited and queue.
5. For each neighbor node, check node is not in visited then add node to visited and queue list.
6.  Creating loop to print the visited node.
7.   Call the bfs function by passing arguments visited, graph and starting node.
8.   Stop the program.
### Program:
```
# Python program to implement Breadth-First Search

def bfs(graph, start_node):
    visited = set()  # Set to keep track of visited nodes
    queue = []  # Queue to maintain nodes to visit
    
    visited.add(start_node)
    queue.append(start_node)
    
    while queue:
        node = queue.pop(0)  # Dequeue a node
        print(node, end=" ")  # Process the node
        
        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)

# Example graph represented as an adjacency list
graph = {
    'A': ['B', 'C'],
    'B': ['A', 'D', 'E'],
    'C': ['A', 'F', 'G'],
    'D': ['B'],
    'E': ['B', 'H'],
    'F': ['C'],
    'G': ['C'],
    'H': ['E']
}

# Call BFS function
print("Breadth-First Search starting from node A:")
bfs(graph, 'A')
```
### Output:
![ai exp1](https://github.com/user-attachments/assets/2639d9bc-1277-4b2d-88e4-81514167e103)


### Result:
Thus the breadth first search order was found sucessfully.
