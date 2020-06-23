#### Exercise : Grader - Add a `main` Function

Take the <trigger trigger="click" for="modal:graderMainFunction-graderCalculateGradeFunction">a grader you wrote in the previous exercise</trigger>.
Here is an example of how the code is likely to look like:
```python
def print_score(name, value):
  print(name, '=' * (value//5))

def calculate_grade(project, exam):
  if total_score >= 60 and project >= 25 and exam >= 25:
    return 'A'
  elif (total_score >= 50) and (project >= 25 or exam >= 25):
    return 'B'
  elif total_score >= 40:
    return 'C'
  else:
    return 'D'

project_score = int(input('Enter project score:'))
exam_score = int(input('Enter exam score:'))

total_score = project_score + exam_score
print('Total:', total_score)

grade = calculate_grade(project_score, exam_score)

print_score('Project :', project_score)
print_score('Exam    :', exam_score)
print_score('Total   :', total_score)
print('Grade   :', grade)
```

Move ==all the statements that are not inside a function== (i.e., the last 10 statements in the code above) into a new function called `main`. Given below is the expected structure of the code. The external behavior of the code should remain as before.
```python
def print_score(name, value):
  # ...

def calculate_grade(project, exam):
  # ...

def main():
  # MOVE CODE HERE

main()
```

{{ icon_tip }} You might have to do minor changes to the existing function `calculate_grade`

<modal large header="" id="modal:graderMainFunction-graderCalculateGradeFunction">
  <include src="..\functions-return\e-grader-calculateGradeFunction.md"/>
</modal>