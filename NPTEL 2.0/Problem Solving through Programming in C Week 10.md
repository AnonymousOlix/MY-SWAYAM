# Problem Solving through Programming in C

# Week 10

# Programming Assignment 1

```bash
do
    {
        if (fun(a)*fun(x) < 0)
            b=x;
        else
            a=x;
        bisection (&x1, a, b, &itr);
        if (((x1-x)<0 && -(x1-x)< allerr) || ((x1-x)>0 && (x1-x)< allerr))
        {
            printf("Root = %1.4f\n", x1);
            return 0;
        }
        x=x1;
    }
    while (itr < maxmitr);
    return 1;
}
float fun (float x)
{
    return (2*x*x*x - 3*x - 5);
}
void bisection (float *x, float a, float b, int *itr)
{
    *x=(a+b)/2;
    ++(*itr);
}
```

# Programming Assignment 2

```bash
determinant = a[0][0] * ((a[1][1]*a[2][2]) - (a[2][1]*a[1][2])) -a[0][1] * (a[1][0]
   * a[2][2] - a[2][0] * a[1][2]) + a[0][2] * (a[1][0] * a[2][1] - a[2][0] * a[1][1]);
   if ( determinant == 0)
       printf("The given matrix is not invertible");
   else
       printf("The given matrix is invertible");
   return 0;
}
```

# Programming Assignment 3

```bash
int j,t;
for (i=0; i<(n-1); i++) 
    {
        for (j=i+1; j<n; j++)
        {
            if (*(a+i)>*(a+j))
            {
                t=*(a+i);
                *(a+i)=*(a+j);
                *(a+j)=t;
            }
        }
    }
```

# Programming Assignment 4

```bash
void sort(int *a, int n)
{
    int i,temp,j;
    for(i=1;i<n;i++)
    {
        for(j=0;j<n-i;j++)
        {
           if(*(a+j)>=*(a+j+1))
        {
            temp = *(a+j);
            *(a+j)= *(a+j+1);
            *(a+j+1)= temp;
        }
        }
    }
}
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
