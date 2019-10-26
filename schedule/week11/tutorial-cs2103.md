{% from "common/macros.njk" import embed_topic, thumb, show_as_tab, timing_badge with context %}
{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(11, "tutorial") }}

#### {{ thumb(1) }} Demo v1.3

* One member is to do a quick demo of your `v1.3` ==using the jar file==. Make sure the jar file is ==in an empty folder== before you start. Others can help to confirm the jar file works on other OS'es.

<div class="indented-level2">
<box type="success" border-left-color="green" icon="">

You may release a newer version to be used for the PE dry run, but make sure it is released <span class="text-danger">by Friday 10am</span>.
</box>
</div>

#### {{ thumb(2) }} Exercise: test case design

* Divide into sub-teams and do the following exercises on the white board. Both sub-teams should do both exercises.

1. What are the EPs for the parameter `day` of this method
   ```java
   /**
    * Returns true if the three values represent a valid day
    */
   boolean isValidDay(int year, int month, int day){
   
   } 
   ```
1. What are the boundary values for the parameter `day` in the question above?

<div class="indented-level2">
  <include src="../../book/testCaseDesign/combiningTestInputs/mix/q-testCasesForConsumeMethod.md" />
</div>
<br>

#### {{ thumb(3) }} Exercise: defensive programming

1. Demonstrate an assertion failure using Intellij.
1. Give an example of defensive programming from your project.

#### {{ thumb(4) }} Exercise: process models

* Divide XP and Scrum between the two sub-teams.

* Each sub-team to use the Web to find about 5 distinguishing features of the process model.
  * Some interesting [SCRUM concepts](https://www.scrum.org/resources/what-is-scrum): Product backlog, scrum board, story points, burndown charts, scrum master, product owner
  * XP rules are described at [http://www.extremeprogramming.org/rules.html](http://www.extremeprogramming.org/rules.html)

* Relate those features to your project. %%i.e. are they applicable? are you doing something similar?%%
