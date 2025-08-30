# The Joy of Computing using Python

# Week 7

# Programming Assignment 1

```bash
def minor_matrix(M, i, j):
  return [
    [M[row][col] for col in range(len(M)) if col != j]
    for row in range(len(M)) if row != i
]
```

# Programming Assignment 2

```bash
import sys

def main():
    teams = ["CSK", "DC", "KKR", "MI", "PK", "RR", "RCB", "SH"]
    wins = {t: 0 for t in teams}
    lines = []
    for _ in range(8):
        line = sys.stdin.readline()
        if not line:
            break
        lines.append(line.rstrip("\n"))
    for idx, raw in enumerate(lines):
        tokens = [t.strip() for t in raw.split(",") if t.strip() != ""]
        if tokens and tokens[0] in wins:
            team = tokens[0]
            defeated = tokens[1:]
        else:
            team = teams[idx] if idx < len(teams) else None
            defeated = tokens
        defeated = [op for op in defeated if op in wins and op != team] 
        wins[team] += len(defeated)
    
    sorted_table = sorted(wins.items(), key=lambda x: (-x[1], x[0]))
    
    for team, w in sorted_table:
        print(f"{team}:{w}")

if __name__ == "__main__":
    main()
```

# Programming Assignment 3

```bash
def pattern(n):
    for i in range(1, 2*n):
        if i <= n:
            left = i
        else:
            left = 2*n - i
        spaces = 2*(n - left)
        print("*"*left + " "*spaces + "*"*left)

if __name__ == "__main__":
    n = int(input().strip())
    pattern(n)
```

### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
