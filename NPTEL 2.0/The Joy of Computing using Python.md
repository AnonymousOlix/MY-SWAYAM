# The Joy of Computing using Python

# Week 5 

# Programming Assignment 1

```bash
def factors(n):
    """Return all positive factors of n."""
    return [iii for iii in range(1, n + 1) if n % iii == 0]

# Read choice
choice = int(input().strip())

if choice == 1:
    n = int(input().strip())
    print(factors(n))

elif choice == 2:
    a = int(input().strip())
    b = int(input().strip())
    fa = factors(a)
    fb = factors(b)
    common = sorted(set(fa) & set(fb))
    print(common)

elif choice == 3:
    n = int(input().strip())
    factor_dict = {i: factors(i) for i in range(1, n + 1)}
    print(factor_dict)

else:
    print("Invalid choice")
```

# Programming Assignment 2

```bash
n = int(input().strip())
station_dict = {}

for baba in range(n):
    train_name = input().strip()
    m = int(input().strip())
    compartments = {}
    for _ in range(m):
        comp, passengers = input().strip().split(",")
        compartments[comp] = int(passengers)
    station_dict[train_name] = compartments

# Print in sorted order of train names
print({k: station_dict[k] for k in sorted(station_dict)})
```

# Programming Assignment 3

```bash
def exact_count(para, n):
    # Split paragraph into words
    words = para.split()
    
    # Count frequencies
    freq = {}
    for wind in words:
        freq[wind] = freq.get(wind, 0) + 1
    
    # Check if any word count == n
    return any(count == n for count in freq.values())
```

### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
