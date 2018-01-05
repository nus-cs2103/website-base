Note that project grading is ==not competitive (not bell curved)==. CS2103T projects will be assessed separately from CS2103 projects. This is to account for the perceived difference in workload. Given below is the marking scheme.

**Total**: 50 marks (:bust_in_silhouette: 40 individual marks + :busts_in_silhouette: 10 team marks)

<panel header="1. **Product features** [:busts_in_silhouette:][5 marks]" expanded>

Evaluates: How well do your features fit together to form a cohesive product (not how many features or how big the features are)?

Based on: user guide and the product demo. The **quality of the demo will be factored in** as well.

:exclamation: ‘Half-baked’ (i.e. not production quality) or 'ill-fitting' (feature does not go well with the other features) features will not earn marks at all. It may be better to remove such features before submission.

</panel>

<panel header="2. **Implementation** [:bust_in_silhouette:][15 marks]" expanded>

Evaluates: 

**A. Code quality/quantity:** 

How good your implementation is, in terms of the quality and the quantity of the code you have written yourself.

Based on: an inspection of the collated code (submitted in your `/collated/*.md` files).

<span id="code-quality-tips">

<panel header=":bulb: Tips: how to score high for code quality" no-close>

* Ensure your code has at least some evidence of these (see [here](../book/errorHandling/index.html) for more info)
  * logging
  * exceptions
  * assertions
  * defensive coding
  
* Ensure there are no [coding standard](https://oss-generic.github.io/process/codingStandards/CodingStandard-Java.html) violations %%&nbsp;e.g. all boolean variables/methods sounds like booleans%%. Checkstyle can prevent only _some_ coding standard violations; others need to be checked manually.

* Ensure [SLAP](../book/codeQuality/maximiseReadability/intermediate/index.html) is applied at a reasonable level. Long methods or deeply-nested code are symptoms of low-SLAP may be counted against your code quality.

* Reduce code duplications %%&nbsp;i.e. if there multiple blocks of code that vary only in minor ways, try to extract out similarities into one place%%, especially in test code. 

* In addition, tyr to apply as many of the <trigger trigger="click" for="modal:v15-codeQuality">code quality guidelines covered in the module</trigger> as much as you can.

</panel><p>

</span>

**B. Depth and completeness of the major feature**

</panel>

<panel header="3. **QA** [:bust_in_silhouette:][10 marks]" expanded>

Evaluates: How good is your Quality Assurance? 

Based on: 1. your test code 2. our own manual testing 3. your performance in the v1.5 Practical Exam, 4. bugs found during PE. 

<panel type="seamless" header="%%Click here for more info on v1.5 practical exam%%">
  <include src="project-v15.md#v15-practicalExam"/>
</panel>
<panel type="seamless" header="Expectations for writing automated tests:" expanded>
  <include src="project-testing.md#expectations"/>
</panel>
  
</panel>

<panel header="4. **Documentation** [:bust_in_silhouette:][10 marks]" expanded>

Evaluates: How well does your user guide achieves its objectives? 

Based on: the relevant sections of your project portfolio. Criteria considered:
* Explanation should be clear and written to match the audience.
* Good use of visuals to complement text.
    
</panel>
  
<panel header="5. **Project management** [:busts_in_silhouette: 5 + :bust_in_silhouette: 5 = 10 marks]" expanded>
<div id="project-management-grading"> 

**A. Process:** 

Evaluates: How well you did in project management related aspects of the project, as an individual and as a team 

Based on: Supervisor observations of weekly milestones and GitHub data. ==Marks will be deducted== if,
 * if you missed more than two individual milestones %%&nbsp;out of the six milestones v1.0 - v1.5rc%% (only the team member loses marks)
 * if your team missed more than two team milestones %%&nbsp;out of the six milestones v1.0 - v1.5rc%% (all team members lose marks)
 
Milestones ==need to be reached _before_ the start of the tutorial==. If you reach the milestone _during_ the tutorial, it will be considered as missed.
  
Other criteria:
* Good use of GitHub milestones
* Good use of GitHub release mechanism
* Good version control, based on the repo
* Reasonable attempt to use the forking workflow
* Good task definition, assignment and tracking, based on the issue tracker
* Good use of buffers %%(opposite: everything at the last minute)%%
* Project done iteratively and incrementally %%(opposite: doing most of the work in one big burst)%% 

**B. Team-based tasks**: 

Evaluates: how much you contributed to common team-based tasks

Based on: peer evaluations and tutor observations

<panel type="seamless" header="Admin » Project Scope → Examples of team tasks">
  <include src="project-scope.md#example-team-tasks"/>
</panel>

</div>
</panel>
<p/>
