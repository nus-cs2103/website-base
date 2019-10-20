{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(11, "tutorial") }}

**A. One member do a quick demo of your v1.3 using the jar file** (preferably a different member from previous weeks):

**B. Whole team: do this question together, using the whiteboard**

<div class="indented">
  <include src="../../book/testCaseDesign/combiningTestInputs/mix/q-testCasesForConsumeMethod.md" />
</div>
<br>

**C. Divide these questions among team members and get ready to answer them.**

1. Distinguish between _sequential_ and _iterative_ processes. Which one are we using in the project?
1. Distinguish between _breadth-first_ and _depth-first_ iterative processes using your project as an example.
1. Describe how _agile process models_ differ from traditional process models.
1. When do you use _MVC_ pattern? Do we have MVC in AB3?
1. When do you use the _Observer_ pattern? Do we have the Observer pattern in AB3?

**D. Divide XP and Scrum between the two teams** for the following activity, if there is enough time left.

* Each team use the Web to find about 5 distinguishing features of the process model.
  * Some interesting [SCRUM concepts](https://www.scrum.org/resources/what-is-scrum): Product backlog, scrum board, story points, burndown charts, scrum master, product owner
  * XP rules are described at [http://www.extremeprogramming.org/rules.html](http://www.extremeprogramming.org/rules.html)

* Relate those features to your project. %%i.e. are they applicable? are you doing something similar?%%

1. What are the EPs for the parameter `day` of this method
   ```java
   /**
    * Returns true if the three values represent a valid day
    */
   boolean isValidDay(int year, int month, int day){
   
   } 
   ```
1. What are the boundary values for the parameter `day` in the question above?
1. What’s the purpose of logging levels? What are the available logging levels in AB3?
1. Demonstrate an assertion failure using Intellij.
1. Give an example of defensive programming from your project.