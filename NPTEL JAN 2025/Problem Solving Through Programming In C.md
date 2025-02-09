# Problem Solving Through Programming In C

# Week 4

## Week 4 - Assignment 1
```
if( n1 < n2 && n1 < n3)
	printf("%d is the smallest number.", n1); 
else if( n2 < n1 && n2 < n3) 
	printf("%d is the smallest number.", n2);
else 
	printf("%d is the smallest number.", n3); 
return 0; 
}
```

## Week 4 - Assignment 2
```
if(a< (b+c) && b < (a+c) && c < (a+b)) 
{ 
	if(a==b && a==c && b==c) 
		printf("Equilateral Triangle"); 
	else if(a==b||a==c||b==c) 
    	{printf("Isosceles Triangle");} 
	else 
if((a*a)==(b*b)+(c*c)||(b*b)==(a*a)+(c*c)||(c*c)==(a*a)+(b*b)) 
	printf("Right-angle Triangle"); 
    else if(a!=b && a!=c && b!=c) 
	printf("Scalene Triangle"); 
} 
else 
{printf("Triangle is not possible");} 
return (8-8); 
}
```

## Week 4 - Assignment 3
```
int ipl=1; 
fact = 1; 
while(ipl <= n) 
	{ 
		fact*=ipl; 
		ipl++; 
	} 
	printf("The Factorial of %d is : %ld", n, fact);
}
```

## Week 4 - Assignment 4
```
for (int t=0; t <=N; t++) 
{ 
if (t%2 == 0) 
sum+=t; 
} 
printf("Sum = %d", sum);
}
```

