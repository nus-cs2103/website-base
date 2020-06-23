#### Exercise: Get Subject Info

Complete the `get_subject_info` function below to return a dictionary such that the code produces the given output.

```python
def get_subject_info(code, name, level, is_core):
  return {} # UPDATE THIS LINE
  
print(get_subject_info('TE3201', 'Software Engineering', 3, False))
print(get_subject_info('CS1101', 'Programming Basics', 1, True))
```
{{ icon_output }}
```
{'code': 'TE3201', 'name': 'Software Engineering', 'level': 3, 'core?': False}
{'code': 'CS1101', 'name': 'Programming Basics', 'level': 1, 'core?': True}
```

<panel type="seamless" header="%%:fas-battery-quarter: Partial solution%%">

```python
def get_subject_info(code, name, level, is_core):
  return {'code': code, ...} 
  
print(get_subject_info('TE3201', 'Software Engineering', 3, False))
```

</panel>