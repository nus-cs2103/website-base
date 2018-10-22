**Questions to discuss during tutorial:**

Whole team: do this question together, using the whiteboard:

<div class="indented">
  <include src="../../book/modeling/modelingBehaviors/activityDiagrams/q-modelWorkflowOfBurgerShop.md" />
</div>
<br>

Divide these five questions among team members. Be prepared to answer questions allocated to you.

**Q1**
1. What’s the use of assertions?
1. Demonstrate an assertion failure using Intellij.
1. What’s the purpose of logging levels? What are the available logging levels in AB4?

**Q2**
1. What is _Liskov Substitution Principle_?<br>
   Give an example from the project where LSP is followed and explain how to change the code to break LSP.

**Q3**
1. What is _defensive programming_?<br>
   Give an example of defensive programming from your project.

**Q4**
1. What’s the difference between _validation_ and _verification_?<br>
   Acceptance tests are validation tests or verification tests?
1. Give an example of _static analysis_ being used in Intellij

**Q5**
1. Explain how _Law of Demeter_ affects coupling<br>
   a. Add a line to this code that violates LoD
   ```java
   void foo(P p){
       //...
   }
   ```
1. Give an example in the project code that violates the _Law of Demeter_.
1. What’s the problem with the architecture diagram on the right?<br>
   <img src="{{baseUrl}}/book/architecture/architectureDiagrams/drawing/images/tip.png" height="190" /><br>


