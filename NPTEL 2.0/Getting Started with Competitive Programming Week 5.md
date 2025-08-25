# Getting Started with Competitive Programming

# Week 5

# Programming Assignment 1

```bash
def min_groups(n, parents):
    from collections import defaultdict, deque

    # Build adjacency list
    children = defaultdict(list)
    roots = []

    for i in range(n):
        p = parents[i]
        if p == -1:
            roots.append(i)
        else:
            children[p-1].append(i)  # zero-based indexing

    max_depth = 0

    # BFS from each root to find max depth
    for root in roots:
        queue = deque()
        queue.append((root, 1))  # (node, depth)
        while queue:
            node, depth = queue.popleft()
            max_depth = max(max_depth, depth)
            for child in children[node]:
                queue.append((child, depth + 1))

    return max_depth

if __name__ == "__main__":
    n = int(input())
    parents = [int(input()) for _ in range(n)]
    print(min_groups(n, parents))
```

# Programming Assignment 2

```bash
import sys
sys.setrecursionlimit(10**7)
input = sys.stdin.readline

def dfs(node, parent, depth, flip_even, flip_odd):
    global flips, v, d, graph

    # Calculate current effective value of this node
    if depth % 2 == 0:
        current = v[node] ^ flip_even
    else:
        current = v[node] ^ flip_odd

    # If current value != desired value, flip this node
    if current != d[node]:
        flips += 1
        # Update flip flags for children
        if depth % 2 == 0:
            flip_even ^= 1
        else:
            flip_odd ^= 1

    # Visit children
    for child in graph[node]:
        if child != parent:
            dfs(child, node, depth + 1, flip_even, flip_odd)

if __name__ == "__main__":
    n = int(input())
    graph = [[] for _ in range(n)]

    for _ in range(n - 1):
        a, b = map(int, input().split())
        a -= 1
        b -= 1
        graph[a].append(b)
        graph[b].append(a)

    v = list(map(int, input().split()))
    d = list(map(int, input().split()))

    flips = 0
    dfs(0, -1, 0, 0, 0)
    print(flips)
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
