# Problem Solving through Programming in C

# Week 8

# Programming Assignment 1

```bash
int HCF(int a, int b) {
    if (b == 0)
        return a;
    return HCF(b, a % b);
}
```

# Programming Assignment 2

```bash
long power(int base, int exponent) {
    if (exponent == 0)
        return 1;  // base case: any number to the power of 0 is 1
    else
        return base * power(base, exponent - 1);  // recursive step
}
```

# Programming Assignment 3

```bash
int binary_conversion(int num) {
    if (num == 0)
        return 0;
    else
        return (num % 2) + 10 * binary_conversion(num / 2);
}
```

# Programming Assignment 4

```bash
int num = 2; // Start checking for prime numbers from 2
   int printed = 0;

   for (int i = 1; i <= lines; i++) {
       int count = 0; // Number of primes printed in the current line

       while (count < i) {
           if (prime(num)) {
               printf("%d\t", num); // Print prime number with tab spacing
               count++;
           }
           num++;
       }
       printf("\n"); // New line after each row
   }

   return 0;
}

// Function to check if a number is prime
int prime(int num) {
   if (num < 2)
       return 0;
   for (int i = 2; i * i <= num; i++) {
       if (num % i == 0)
           return 0;
   }
   return 1;
}
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
