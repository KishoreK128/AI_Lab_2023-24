# Ex.No: 2  Implementation of Depth First Search
### DATE: 26/08/2025                                                                           
### REGISTER NUMBER : 212223060128
### AIM: 
To write a python program to implement Depth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.
### Program:

```
from collections import deque

def bfs(graph, start):
    visited = set()
    queue = deque([start])

    while queue:
        vertex = queue.popleft()
        if vertex not in visited:
            print(vertex, end=" ")
            visited.add(vertex)

            
            for neighbor in graph[vertex]:
                if neighbor not in visited:
                    queue.append(neighbor)

graph = {
    'A': ['B', 'C'],
    'B': ['A', 'D', 'E'],
    'C': ['A', 'F'],
    'D': ['B'],
    'E': ['B', 'F'],
    'F': ['C', 'E']
}

print("Breadth-First Search starting from node A:")
bfs(graph, 'A')
```








### Output:

<img width="441" height="134" alt="Screenshot 2025-08-26 095145" src="https://github.com/user-attachments/assets/62321c8a-9b23-4e8b-bbe6-edfa89c726a3" />


### Result:
Thus the depth first search order was found sucessfully.
