# The Joy of Computing using Python

# Week 5 

# Programming Assignment 1

```bash
L = input().split(' ')
L = [int(num) for num in L]
x = int(input())
 
first_pos = 0
last_pos = len(L)-1
flag=0
count = 0
while(first_pos<=last_pos and flag==0):
  count+=1
  mid = (first_pos+last_pos)//2
  if (x==L[mid]):
    flag = 1
    print(mid,end ='')
    break
  else:
    if (x < L[mid]):
      last_pos = mid-1
    else:
      first_pos = mid+1
else:
  print('-1',end ='')
```

# Programming Assignment 2

```bash
L1 = input().split(' ')
L1 = [int(num) for num in L1]
L2 = input().split(' ')
L2 = [int(num) for num in L2]
L = []
c1,c2 = 0,0
while(1):
  if c1 < len(L1) and L1[c1] <= L2[c2]:
    L += [L1[c1]]
    c1+=1
    if c1 == len(L1):
      L += L2[c2:]
      break
  elif c2 < len(L2) and L2[c2] <= L1[c1]:
    L += [L2[c2]]
    c2+=1
    if c2 == len(L2):
      L += L1[c1:]
      break
print(' '.join(map(str,L)), end='')
```

# Programming Assignment 3

```bash
L = input().split(' ')
L = [int(num) for num in L]
k = int(input())
L.sort()
if L[k-1] == L[-k]:
  if k == len(L)//2+1:
    print('1',end = '')
  else:
    print('-1',end = '')
else:
  print('0',end = '')
```

### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)