# The Joy of Computing using Python

# Week 4

## Week 4 - Assignment 1
```
def is_diagonal_matrix(matrix, n): 
	for i in range(n): 
		for j in range(n): 
			#Check if the element is off the main diagonal and not zero 
			if i!= j and matrix[i][j] != 0: 
				return 0
	return 1 

#Read matrix dimensions 
r = int(input()) 

#Read the matrix elements 
matrix = [] 
print() 
for _ in range(r): 
	row = list(map(int, input().split())) 
	matrix.append(row) 

#Check if the matrix is diagonal and print the result 
result = is_diagonal_matrix(matrix, r) 
print(result)
```

## Week 4 - Assignment 2
```
def transpose_and_add_scalar (matrix, scalar): 
	#Get the dimensions of the matrix 
	rows = len(matrix) 
	cols = len(matrix[0]) 

    # Compute the transpose and add the scalar 
	result = [] 
	for j in range(cols): 
		row_result = [] 
		for i in range(rows): 
			row_result.append(matrix[i][j] + scalar) 
		result.append(row_result) 
	return result 
#Read matrix dimensions 
r = int(input())
c = int(input())

#Read the matrix elements 
matrix = [] 
print() 
for _ in range(r): 
	row = list(map(int, input().split())) 
	matrix.append(row) 

#Read the scalar value 
scalar = int(input()) 

#Compute the result 
result = transpose_and_add_scalar(matrix, scalar) 

#Print the resulting matrix 
for row in result: 
	print(*row)
```

## Week 4 - Assignment 3
```
def is_symmetric_matrix(matrix, n): 
	#Check if the matrix is symmetric 
	for i in range(n): 
		for j in range(n): 
			if matrix[i][j] != matrix[j][i]: 
				return 0
	return 1 

#Read matrix dimensions 
r = int(input()) 

#Read the matrix elements 
matrix = [] 
print() 
for _ in range(r): 
	row = list(map(int, input().split())) 
	matrix.append(row) 

#Check if the matrix is symmetric and print the result 
result = is_symmetric_matrix(matrix, r) 
print(result)
```
