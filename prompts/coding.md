# Coding Prompts

This file contains prompt engineering examples related to
coding and software development.

---

## Prompt #1 — Python Program Generation

### Domain
Coding

### Prompt Technique
Zero-shot

### Use Case
Generating a beginner-friendly Python program for calculating
student marks and grades.

---

## 1. Bad Prompt

> Write a Python program for students.

### Why is this a bad prompt?

The prompt is vague and does not specify the exact task,
inputs, expected output, complexity level, or requirements.
The AI therefore has to make assumptions.

---

## 2. Bad Prompt Output


```python
name = input("Enter student name: ")

mark1 = int(input("Enter marks in Subject 1: "))
mark2 = int(input("Enter marks in Subject 2: "))
mark3 = int(input("Enter marks in Subject 3: "))

total = mark1 + mark2 + mark3
average = total / 3

print("\n--- Student Result ---")
print("Name:", name)
print("Total Marks:", total)
print("Average:", average)

if average >= 90:
    print("Grade: A")
elif average >= 75:
    print("Grade: B")
elif average >= 60:
    print("Grade: C")
elif average >= 50:
    print("Grade: D")
else:
    print("Grade: F")
```
```text
Example Output
Enter student name: Rahul
Enter marks in Subject 1: 85
Enter marks in Subject 2: 90
Enter marks in Subject 3: 80

--- Student Result ---
Name: Rahul
Total Marks: 255
Average: 85.0
Grade: B
```

## 3. Optimized Prompt

> Act as an experienced Python developer.
>
> Create a beginner-friendly Python program that calculates
> the total marks, average marks, and grade of a student.
>
> Requirements:
> - Accept marks for five subjects as input.
> - Calculate the total marks.
> - Calculate the average.
> - Assign a grade based on the average.
> - Validate that marks are between 0 and 100.
> - Display the total, average, and grade clearly.
> - Use meaningful variable names.
> - Add brief comments to explain the important parts of the code.
>
> The code should be simple enough for a beginner to understand.

---

## 4. Optimized Prompt Output
```python
subject1 = float(input("Enter marks for Subject 1: "))
subject2 = float(input("Enter marks for Subject 2: "))
subject3 = float(input("Enter marks for Subject 3: "))
subject4 = float(input("Enter marks for Subject 4: "))
subject5 = float(input("Enter marks for Subject 5: "))

marks = [subject1, subject2, subject3, subject4, subject5]

if any(mark < 0 or mark > 100 for mark in marks):
    print("Invalid marks! Marks must be between 0 and 100.")

else:
    total_marks = sum(marks)
    average_marks = total_marks
    if average_marks >= 90:
        grade = "A"
    elif average_marks >= 80:
        grade = "B"
    elif average_marks >= 70:
        grade = "C"
    elif average_marks >= 60:
        grade = "D"
    else:
        grade = "F"
    print("\n--- Student Result ---")
    print("Total Marks:", total_marks)
    print("Average Marks:", average_marks)
    print("Grade:", grade)
```
```text
Example output
Enter marks for Subject 1: 85
Enter marks for Subject 2: 90
Enter marks for Subject 3: 78
Enter marks for Subject 4: 88
Enter marks for Subject 5: 92

--- Student Result ---
Total Marks: 433
Average Marks: 86.6
Grade: B
```
## 5. Why the Optimized Prompt Is Better

The optimized prompt improves the original prompt by:

1. **Defining a role** — The AI is instructed to act as an experienced Python developer.
2. **Clearly defining the task** — The required program is specifically described.
3. **Providing input requirements** — Five subject marks must be accepted.
4. **Defining processing requirements** — Total, average, and grade must be calculated.
5. **Adding validation** — The program must reject marks outside the 0–100 range.
6. **Defining the expected output** — Results must be displayed clearly.
7. **Specifying the target audience** — The code should be beginner-friendly.
8. **Improving code quality** — Meaningful variable names and comments are required.

### Key Lesson

A good prompt provides sufficient context, constraints,
requirements, and expected output instead of leaving the AI
to guess the user's intention.

---

## 6. Prompt Engineering Principles Demonstrated

- Role prompting
- Task specification
- Context
- Constraints
- Output requirements
- Audience specification

## Prompt #2 — Debugging Python Code

### Domain
Coding

### Prompt Technique
Zero-shot

### Use Case
Identifying and fixing errors in Python code.

---

## 1. Bad Prompt
```python
Fixed Code
numbers = [10, 20, 30, 40, 50]
average = sum(numbers) / len(numbers)

print("Average:", average)
```
---

## 2. Bad Prompt Output

```text
Output
Average: 30.0
```
---

## 3. Optimized Prompt

Act as an experienced Python developer.

Fix the following Python code and explain the problem in a beginner-friendly way.

Requirements:
- Identify the error.
- Explain why the error occurs.
- Provide the corrected code.
- Show the expected output.
- Keep the code simple.

Code:

numbers = [10, 20, 30, 40, 50]
average = sum(numbers) / 0

print("Average:", average)

---

## 4. Optimized Prompt Output
```text
1. Error

The error is here:

average = sum(numbers) / 0

You are trying to divide by 0, which is not allowed in Python. It causes a ZeroDivisionError.

2. Why does it happen?

To calculate an average:

Average = Total ÷ Number of values

There are 5 numbers in the list, so we should divide the sum by len(numbers), not 0.

3. Corrected code
```python
numbers = [10, 20, 30, 40, 50]

average = sum(numbers) / len(numbers)

print("Average:", average)
```
```text
4. Expected output
Average: 30.0
```
---

## 5. Why the Optimized Prompt Is Better

The optimized prompt is better because:

1. It clearly tells the AI what to do.
2. It asks the AI to identify the error.
3. It asks for an explanation.
4. It asks for the corrected code.
5. It asks for the expected output.
6. It is easy for a beginner to understand.

---

## 6. Prompt Engineering Principles Demonstrated

- Role prompting
- Clear task definition
- Error identification
- Output requirements
- Audience specification
- Constraints
