{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-grading") %}
<div id="main">

Note that project grading is ==not competitive (not bell curved)==.<span tags="m--cs2113 m--cs2103">
{{ course }}T projects will be assessed separately from {{ course }} projects.</span> Given below is the marking scheme.

****Total****: {{ marks_tp }} marks ({{ icon_individual }} {{ marks_tp_individual }} individual marks + {{ icon_team }} {{ marks_tp_team }} team marks)

See the sections below for details of how we assess each aspect.

<!-- -------------------------------------------------------------------------------------------------------------- -->
<div id="criteria-productDesign">

#### <div class="bg-warning text-dark p-1">1. Project Grading: Product Design %%[{{ icon_individual }} {{ marks_tp_design }} marks]%%</div>

**Evaluates:**
* how well your features _fit together_ to form a cohesive product<br>
  (not how many features or how big/novel/interesting/difficult the features are)
* how well it _matches the target user_

<div tags="m--cs2113 m--cs2103">

**Evaluated by:**
* the teaching team (based on product demo and user guide)
* peers from other teams (based on peer testing and user guide)

{{ embed_topic("tp-pe-fragment.md#projectGrading-featureFit-instructions", "Admin " + icon_embedding + " tP → PE → ==Grading Instructions for Product Design==", "3") }}
<p/>

In addition, feature flaws reported in the PE will be considered when grading this aspect.

<box tags="m--cs2113" type="tip">

Note that 'product design' or 'functionality' are not critical learning outcomes of the tP. Therefore, ==the bar you need to reach to get full marks will be quite low==. For example, the `Medium` level in the rubric given in the panel above should be enough to achieve full marks. Similarly, only cases of _excessive_ 'feature flaw' bugs will affect the score.
</box>

<box>
<include src="tp-grading-bugs-fragment.md#featureFlaws" />
</box>
</div>

</div>

<!-- -------------------------------------------------------------------------------------------------------------- -->
<div id="grading-implementation">

#### <div class="bg-warning text-dark p-1">2. Project Grading: Implementation %%[{{ icon_individual }} {{ marks_tp_implementation }} marks]%%</div>

**++2A. Code quality++**

**Evaluates:** the quality of the parts of the code you claim as written by you

**Evaluation method:** manual inspection by tutors + automated-analysis by a script

**Criteria:**

<span id="projectGrading-codeQuality-criteria">

* At least some evidence of these (see [here]({{baseUrl}}/se-book-adapted/chapters/errorHandling.html) for more info)
  * logging
  * exceptions
  * assertions{% if cs2103 %}
  * defensive coding{% endif %}

* No [coding standard]({{url_java_coding_standard}}) violations %%e.g., all boolean variables/methods sounds like booleans%%. Checkstyle can prevent only _some_ coding standard violations; others need to be checked manually.

* [SLAP]({{baseUrl}}/se-book-adapted/chapters/codeQuality.html#slap-hard) is applied at a reasonable level. Long methods or deeply-nested code are symptoms of low-SLAP.

* No noticeable code duplications %%i.e., if there multiple blocks of code that vary only in minor ways, try to extract out similarities into one place%%, especially in test code.

* Evidence of applying [code quality guidelines covered in the course](../book/codeQuality/).

</span>

**++2B. Effort++**

**Evaluates:** how much value you contributed to the product

**Evaluation method:**

<div tags="m--cs2103">

* Step 1: Evaluate the effort for the entire project. This is evaluated by peers who tested your product, and tutors.

{{ embed_topic("tp-pe-fragment.md#projectGrading-effort-instructions", "Admin " + icon_embedding + " tP → PE → ==Questions used for Implementation Effort==", "3", indent="2") }}

* Step 2: Evaluate how much of that effort can be attributed to you. This is evaluated by team members, and tutors.

{{ embed_topic("peerEvaluations-midterm-fragment.md#teamMemberEvaluation-implementation", "Admin " + icon_embedding + " Peer Evaluations → ==Questions used for Evaluating Implementation Effort==", "3", indent="2") }}

* Baseline: If your team received a value higher than `5` in step 1 and the team agrees that you did roughly an equal share of implementation work, you should receive full marks for effort.
</div>
<div tags="m--cs2113">

* This is evaluated by peers who tested your product, and tutors.

{{ embed_topic("tp-pe-fragment.md#projectGrading-effort-instructions", "Admin " + icon_embedding + " tP → PE → ==Question used for Implementation Effort==", "3", indent="2") }}

* The score could be further moderated by this question answered by team members.

{{ embed_topic("peerEvaluations-midterm-fragment.md#teamMemberEvaluation-implementation", "Admin " + icon_embedding + " Peer Evaluations → ==Questions used for Evaluating Implementation Effort==", "3", indent="2") }}

Note: Effort put into non-user-visible implementation work (e.g., major refactorings) can also be counted for this component of grading, but it is up to you to describe that work in your PPP so that evaluators can factor those in.

</div>

</div>
<!-- -------------------------------------------------------------------------------------------------------------- -->

#### <div class="bg-warning text-dark p-1">3. Project Grading: QA %%[{{ icon_individual }} {{ marks_tp_qa }} marks]%%</div>

<div tags="m--cs2113 m--cs2103">

++**3A. Developer Testing:**++

**Evaluates:** How well you tested your own feature

**Based on:**
1. functionality bugs in your work found by others during the [Practical Exam (PE)]({{baseUrl}}/admin/tp-pe.html#tp-practical-exam)
1. your test code %%(note <trigger trigger="click" for="modal:projectGradingQA-testingExpectations">our expectations for automated testing</trigger>)%%

<modal large header="Our expectations for automated testing in the project" id="modal:projectGradingQA-testingExpectations">
  <include src="tp-expectations.md#testing-expectations"/>
</modal>

<box>
<include src="tp-grading-bugs-fragment.md#functionalityBugs" />
</box>


++**3B. System/Acceptance Testing:**++

**Evaluates:** How well you can system-test/acceptance-test a product

**Based on:** bugs you found in the PE. In addition to functionality bugs, you get credit for reporting documentation bugs and feature flaws.

<box>
<include src="tp-grading-bugs-fragment.md#bugCalculationNotes" />
</box>
</div>

<!-- -------------------------------------------------------------------------------------------------------------- -->
<div id="criteria-documentation">

#### <div class="bg-warning text-dark p-1">4. Project Grading: Documentation %%[{{ icon_individual }} {{ marks_tp_documentation }} marks]%%</div>

<div tags="m--cs2113 m--cs2103">

**Evaluates:** your contribution to project documents

**Method:** Evaluated in two steps.

* Step 1: Evaluate the whole UG and DG. This is evaluated by peers who tested your product, and tutors.

{{ embed_topic("tp-pe-fragment.md#projectGrading-userGuide-instructions", "Admin " + icon_embedding + " tP → PE → ==Grading Instructions for User Guide==", "3", indent="2") }}
{{ embed_topic("tp-pe-fragment.md#projectGrading-devGuide-instructions", "Admin " + icon_embedding + " tP → PE → ==Grading Instructions for Developer Guide==", "3", indent="2") }}

* Step 2: Evaluate how much of that effort can be attributed to you. This is evaluated by team members, and tutors.

{{ embed_topic("peerEvaluations-midterm-fragment.md#teamMemberEvaluation-ug", "Admin " + icon_embedding + " Peer Evaluations → ==Questions used for Evaluating the Contribution to the UG==", "3", indent="2") }}
{{ embed_topic("peerEvaluations-midterm-fragment.md#teamMemberEvaluation-dg", "Admin " + icon_embedding + " Peer Evaluations → ==Questions used for Evaluating the Contribution to the DG==", "3", indent="2") }}

* In addition, UG and DG bugs you received in the PE will be considered for grading this component.

<div class="indented-level2">

<box>
<include src="tp-grading-bugs-fragment.md#ugBugs" />
</box>

<box>
<include src="tp-grading-bugs-fragment.md#dgBugs" />
</box>
</div>
</div>

</div>
<!-- -------------------------------------------------------------------------------------------------------------- -->

#### <div class="bg-warning text-dark p-1">5. Project Grading: Project Management %%[{{ icon_team }} {{ marks_tp_pm_team }} + {{ icon_individual }} {{ marks_tp_pm_individual }} = {{ marks_tp_pm }} marks]%%</div>

<div id="project-management-grading">

++**5A. Process:**++

**Evaluates:** How well you did in project management related aspects of the project, as an individual and as a team

**Based on:** tutor/grading-script observations of project milestones and GitHub data

**Grading criteria:**

* Project done iteratively and incrementally %%(opposite: doing most of the work in one big burst)%%

* Project tasks done on time (to get a good grade for this aspect, finish at least 75% of the tasks by the deadline).
* Good use of these GitHub mechanisms:
   * milestones
   * releases
   * issue tracker (with good task definition, assignment, and tracking)
   * PRs, and PR reviews
* Good version control, based on the repo.
* Reasonable attempt to use the prescribed workflows.
* Good use of buffers %%(opposite: everything at the last minute)%%.


++**5B. Team-tasks:**++

**Evaluates:** How much you contributed to team-tasks

{{ embed_topic("tp-expectations.md#example-team-tasks", "Admin " + icon_embedding + " tP → Expectations: Examples of team-tasks", "3", indent="1") }}

**Based on:** peer evaluations, tutor observations

**Grading criteria:** Do the following to get a good grade for this aspect:
* Do close to an equal share of the team tasks.
* Have commits in four of weeks 7, 8, 9, 10, 11, 12

</div>

</div>

{% endcall %}
