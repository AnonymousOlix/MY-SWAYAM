# Problem Solving through Programming in C

# Week 9

# Programming Assignment 1

```bash
for (c = 0; c < n; c++)
    {
      if (array[c] == search)
      {
         printf("%d is present at location %d.\n", search, c+1);
         count++;
      }
    }
   if (count == 0)
      printf("%d is not present in the array.\n", search);
   else
      printf("%d is present %d times in the array.\n", search, count);
 
   return 0;
}
```

# Programming Assignment 2

```bash
position = linear_search(array, n, search);
   if (position == -1)
      printf("%d is not present in the array.\n", search);
   else
      printf("%d is present at location %d.\n", search, position+1);
   return 0;
}
 
int linear_search(int a[], int n, int find) {
   int c;
   for (c = 0 ;c < n ; c++ )
    {
      if (a[c] == find)
         return c;
    }
   return -1;
}
```

# Programming Assignment 3

```bash
int first, last, middle;
   first = 0;
   last = n - 1;
   middle = (first+last)/2;
 
   while (first <= last) {
      if (array[middle] < search)
         first = middle + 1;
      else if (array[middle] == search) {
         printf("%d found at location %d.\n", search, middle+1);
         break;
      }
      else
         last = middle - 1;
 
      middle = (first + last)/2;
      }
   if (first > last)
      printf("Not found! %d isn't present in the list.\n", search);
 
     return 0;
      }
```

# Programming Assignment 4

```bash
int temp, end;
   end = n - 1;
   for (c = 0; c < n/2; c++) {
    temp       = array[c];
    array[c]   = array[end];
    array[end] = temp;
 
    end--;
  }
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
