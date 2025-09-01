# Design and Analysis of Algorithms

# Week 7

# Programming Assignment 1

```bash
public static String findLongestWord(String text) {
        String longestWord = "";
        
        // Split the text into words based on whitespace
        String[] words = text.split("\\s+");
        
        // Iterate through each word to find the longest one
        for (String word : words) {
            if (word.length() > longestWord.length()) {
                longestWord = word;
            }
        }
        
        return longestWord;
    }
```

# Programming Assignment 2

```bash
public static int[] removeAll(int[] array, int elementToRemove) {
        int[] result = new int[array.length];
        int index = 0;

        // Iterate through the original array
        for (int value : array) {
            // Copy only if the current element is not equal to the element to be removed
            if (value != elementToRemove) {
                result[index++] = value;
            }
        }

        // If the resulting array is smaller than the original, resize it
        return Arrays.copyOf(result, index);
    }
```

# Programming Assignment 3

```bash
// Helper method to check if a number is prime
    private static boolean isPrime(int num) {
        if (num <= 1) {
            return false;
        }
        for (int i = 2; i <= Math.sqrt(num); i++) {
            if (num % i == 0) {
                return false;
            }
        }
        return true;
    }
    
    // Method to compute sum of prime numbers in range [x, y]
    public static int primeSum(int x, int y) {
        int sum = 0;
        for (int i = x; i <= y; i++) {
            if (isPrime(i)) {
                sum += i;
            }
        }
        return sum;
    }
```

# Programming Assignment 4

```bash
private int start;
    private int end;
    
    public PrintNumbers(int start, int end) {
        this.start = start;
        this.end = end;
    }
    
    @Override
    public void run() {
        for (int i = start; i <= end; i += 2) {
            System.out.println(Thread.currentThread().getName() + ": " + i);
        }
    }

```

# Programming Assignment 5

```bash
// Method to check if password is valid
    public boolean isValidPassword(String password) {
        // Step 1: Check if the password length is at least 8 characters
        if (password.length() < 8) {
            return false;
        }

        // Flags to track uppercase letter and number
        boolean hasUpperCase = false;
        boolean hasDigit = false;

        // Step 2: Loop through each character in the password
        for (char ch : password.toCharArray()) {
            if (Character.isUpperCase(ch)) {
                hasUpperCase = true;
            }
            if (Character.isDigit(ch)) {
                hasDigit = true;
            }

            // If both conditions are met, no need to check further
            if (hasUpperCase && hasDigit) {
                return true;
            }
        }

        // Step 3: Return true only if both conditions are met
        return hasUpperCase && hasDigit;
    }
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
