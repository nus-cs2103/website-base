{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(9, "tutorial") }}

**Questions to discuss during tutorial:**

<div class="indented">
  <include src="../../book/modeling/modelingStructures/objectOrientedDomainModels/q-courseDomainModel.md" />
</div>
<br>

**Q1**
1. What is _Liskov Substitution Principle_?<br>
   Give an example from the project where LSP is followed and explain how to change the code to break LSP.

**Q2**
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

**Q3**
1. How does an _OO Domain Model_ differ from a class diagram?
1. What's the relationship between an OODM and a class diagram for a software? %%e.g., exactly the same?, one is a sub-set of the other?%%
1. Which diagram can we use to show ~~class~~object structures in a problem domain?
