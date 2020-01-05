{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-grading") %}
<div id="main">

Note that project grading is ==not competitive (not bell curved)==. {{ module }}T projects will be assessed separately from {{ module }} projects. Given below is the marking scheme.

**Total**: 45 marks ({{ icon_individual }} 35 individual marks + {{ icon_team }} 10 team marks)

See the sections below for details of how we assess each aspect.

<!-- -------------------------------------------------------------------------------------------------------------- -->
<div id="criteria-productDesign">

#### <div class="bg-warning p-1">1. Project Grading: Product Design %%[{{ icon_team }}/{{ icon_individual }} 5 marks]%%</div>

**Evaluates:** how well your features fit together to form a cohesive product (not how many features or how big the features are) and how well does it match the target user

**Evaluated by:**
* tutors (based on product demo and user guide)
* peers from other teams (based on peer testing and user guide)

{{ embed_topic("tp-deliverables-pe.mbdf#projectGrading-featureFit-instructions", "Admin " + icon_embedding + " tP Deliverables → PE → ==Grading Instructions for Product Design==", "3") }}

In addition, feature flaws reported in the PE will be considered when grading this aspect.

<box>
<include src="tp-grading-bugs.mbdf#featureFlaws" />
</box>
</div>

<!-- -------------------------------------------------------------------------------------------------------------- -->

#### <div class="bg-warning p-1">2. Project Grading: Implementation %%[{{ icon_individual }} 10 marks]%%</div>

**<big>2A. Code quality</big>**

**Evaluates:** the quality of the parts of the code you claim as written by you

**Evaluation method:** manual inspection by tutors + automated-analysis by a script

**Criteria:**

<span id="projectGrading-codeQuality-criteria">

* At least some evidence of these (see [here]({{baseUrl}}/se-book-adapted/chapters/errorHandling.html) for more info)
  * logging
  * exceptions
  * assertions
  * defensive coding

* No [coding standard]({{java_coding_standard}}) violations %%e.g. all boolean variables/methods sounds like booleans%%. Checkstyle can prevent only _some_ coding standard violations; others need to be checked manually.

* [SLAP]({{baseUrl}}/se-book-adapted/chapters/codeQuality.html#slap-hard) is applied at a reasonable level. Long methods or deeply-nested code are symptoms of low-SLAP.

* No noticeable code duplications %%i.e. if there multiple blocks of code that vary only in minor ways, try to extract out similarities into one place%%, especially in test code.

* Evidence of applying [code quality guidelines covered in the module](../book/codeQuality/).

</span>

**<big>2B. Effort</big>**

**Evaluates:** how much value you contributed to the product

**Method:**

* Step 1: Evaluate the effort for the entire project. This is evaluated by peers who tested your product, and tutors.

{{ embed_topic("tp-deliverables-pe.mbdf#projectGrading-effort-instructions", "Admin " + icon_embedding + " tP Deliverables → PE → ==Questions used for Implementation Effort==", "3", indent="2") }}

* Step 2: Evaluate how much of that effort can be attributed to you. This is evaluated by team members, and tutors.

{{ embed_topic("peerEvaluations-midterm.mbdf#teamMemberEvaluation-implementation", "Admin " + icon_embedding + " Peer Evaluations → ==Questions used for Evaluating Implementation Effort==", "3", indent="2") }}

<!-- -------------------------------------------------------------------------------------------------------------- -->

#### <div class="bg-warning p-1">3. Project Grading: QA %%[{{ icon_individual }} 10 marks]%%</div>


<big>**3A. Developer Testing:**</big>

**Evaluates:** How well you tested your own feature

**Based on:**
1. functionality bugs in your work found by others during the [Practical Exam (PE)]({{baseUrl}}/admin/tp-deliverables.html#deliverable-practical-exam)
1. your test code %%(note <trigger trigger="click" for="modal:projectGradingQA-testingExpectations">our expectations for automated testing</trigger>)%%

<modal large title="Our expectations for automated testing in the project" id="modal:projectGradingQA-testingExpectations">
  <include src="tp-expectations.md#testing-expectations"/>
</modal>

<box>
<include src="tp-grading-bugs.mbdf#functionalityBugs" />
</box>


<big>**3B. System/Acceptance Testing:**</big>

**Evaluates:** How well you can system-test/acceptance-test a product

**Based on:** bugs you found in the PE. In addition to functionality bugs, you get credit for reporting documentation bugs and feature flaws.

<box>
<include src="tp-grading-bugs.mbdf#bugCalculationNotes" />
</box>

<!-- -------------------------------------------------------------------------------------------------------------- -->
<div id="criteria-documentation">

#### <div class="bg-warning p-1">4. Project Grading: Documentation %%[{{ icon_individual }} 10 marks]%%</div>

**Evaluates:** your contribution to project documents

**Method:** Evaluated in two steps.

* Step 1: Evaluate the whole UG and DG. This is evaluated by peers who tested your product, and tutors.

{{ embed_topic("tp-deliverables-pe.mbdf#projectGrading-userGuide-instructions", "Admin " + icon_embedding + " tP Deliverables → PE → ==Grading Instructions for User Guide==", "3", indent="2") }}
{{ embed_topic("tp-deliverables-pe.mbdf#projectGrading-devGuide-instructions", "Admin " + icon_embedding + " tP Deliverables → PE → ==Grading Instructions for Developer Guide==", "3", indent="2") }}

* Step 2: Evaluate how much of that effort can be attributed to you. This is evaluated by team members, and tutors.

{{ embed_topic("peerEvaluations-midterm.mbdf#teamMemberEvaluation-ug", "Admin " + icon_embedding + " Peer Evaluations → ==Questions used for Evaluating the Contribution to the UG==", "3", indent="2") }}
{{ embed_topic("peerEvaluations-midterm.mbdf#teamMemberEvaluation-dg", "Admin " + icon_embedding + " Peer Evaluations → ==Questions used for Evaluating the Contribution to the DG==", "3", indent="2") }}

* In addition, UG and DG bugs you received in the PE will be considered for grading this component.

<div class="indented-level2">

<box>
<include src="tp-grading-bugs.mbdf#ugBugs" />
</box>

<box>
<include src="tp-grading-bugs.mbdf#dgBugs" />
</box>
</div>

</div>
<!-- -------------------------------------------------------------------------------------------------------------- -->

#### <div class="bg-warning p-1">5. Project Grading: Project Management %%[{{ icon_team }} 5 + {{ icon_individual }} 5 = 10 marks]%%</div>

<div id="project-management-grading"> 

<big>**5A. Process:**</big>

**Evaluates:** How well you did in project management related aspects of the project, as an individual and as a team

**Based on:** tutor/bot observations of project milestones and GitHub data

**Grading criteria:**

* Milestones ==need to be reached the midnight before of the tutorial== for it to be counted as achieved. ==To get a good grade for this aspect, achieve at least 60% of the recommended milestone progress.==
* Good use of GitHub milestones
* Good use of GitHub release mechanism
* Good version control, based on the repo
* Reasonable attempt to use the forking workflow
* Good task definition, assignment and tracking, based on the issue tracker
* Good use of buffers %%(opposite: everything at the last minute)%%
* Project done iteratively and incrementally %%(opposite: doing most of the work in one big burst)%%


<big>**5B. Team-tasks:**</big>

**Evaluates:** How much you contributed to team-tasks

{{ embed_topic("tp-expectations.md#example-team-tasks", "Admin " + icon_embedding + " tP → Expectations: Examples of team-tasks", "3", indent="1") }}

**Based on:** peer evaluations, tutor observations

**Grading criteria:** To earn full marks, you should have done close to a fair share of the team tasks. You can earn bonus marks by doing more than your fair share.


</div>

</div>

{% endcall %}
