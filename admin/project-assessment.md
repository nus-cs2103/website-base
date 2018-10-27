{% macro show_main_text() %}
<div id="main">

Note that project grading is ==not competitive (not bell curved)==. {{ module }}T projects will be assessed separately from {{ module }} projects. This is to account for the perceived difference in workload. Given below is the marking scheme.

**Total**: 50 marks ({{ icon_individual }} 40 individual marks + {{ icon_team }} 10 team marks)

<panel header="1. **Product features** %%[{{ icon_team }} 5 marks]%%" expanded>

Evaluates: How well do your features fit together to form a cohesive product (not how many features or how big the features are)?

Based on: user guide and the product demo. The **quality of the demo will be factored in** as well.

:bulb: Feature that fit well with the other features will earn more marks.

</panel>

<panel header="2. **Implementation** %%[{{ icon_individual }} 15 marks]%%" expanded>

Evaluates: 

**A. Code quality/quantity:** 

How good your implementation is, in terms of the quality and the quantity of the code you have written yourself.

Based on: an inspection of the parts of the code you claim as written by you.

<panel header=":bulb: Tips: how to score high for code quality" no-close>

<span id="code-quality-tips">

* Ensure your code has at least some evidence of these (see [here]({{baseUrl}}/se-book-adapted/chapters/errorHandling.html) for more info)
  * logging
  * exceptions
  * assertions
  * defensive coding
  
* Ensure there are no [coding standard]({{java_coding_standard}}) violations %%&nbsp;e.g. all boolean variables/methods sounds like booleans%%. Checkstyle can prevent only _some_ coding standard violations; others need to be checked manually.

* Ensure [SLAP]({{baseUrl}}/se-book-adapted/chapters/codeQuality.html#slap-hard) is applied at a reasonable level. Long methods or deeply-nested code are symptoms of low-SLAP may be counted against your code quality.

* Reduce code duplications %%&nbsp;i.e. if there multiple blocks of code that vary only in minor ways, try to extract out similarities into one place%%, especially in test code. 

* In addition, try to apply as many of the <trigger trigger="click" for="modal:v15-codeQuality">code quality guidelines covered in the module</trigger> as much as you can.


<modal large title="Textbook {{ icon_embedding }} Implementation →" id="modal:v15-codeQuality">
  <include src="../book/codeQuality/container-inElsewhere-asFlat.md" boilerplate />
</modal>

</span>

</panel><p>


**B. Depth and completeness of your feature**

</panel>

<panel header="3. **QA** %%[{{ icon_individual }} 10 marks]%%" expanded>

Evaluates: How good is your Quality Assurance? 

Based on: 1. your test code 2. our own manual testing 3. your performance in the v1.4 [Practical Exam]({{baseUrl}}/admin/index-flat.html#deliverable-practical-exam), 4. bugs found during PE.

{{ embed_topic("project-deliverables.md#project-deliverables-practicalexam", "Admin " + icon_embedding + " Deliverables → Practical Exam", "projectAssessment-Pe", "3") }}
<panel type="seamless" header="Expectations for writing automated tests:" expanded>
  <include src="project-testing.mbdf#expectations"/>
</panel>
  
</panel>

<panel header="4. **Documentation** %%[{{ icon_individual }} 10 marks]%%" expanded>

Evaluates: How well does your user guide achieves its objectives? 

Based on: the relevant sections of your project portfolio. Criteria considered:
* Explanation should be clear and written to match the audience.
* Good use of visuals to complement text.
    
</panel>
  
<panel header="5. **Project management** %%[{{ icon_team }} 5 + {{ icon_individual }} 5 = 10 marks]%%" expanded>
<div id="project-management-grading"> 

**A. Process:** 

Evaluates: How well you did in project management related aspects of the project, as an individual and as a team 

Based on: Supervisor observations of project milestones and GitHub data. 
 
Milestones ==need to be reached the midnight before of the tutorial== for it to be counted as achieved. To get a good grade for this aspect, achieve recommended weekly progress in at least 6/10 weeks.
  
Other criteria:
* Good use of GitHub milestones
* Good use of GitHub release mechanism
* Good version control, based on the repo
* Reasonable attempt to use the forking workflow
* Good task definition, assignment and tracking, based on the issue tracker
* Good use of buffers %%(opposite: everything at the last minute)%%
* Project done iteratively and incrementally %%(opposite: doing most of the work in one big burst)%% 

**B. Team-based tasks**: 

  Evaluates: how much you contributed to common <span class="embedding">team-based tasks</span><span class="flat">[team-based tasks]({{baseUrl}}/admin/index-flat.html#scope-example-team-tasks)</span>

Based on: peer evaluations and tutor observations

{{ embed_topic("project-scope.md#example-team-tasks", "Admin " + icon_embedding + " Project Scope → Examples of team tasks", "projectAssessment-exmapleTeamTasks", "3") }}

</div>
</panel>
<p/>

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-assessment", show_main_text) }}
