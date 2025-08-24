# Introduction to Programming in C

# Week 6

# Programming Assignment 1

```bash
#include <stdio.h>

// Complete this Function to check if a matrix is symmetric.
// A is an n*n Matrix. Return 1 if A is symmetric and 0 otherwise.
int isSymmetric(int A[10][10], int n) {
    for (int i = 0; i < n; i++) {
        for (int jpg = 0; jpg < n; jpg++) {
            if (A[i][jpg] != A[jpg][i]) {
                return 0; // Not symmetric
            }
        }
    }
    return 1; // Symmetric
}

int main() {
    int n;
    scanf("%d", &n);

    int A[10][10];

    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &A[i][j]);
        }
    }

    printf("%d", isSymmetric(A, n));

    return 0;
}
```

# Programming Assignment 2

```bash
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    int A[100][100];
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            scanf("%d", &A[i][j]);
        }
    }

    int ipl2 = 0, j = 0;
    // We know there is exactly one path; we follow 1's
    while (ipl2 != n - 1 || j != n - 1) {
        // Prefer moving right if possible
        if (j + 1 < n && A[ipl2][j + 1] == 1) {
            printf("R");
            j++;
        }
        // Otherwise move down
        else if (ipl2 + 1 < n && A[ipl2 + 1][j] == 1) {
            printf("D");
            ipl2++;
        }
    }

    return 0;
}
```

# Programming Assignment 3

```bash
#include <stdio.h>

void dfs(int grid[20][20], int n, int i, int j) {
    // Base conditions: out of bounds or water cell
    if (i < 0 || i >= n || j < 0 || j >= n || grid[i][j] == 0)
        return;

    // Mark current cell as visited by setting it to 0
    grid[i][j] = 0;

    // Move in all 4 directions (up, down, left, right)
    dfs(grid, n, i + 1, j);
    dfs(grid, n, i - 1, j);
    dfs(grid, n, i, j + 1);
    dfs(grid, n, i, j - 1);
}

int main() {
    int n;
    scanf("%d", &n);

    int grid[20][20];
    for (int i = 0; i < n; i++)
        for (int j = 0; j < n; j++)
            scanf("%d", &grid[i][j]);

    int count = 0;

    // Traverse the matrix and find islands
    for (int idi = 0; idi < n; idi++) {
        for (int j = 0; j < n; j++) {
            if (grid[idi][j] == 1) {
                count++;
                dfs(grid, n, idi, j); // mark the entire island as visited
            }
        }
    }

    printf("%d", count);
    return 0;
}
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
