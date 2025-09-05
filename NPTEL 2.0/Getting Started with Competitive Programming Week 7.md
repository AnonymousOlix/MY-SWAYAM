# Getting Started with Competitive Programming

# Week 7

# Programming Assignment 1

```bash
class UnionFind:
    def __init__(self, n):
        self.parent = list(range(n))
        self.rank = [0] * n

    def find(self, x):
        if self.parent[x] != x:
            self.parent[x] = self.find(self.parent[x])  # Path compression
        return self.parent[x]

    def union(self, x, y):
        rootX = self.find(x)
        rootY = self.find(y)
        if rootX != rootY:
            # Union by rank
            if self.rank[rootX] > self.rank[rootY]:
                self.parent[rootY] = rootX
            elif self.rank[rootX] < self.rank[rootY]:
                self.parent[rootX] = rootY
            else:
                self.parent[rootY] = rootX
                self.rank[rootX] += 1
            return True
        return False

def kruskal(n, edges):
    uf = UnionFind(n)
    mst_weight = 0
    mst_edges = []
    
    # Sort edges by their weight
    edges.sort(key=lambda x: x[2])
    
    for u, v, weight in edges:
        if uf.union(u, v):
            mst_weight += weight
            mst_edges.append((u, v, weight))
    
    return mst_weight, mst_edges

def maximum_road_length_to_break(n, m, roads):
    total_weight = sum(c for a, b, c in roads)
    
    # Adjust roads to be 0-indexed for Union-Find
    roads = [(a-1, b-1, c) for a, b, c in roads]
    
    # Calculate the MST weight
    mst_weight, _ = kruskal(n, roads)
    
    # The answer is the total weight of roads minus the MST weight
    return total_weight - mst_weight

# Read input
n, m = map(int, input().split())
roads = [tuple(map(int, input().split())) for _ in range(m)]

# Output the result
print(maximum_road_length_to_break(n, m, roads))
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
