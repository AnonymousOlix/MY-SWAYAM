# Problem Solving through Programming in C

# Week 6

# Programming Assignment 1

```bash
#include <stdio.h>
int main()
{
    int i, n, largest;
    int arr[100];
    scanf("%d", &n); /*Accepts total number of elements from the test data */
for(i = 0; i < n; ++i)
    {
       scanf("%d", &arr[i]); /* Accepts the array element from test data */
    }
largest = arr[0];
for(i = 1; i < n; ++i)
    {
           if(largest < arr[i])
           largest = arr[i];
    }
    printf("Largest element = %d", largest);
    return 0;
}
```

# Programming Assignment 2

```bash
int j, temp;  
j = i - 1;   // last Element of the array
i = 0;       // first element of the array
   while (i < j) {
      temp = arr[i];
      arr[i] = arr[j];
      arr[j] = temp;
      i++;             
      j--;        
   }
```

# Programming Assignment 3

```bash
scanf("%d", &n2); //Get the size of second array from test data and store it in n2.
   for (i = 0; i < n2; i++)
      scanf("%d", &arr2[i]); //Accepts the values for second array
//Merge two arrays
int j;
for (i=0;i<n1;++i)
array_new[i]=arr1[i];
size =  n1 + n2;
for(i=0, j=n1; j<size && i<n2; ++i, ++j)
array_new[j] = arr2[i];
```

# Programming Assignment 4

```bash
int j, k;
   for (i = 0; i < size; i++) {
      for (j = i + 1; j < size;) {
         if (array[j] == array[i]) {
            for (k = j; k < size; k++) {
               array[k] = array[k + 1];
            }
            size--;
         } else
            j++;
      }
   }
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
