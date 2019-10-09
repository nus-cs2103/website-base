{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(10, "tutorial") }}

**Questions to discuss during tutorial:**

<div class="indented">
  <include src="../../book/modeling/modelingBehaviors/activityDiagrams/q-modelWorkflowOfBurgerShop.md" />
</div>
<br>


Divide these questions among team members and get ready to answer them.

**Q2**
1. Explain and justify: _testing should be efficient and effective_
1. Explain how _exploratory_ and _scripted_ testing is used in AB3/project
1. Give an example of a _negative_ test case in AB3/project
1. Explain _grey-box_ test case design

**Q3**
1. Explain: _Equivalence Partition_ improve E&E of testing
1. What are the EPs for the parameter `day` of this method
   ```java
   /**
    * Returns true if the three values represent a valid day
    */
   boolean isValidDay(int year, int month, int day){
   
   } 
   ```

**Q4**
1. Explain: _Boundary Value Analysis_ improves E&E of testing
1. What are the boundary values for the parameter `day` in the question above?
1. How can EP and BVA heuristics be used in AB3/project? Hint: See [[AB3 Learning Outcomes: LO-TestCaseDesignHeuristics]({{module_org}}/addressbook-level3/blob/master/docs/LearningOutcomes.adoc#apply-test-case-design-heuristics-code-lo-testcasedesignheuristics-code)]

**Q5**
1. What’s a _design pattern_?
1. When do you use the _Singleton_ pattern, _Facade_ pattern, _Command_ pattern?
1. Which of the three patterns are used in AB3? Hint: See [[AB3 Learning Outcomes: LO-DesignPatterns]({{module_org}}/addressbook-level3/blob/master/docs/LearningOutcomes.adoc#apply-design-patterns-code-lo-designpatterns-code)]


**Q1**
1. What’s the use of assertions?
1. Demonstrate an assertion failure using Intellij.
1. What’s the purpose of logging levels? What are the available logging levels in AB3?
**Q3**
1. What is _defensive programming_?<br>
   Give an example of defensive programming from your project.

**Q4**
1. What’s the difference between _validation_ and _verification_?<br>
   Acceptance tests are validation tests or verification tests?
1. Give an example of _static analysis_ being used in Intellij