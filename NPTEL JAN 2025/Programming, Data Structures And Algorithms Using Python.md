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
