#	Programming, Data Structures And Algorithms Using Python

# Week 3
```
def remdup(l): 
    result = [] 
    for num in reversed (l): 
        if num not in result: 
            result.append(num) 
    return result[::-1] 
def splitsum(l): 
    pos = sum(x**2 for x in l if x > 0) 
    neg = sum(x**3 for x in l if x < 0) 
    return [pos, neg] 
def matrixflip(m, d): 
    if d == 'h': 
        return [row[::-1] for row in m] 
    elif d == 'v': 
        return m[::-1] 
    return m
```

# Week 5
```
import sys

def main():
    grade_points = {"A": 10, "AB": 9, "B": 8, "BC": 7, "C": 6, "CD": 5, "D": 4}
    
    students = {}
    grades = {}
    
    section = None
    for line in sys.stdin:
        line = line.strip()
        if line == "EndOfInput":
            break
        elif line == "Courses":
            section = "Courses"
        elif line == "Students":
            section = "Students"
        elif line == "Grades":
            section = "Grades"
        else:
            if section == "Students":
                roll_number, name = line.split("~")
                students[roll_number] = name
                grades[roll_number] = []
            elif section == "Grades":
                _, _, _, roll_number, grade = line.split("~")
                if roll_number in grades:
                    grades[roll_number].append(grade_points[grade])
    
    result = []
    for roll_number in sorted(students.keys()):
        if grades[roll_number]:
            gpa = round(sum(grades[roll_number]) / len(grades[roll_number]), 2)
        else:
            gpa = 0
        result.append(f"{roll_number}~{students[roll_number]}~{gpa}")
    
    print("\n".join(result))

if __name__ == "__main__":
    main()
```

# Week 8

```
def min_dragon_hunting_distance(R, C, K, D, dragons):
    # Sort dragons by row index
    dragons.sort()

    # Distance DP table: mindist[i][j] represents minimum distance to kill j dragons ending at dragon i
    INF = float('inf')
    dp = [[INF] * (K + 1) for _ in range(D)]

    # Base case: killing the first dragon from (0,0)
    for i in range(D):
        dp[i][1] = abs(dragons[i][0] - 0) + abs(dragons[i][1] - 0)

    # Fill DP table for j dragons
    for j in range(2, K + 1):
        for i in range(D):  # Ending dragon
            for x in range(i):  # Previous dragon
                cost = abs(dragons[i][0] - dragons[x][0]) + abs(dragons[i][1] - dragons[x][1])
                dp[i][j] = min(dp[i][j], dp[x][j - 1] + cost)

    # Find the minimum distance to kill exactly K dragons
    result = min(dp[i][K] for i in range(K - 1, D))

    return result


# Read input
R, C, K, D = map(int, input().split())
dragons = [tuple(map(int, input().split())) for _ in range(D)]

# Compute and print result
print(min_dragon_hunting_distance(R, C, K, D, dragons))
```
