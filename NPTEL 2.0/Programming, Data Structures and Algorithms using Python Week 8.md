# Programming, Data Structures and Algorithms using Python

# Week 8

# Programming Assignment 1

```bash
n = int(input())
LGG = list()
bestvals =list()
best_stored = list()
for x in range(n):
  LGG.append(int(input()))
  best_stored.append(0)

best_stored[0] = 1

for i in range(n):
  maxval = 1
  for j in range(i):
    if LGG[i] % LGG[j] == 0:
      maxval = max(maxval,(best_stored[j])+1)
  best_stored[i] = maxval

print(max(best_stored),end="")
```



### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
