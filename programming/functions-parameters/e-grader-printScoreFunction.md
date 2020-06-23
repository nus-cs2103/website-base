#### Exercise : Grader - `print_score` Function

The code below prints the grade based on exam and project score, somewhat similar to <trigger trigger="click" for="modal:printScoreFunction-gradeAnalyzer">a previous exercise you did</trigger>.
```python
project_score = int(input('Enter project score:'))
exam_score = int(input('Enter exam score:'))
total_score = project_score + exam_score
print('Total:', total_score)

if total_score >= 60 and project_score >= 25 and exam_score >= 25:
    grade = 'A'
elif (total_score >= 50) and (project_score >= 25 or exam_score >= 25):
    grade = 'B'
elif total_score >= 40:
    grade = 'C'
else:
    grade = 'D'

print('Project :', '=' * (project_score//5))
print('Exam    :', '=' * (exam_score//5))
print('Total   :', '=' * (total_score//5))
print('Grade   :', grade)
```
Read the above code to understand how it works. Do you remember <trigger trigger="click" for="printScoreFunction-operators">the meaning of `//` operator</trigger> used in the code above?

<modal large header="%%Programming Basics » Expressions, Data Types, Variables »%%" id="printScoreFunction-operators">
  <include src="../operators/text.md"/>
</modal>

Add a `print_score` function to the code and replace the following three lines,
  
```python
print('Project :', '=' * (project_score//5))
print('Exam    :', '=' * (exam_score//5))
print('Total   :', '=' * (total_score//5))
```

with these three lines,
  
```python
print_score('Project :', project_score)
print_score('Exam    :', exam_score)
print_score('Total   :', total_score)
```
without changing the external behavior of the program.

<modal large header="" id="modal:printScoreFunction-gradeAnalyzer">
  <include src="../if/e-grades.md"/>
</modal>