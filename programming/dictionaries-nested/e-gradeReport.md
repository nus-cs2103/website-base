#### Exercise: Grade Report

Write a program that reads student grades one entry at a time and print a consolidated grade report at the end. Follow the sample output given below.

```
-----------------------------------------------------
     ~ Welcome to Grade Report System ~
* Enter one entry at a time in the format NAME GRADE
* NAME should be one word
* Enter an empty line to proceed to printing report
-----------------------------------------------------
Student name and grade? amy A
Student name and grade? ben B
Student name and grade? ben 
Invalid input! Entry rejected.
Student name and grade? ben C D
Invalid input! Entry rejected.
Student name and grade? ben A
Student name and grade? charlie F
Student name and grade? amy A+
Student name and grade? amy D
Student name and grade? 
============ Grade Report ===============
amy : A A+ D
ben : B A
charlie : F
```

<panel type="seamless" header="%%:bulb: Python hints%%">

* use a dictionary of this format to store grades:
  ```python
  {'amy': ['A', 'A+', 'D'],
   'ben': ['B', 'A'],
   'charlie': ['F']}
  ```
* The program should be able to accept any name (but you can assume each name is only one word e.g., `Jane` but not `Jane Doe`), not just the three names mentioned in the example above.
* The string method `split()` can be useful to break the user entry into name and grade.<br>
  As you know,`'aaa bbb ccc'.split()` evaluates to a list `['aaa', 'bbb', 'ccc']`
* The string method `join()` can be useful when printing grades.<br>
  As you know, `' '.join(['aaa', 'bbb', 'ccc'])` evaluates to `'aaa bbb ccc'`

</panel>