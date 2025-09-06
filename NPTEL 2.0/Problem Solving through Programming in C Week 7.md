# Problem Solving through Programming in C

# Week 7

# Programming Assignment 1

```bash
for (int i = 0; ch[i] != '\0'; i++) {
        if (ch[i] >= 'A' && ch[i] <= 'Z') {
            upper++;  // Count uppercase letters
        } else if (ch[i] >= 'a' && ch[i] <= 'z') {
            lower++;  // Count lowercase letters
        }
    }
```

# Programming Assignment 2

```bash
for (i = 0; i < r; i++)
    {
        int sum = 0;
        for (j = 0; j < c; j++)
        {
            sum += matrix[i][j];
        }
        printf("%d\n", sum);  // Required format
    }

    return 0;
}
```

# Programming Assignment 3

```bash
for (i = 0; i < row; i++)
    {
        for (j = 0; j < col; j++)
        {
            matrix_C[i][j] = matrix_A[i][j] - matrix_B[i][j];
            printf("%d ", matrix_C[i][j]);
        }
        printf("\n"); // Move to next line after each row
    }

    return 0;
}
```

# Programming Assignment 4

```bash
for (i = 0; i < r; i++)
    {
        for (j = 0; j < r; j++)
        {
            if (j <= i)
                printf("%d ", matrix[i][j]);
            else
                printf("0 ");
        }
        printf("\n"); // Move to next line after each row
    }

    return 0;
}
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
