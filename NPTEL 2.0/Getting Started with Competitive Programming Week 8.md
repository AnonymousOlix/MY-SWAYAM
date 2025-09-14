# Getting Started with Competitive Programming

# Week 8

# Programming Assignment 1

```bash
from collections import deque

def bfs(capacity, adj, parent, source, sink):
    visited = [False] * len(capacity)
    queue = deque([source])
    visited[source] = True

    while queue:
        u = queue.popleft()
        for v in adj[u]:
            if not visited[v] and capacity[u][v] > 0:
                parent[v] = u
                visited[v] = True
                if v == sink:
                    return True
                queue.append(v)
    return False

def max_flow(n_nodes, capacity, adj, source, sink):
    flow = 0
    parent = [-1] * n_nodes

    while bfs(capacity, adj, parent, source, sink):
        path_flow = float('inf')
        s = sink
        while s != source:
            path_flow = min(path_flow, capacity[parent[s]][s])
            s = parent[s]

        v = sink
        while v != source:
            u = parent[v]
            capacity[u][v] -= path_flow
            capacity[v][u] += path_flow
            v = parent[v]

        flow += path_flow
    return flow

def main():
    n, m = map(int, input().split())
    A = list(map(int, input().split()))  # students in courses
    B = list(map(int, input().split()))  # room capacities

    total_nodes = n + m + 2
    source = 0
    sink = total_nodes - 1

    capacity = [[0] * total_nodes for _ in range(total_nodes)]
    adj = [[] for _ in range(total_nodes)]

    # source to courses
    for i in range(n):
        course_node = i + 1
        capacity[source][course_node] = 1
        adj[source].append(course_node)
        adj[course_node].append(source)

    # classrooms to sink
    for j in range(m):
        room_node = n + j + 1
        capacity[room_node][sink] = 1
        adj[room_node].append(sink)
        adj[sink].append(room_node)

    # course to suitable classroom
    for i in range(n):
        for j in range(m):
            if B[j] >= A[i]:
                course_node = i + 1
                room_node = n + j + 1
                capacity[course_node][room_node] = 1
                adj[course_node].append(room_node)
                adj[room_node].append(course_node)

    result = max_flow(total_nodes, capacity, adj, source, sink)
    print(result)

if __name__ == "__main__":
    main()

```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
