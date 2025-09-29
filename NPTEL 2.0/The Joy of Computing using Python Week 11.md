# The Joy of Computing using Python

# Week 11

# Programming Assignment 1

```bash
# Helper function to check if a number is prime
def is_prime(x):
    if x <= 1:
        return False
    for i in range(2, int(x ** 0.5) + 1):
        if x % i == 0:
            return False
    return True

# Main function to find all prime pairs that sum up to n
def Goldbach(n):
    # List to store valid prime pairs
    pairs = []
    
    # Iterate over numbers from 2 to n//2
    for a in range(2, n // 2 + 1):
        b = n - a
        # Check if both a and b are prime numbers and a <= b
        if is_prime(a) and is_prime(b) and a <= b:
            pairs.append((a, b))
    
    return pairs

# Input and Output handling
n = int(input())  # Read the input number
result = Goldbach(n)  # Get the Goldbach pairs
print(result)  # Output the result

```

# Programming Assignment 2

```bash
def find_Min_Difference(L, P):
    # Step 1: Sort the list of scores
    L.sort()
    
    # Step 2: Initialize the minimum difference to a large value
    min_diff = float('inf')
    
    # Step 3: Iterate through the list with a sliding window of size P
    for i in range(len(L) - P + 1):
        # Calculate the difference between the highest and lowest score in this window
        current_diff = L[i + P - 1] - L[i]
        
        # Update the minimum difference
        min_diff = min(min_diff, current_diff)
    
    # Step 4: Return the smallest difference found
    return min_diff

# Example input/output handling
L = [3, 4, 1, 9, 56, 7, 9, 12]
P = 5
```

# Programming Assignment 3

```bash
def encrypt_message(message, shift):
    encrypted_message = []
    
    for char in message:
        if char.isalpha():  # Only shift letters
            # Shift character and ensure wrapping using modulo 26
            new_char = chr((ord(char) - ord('A') + shift) % 26 + ord('A'))
            encrypted_message.append(new_char)
        else:
            # Leave spaces and punctuation unchanged
            encrypted_message.append(char)
    
    # Join the list into a string and return it
    return ''.join(encrypted_message)

# Input reading and function calling
message = input().strip()  # The message to be encrypted
shift = int(input())  # The shift value

# Output the encrypted message
print(encrypt_message(message, shift))

```

### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
