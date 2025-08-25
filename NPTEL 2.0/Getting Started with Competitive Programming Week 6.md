# Getting Started with Competitive Programming

# Week 6

# Programming Assignment 1

```bash
import sys
input = sys.stdin.read

def min_empty_distance(matrix, n, m):
    empty_seats = []

    # Collect all empty seat positions
    for i in range(n):
        for j in range(m):
            if matrix[i][j] == 0:
                empty_seats.append((i, j))

    # If fewer than 2 empty seats, not possible
    if len(empty_seats) < 2:
        return -1

    min_dist = float('inf')

    # Compare all pairs of empty seats
    for i in range(len(empty_seats)):
        for j in range(i + 1, len(empty_seats)):
            x1, y1 = empty_seats[i]
            x2, y2 = empty_seats[j]
            dist = abs(x1 - x2) + abs(y1 - y2)
            if dist < min_dist:
                min_dist = dist
                if min_dist == 1:
                    return 1  # Can't get better than 1

    return min_dist

def main():
    data = input().split()
    idx = 0
    T = int(data[idx])
    idx += 1

    results = []

    for _ in range(T):
        n = int(data[idx])
        m = int(data[idx + 1])
        idx += 2

        matrix = []
        for _ in range(n):
            row = list(map(int, data[idx:idx + m]))
            idx += m
            matrix.append(row)

        res = min_empty_distance(matrix, n, m)
        results.append(str(res))

    print("\n".join(results))

if __name__ == "__main__":
    main()
```

# Programming Assignment 2

```bash
import sys
import heapq

def dijkstra(n, graph, s):
    dist = [float('inf')] * n
    dist[s] = 0
    pq = [(0, s)]
    parent = [-1] * n

    while pq:
        d, u = heapq.heappop(pq)
        if d > dist[u]:
            continue
        for v, w, idx in graph[u]:
            nd = d + w
            if nd < dist[v]:
                dist[v] = nd
                parent[v] = u
                heapq.heappush(pq, (nd, v))
    return dist, parent

def solve():
    input = sys.stdin.readline
    n, m, L, s, t = map(int, input().split())

    edges = []
    graph = [[] for _ in range(n)]
    zero_edges = set()

    for i in range(m):
        u, v, w = map(int, input().split())
        edges.append([u, v, w])
        graph[u].append([v, w, i])
        graph[v].append([u, w, i])
        if w == 0:
            zero_edges.add(i)

    # Replace all zero weights with 1 for initial run
    for i in zero_edges:
        u, v, w = edges[i]
        edges[i][2] = 1

    # Rebuild graph with updated edges
    graph = [[] for _ in range(n)]
    for i, (u, v, w) in enumerate(edges):
        graph[u].append([v, w, i])
        graph[v].append([u, w, i])

    dist, parent = dijkstra(n, graph, s)
    if dist[t] > L:
        print("NO")
        return
    if dist[t] == L:
        print("YES")
        # Print edges as requested by problem statement or just "YES"
        # Problem doesn't require printing weights
        return

    # dist[t] < L => try to increase zero edge weights on shortest path from s to t
    # Trace back shortest path edges
    path = []
    cur = t
    while parent[cur] != -1:
        u = parent[cur]
        # find edge between u and cur
        for v, w, idx in graph[u]:
            if v == cur:
                path.append(idx)
                break
        cur = u
    path = path[::-1]

    # Check zero edges on path
    zero_in_path = [idx for idx in path if idx in zero_edges]

    if not zero_in_path:
        # No zero edges on shortest path, can't increase distance
        print("NO")
        return

    # Increase weights on zero edges on path to get distance exactly L
    diff = L - dist[t]
    # Increase first zero edge weight by diff
    idx = zero_in_path[0]
    edges[idx][2] += diff

    # Rebuild graph and verify if shortest path distance == L
    graph = [[] for _ in range(n)]
    for i, (u, v, w) in enumerate(edges):
        graph[u].append([v, w, i])
        graph[v].append([u, w, i])

    dist2, _ = dijkstra(n, graph, s)
    if dist2[t] == L:
        print("YES")
    else:
        print("NO")

if __name__ == "__main__":
    solve()
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
