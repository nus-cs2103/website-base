**Show evidence of achieving mid-v1.3 team/individual milestone**
* [One member] Show the mid-v1.3 release and the milestone on GitHub
* [Each member] Demo your contribution for mid-v1.3 using the jar file 

**Questions to discuss during tutorial:**

==While the tutor is checking team/individual milestones, divide these questions among team members and get ready to answer them==. 

1. Explain and justify: _testing should be efficient and effective_<br>
   a. Explain _exploratory_ and _scripted_ testing<br>
   b. Give an example of a _negative_ test case in AB4<br>
   c. Explain _grey-box_ testing
   
1. What is an _Equivalence Partition_?<br>
   a. How does it help to improve E&E of testing?<br>
   b. What are the EPs for the parameter `day` of this method<br>
   ```java
   /**
    * Returns true if the three values represent a valid day
    */
   boolean isValidDay(int year, int month, int day){
   
   } 
   ``` 
1. How does _Boundary Value Analysis_ improve E&E of testing?<br>
   a. What are the boundary values for the parameter `day` in the question above?
   
1. What’s a _design pattern_?<br>
   a. When do you use the _Singleton_ pattern, _Facade_ pattern, _Command_ pattern?<br>
   b. Which of the three patterns are used in AB4? Hint: See [[AB4 Learning Outcomes: LO-DesignPatterns]({{module_org}}/addressbook-level4/blob/master/docs/LearningOutcomes.adoc#apply-design-patterns-code-lo-designpatterns-code)]
1. Explain basic AD notation using the example below:<br>
   <img src="https://upload.wikimedia.org/wikipedia/commons/e/e7/Activity_conducting.svg"><br>
   <sub>[[source:wikipeida](https://en.wikipedia.org/wiki/Activity_diagram)]</sub>


1. Explain how _Law of Demeter_ affects coupling<br>
   a. Add a line to this code that violates LoD
   ```java
   void foo(P p){
       //...
   }   
   ```
1. distinguish between _libraries_, _frameworks_, _platforms_<br>
   a. give examples of each used in AB4


{% from "schedule/index.md" import all_outcomes with context %}
{% from "common/tutorial.njk" import  show_week_evidences with context %}
{{ show_week_evidences("10", all_outcomes) }}