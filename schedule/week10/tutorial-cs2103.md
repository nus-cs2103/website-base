**Questions to discuss during tutorial:**

Divide these questions among team members and get ready to answer them.

1. How does an _OO Domain Model_ differ from a class diagram?

1. Draw an OODM for the description below, about how modules work in a certain university:

   <box>

   A module has a name and a code. A module is taken by 10 or more students, and taught by one instructor. A module can have a number tasks which can be assignments or tests. Some assignments are compulsory. When a student attempts a task, a grade and an optional feedback is given.

   </box>

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


To be moved to T9

1. Explain how _Law of Demeter_ affects coupling<br>
   a. Add a line to this code that violates LoD
   ```java
   void foo(P p){
       //...
   }   
   ```

