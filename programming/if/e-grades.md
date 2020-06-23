#### Exercise - Grade Analyzer

Write a program to read project score and exam score from the keyboard and print a bar chart of the scores and a grade. Follow the example below:
```python
Enter project score:
30

Enter exam score:
40

Total: 70

Project : ======
Exam    : ========
Total   : ==============
Grade   : A
```

* Note how the colons (`:`) are aligned.
* Note the extra blank lines in the expected output.
* The bar chart has one `=` for each 5 marks %%&nbsp;24 marks should be shown as `====`.%%
* Assume all inputs are positive integers.

Grading rules: 
* `A`: at least 25 marks for each component and at least 60 in total
* `B`: at least one component has 25 or more marks and at least 50 in total 
* `C`: at least 40 in total
* `D`: otherwise