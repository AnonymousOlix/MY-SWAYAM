#	Programming, Data Structures And Algorithms Using Python

# Week 3
```
def remdup(l): 
    result = [] 
    for num in reversed (l): 
        if num not in result: 
            result.append(num) 
    return result[::-1] 
def splitsum(l): 
    pos = sum(x**2 for x in 1 if x > 0) 
    neg = sum(x**3 for x in 1 if x < 0) 
    return [pos, neg] 
def matrixflip(m, d): 
    if d == 'h': 
        return [row[::-1] for row in m] 
    elif d == 'v': 
        return m[::-1] 
    return m
```
