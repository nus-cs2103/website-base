#### Exercise : Grader - Restructure the `main` Function

Take the <trigger trigger="click" for="modal:graderRestructureMain-graderMainFunction">a grader you wrote in the previous exercise</trigger>.
Restructure the `main` function so that its code looks as follows:
```python
def print_score(name, value):
  # ...

def calculate_grade(project, exam):
  # ...

# ADD MISSING FUNCTIONS

def main():
  project_score = read_number('Enter project score:')
  exam_score = read_number('Enter exam score:')
  grade = calculate_grade(project_score, exam_score)
  print_report(project_score, exam_score, grade)

main()
```

The external behavior of the code should remain as before.

{{ icon_tip }} You need to add functions `read_number` and `print_report`.

<modal large header="" id="modal:graderRestructureMain-graderMainFunction">
  <include src="e-grader-addMainFunction.md"/>
</modal>