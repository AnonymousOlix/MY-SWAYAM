# Problem Solving Through Programming in C

# Week 5 

# Programming Assignment 1

```bash
int i, sum=0;
    for(i=1; i<N;i++)
    {
        if(N%i==0)
            sum+=i;
    }
 
    if(sum==N)
        printf("%d is a perfect number.",N);
    else
        printf("%d is not a perfect number.",N);
}
```

# Programming Assignment 2

```bash
int temp, count; 
count=0;
    temp=N;
    while(temp>0)
    {
        count++;
        temp/=10;
    }
     printf("The number %d contains %d digits.",N,count);
}
```

# Programming Assignment 3

```bash
int temp, flag;
    temp=N;
    flag=0;
   
    while(temp!=1)
    {
        if(temp%2!=0){
            flag=1;
            break;
        }
        temp=temp/2;
    }
  
    if(flag==0)
        printf("%d is a number that can be expressed as power of 2.",N);
    else
        printf("%d cannot be expressed as power of 2.",N);
}
```

# Programming Assignment 4

```bash
int i,j;
for(i=N; i>0; i--)
  {
  for(j=0;j<i;j++)
    {
    printf("*");
    }
  printf("\n");
  } 
}
```


### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)