# Problem Solving through Programming in C

# Week 5 

# Programming Assignment 1

```bash
int sum = 0;
    for (int i = 1; i <= N / 2; i++) {
        if (N % i == 0) {
            sum += i;  // add proper divisor
        }
    }

    if (sum == N) {
        printf("%d is a perfect number.", N);
    } else {
        printf("%d is not a perfect number.", N);
    }
    
    return 0;
}
```

# Programming Assignment 2

```bash
int count = 0;
    int temp = N;
    
    if (temp == 0) {
        count = 1;  // zero has 1 digit
    } else {
        if (temp < 0) {
            temp = -temp;  // handle negative numbers
        }
        while (temp > 0) {
            temp /= 10;
            count++;
        }
    }
    
    printf("The number %d contains %d digits.", N, count);
    
    return 0;
}
```

# Programming Assignment 3

```bash
if (N > 0 && (N & (N - 1)) == 0) {
        printf("%d is a number that can be expressed as power of 2.", N);
    } else {
        printf("%d cannot be expressed as power of 2.", N);
    }

    return 0;
}
```

# Programming Assignment 4

```bash
for (int i = N; i >= 1; i--) {
        for (int j = 1; j <= i; j++) {
            printf("*");
        }
        printf("\n");
    }
    
    return 0;
}
```

### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
