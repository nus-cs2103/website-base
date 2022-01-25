#### Exercise : Grader - Analyze Grades in a Loop

Take the program you wrote in the <trigger trigger="click" for="modal:analyzeGradesInLoop-restructureMain">previous exercise</trigger>. Enhance it to analyze grades in a loop until the user chooses to stop. A sample output is given below:
```python
Enter project score:10
Enter exam score:50
Total: 60
Project : ==
Exam    : ==========
Total   : ============
Grade   : B
Continue y/n?y
Enter project score:50
Enter exam score:49
Total: 99
Project : ==========
Exam    : =========
Total   : ===================
Grade   : A
Continue y/n?n
```

<modal large header="" id="modal:analyzeGradesInLoop-restructureMain">
  <include src="e-grader-restructureTheMainFunction.md"/>
</modal>