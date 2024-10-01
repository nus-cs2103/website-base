{% from "common/macros.njk" import embed_topic, show_faq with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-expectations") %}
<div id="main">

<span class="keyword d-none">project expectations</span>

<!-- ==================================================================================================== -->
<div id="functionalityExpectations">

<h2 class="text-white bg-danger p-1">Functionality Expectations</h2>

<div tags="m--cs2103" id="functionality-expectations">

**The expected level of _functionality_ is what you could achieve if each member puts in about ==50% of the implementation effort they put into the iP==** (reason for setting it much less than 100%: even after adding the extra overheads of doing the project as a team, and working with an exising codebase, we don't want the tP to take more effort than the iP).<br>
Furthermore, we estimate that the above-mentioned bar is roughly _equivalent_ to **writing about 300-400 lines of functional code** (excluding testing and documentation) per person.

<box type="important" seamless>

  In case you happen to look at tP's of past batches (2023 and before) in order to gauge the required effort, note that the above reflects a ==drastically lower bar from those semesters==. For reference, the bar given to previous batches was 'same as iP effort' (not half), and the median LoC of functional code written by a student was about 850 LoC.
</box>
</div>
<div tags="m--cs2113">

**The expected level of _functionality_ from a team is roughly ==what you can achieve if each member contributes about the same amount of functional code as required by a <tooltip content="i.e., if all requirements were met at the _minimal_ level specified">typical iP</tooltip>==**.
</div>

==There are no extra marks for exceeding implementation _effort_ bar== stated above. Hence, _effort_ is graded on mostly an S/U basis) -- it is the _quality_ of the code that really determines the marks for _implementation_ component (more info <trigger trigger="click" for="modal:tPexpectations-implementationGrading">here</trigger>).  Try to avoid adding more features than necessary, unless you are doing it out of interest; you are better off spending more effort in improving other aspects of the project instead. As mentioned elsewhere, a functionality just the right size and of high quality will earn more marks than a functionality that is bigger (or more difficult, or more interesting/novel) but of lower quality.

<div tags="m--cs2103">

{{ show_faq("tpEnoughFeatures") }}
{{ show_faq("tpMustWrite300Loc") }}
{{ show_faq("tpFullMarksFor300Loc") }}
<p/>
</div>

<modal large header="tP: Grading [extract] → " id="modal:tPexpectations-implementationGrading">
  <include src="tp-grading.md#grading-implementation"/>
</modal>

<box type="important" tags="m--cs2113" seamless>

In the most recent semester, more than 80% of the students did significantly more work than what was needed to earn full marks for effort. Many of them were likely under the wrong impression that doing more features will earn them more marks. Try to avoid doing the same mistake yourself.

In fact, here is the grading criterion for the individual project effort:
{{ embed_topic("tp-pe-fragment.md#projectGrading-effort-instructions", "Admin " + icon_embedding + " tP → PE → ==Evaluating the  Implementation Effort==", "3") }}
</box>

<box tags="m--cs2103">

{{ icon_tip }} If you wish to add the following features to your app, we recommend (but not require) you to follow similar features in AB4 (not AB3) in order to reduce the effort required.
  * [Undo/redo](https://se-education.org/addressbook-level4/DeveloperGuide.html#undo-redo-feature)
  * [Automated GUI tests](https://se-education.org/addressbook-level4/Testing.html#types-of-tests)
</box>

</div>
<!-- ==================================================================================================== -->
<div id="teamExpectations">

<h2 class="text-white bg-success p-1">{{ icon_team }} Team Expectations</h2>

* <span class="badge bg-success">Expectation</span> <span class="text-success">**Produce a _cohesive_ product:**</span> i.e. ensure,
  1. features fit together to form a cohesive product,
  1. documentation follows a consistent style and presents a cohesive picture to the reader{% if cs2113 %}, and
  1. final project demo presents a cohesive picture to the audience.{% endif %}
* <span class="badge bg-success">Expectation</span> <span class="text-success">**Maintain product integrity/quality:**</span> i.e. prevent breaking other parts of the product as it evolves. <span tags="m--cs2103 m--cs2113">
* <span class="badge bg-success">Expectation</span> <span class="text-success">**Manage the project:**</span> i.e. ensure workflow, code maintenance, integration, releases, etc. are done properly.
</span>

</div>
<!-- ==================================================================================================== -->
<div id="individualExpectations">

<h2 class="text-white bg-info p-1">{{ icon_individual }} Individual Expectations</h2>

#### <span class="badge bg-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Implementation</span>

* <span class="badge bg-info">Expectation</span> <span class="text-info">**Contribute to the functional code of the product.**</span>
  * User-visible features are preferred, but it is not a strict requirement.:
  * **The enhancement(s) should fit with the rest of the software** (and the target user profile) and should have the consent of the team members. %%You will lose marks if you go 'rogue' and add things that don't fit with the product.%%

<div tags="m--cs2103" class="indented-level2">

<panel type="seamless" header="Some example enhancements" >

  * Add a new feature %%e.g. add the ability to view statistics%%
  * Tweak an existing features %%e.g. make the command syntax more user-friendly and closer to natural language%%
  * A redesign of the GUI %%e.g. make it work like a chat application (note: chat is a form of CLI)%%
  * A redesign of the code %%e.g. Improve the design to improve the code quality.%%

</panel><p/>
</div>

* **Recommended: Contribute to _all_ aspects of the project** e.g. write back-end code, front-end code, test code, user documentation, and developer documentation. %%Reason: If you limit yourself to certain aspects only, you could lose marks allocated for the aspects you did not do. In addition, the final exam assumes that you are familiar with all aspects of the project.%%

* **Recommended: Do _all_ the work related to your enhancement yourself.** %%Reason: If there is no clear division of who did which enhancement, it will be difficult to divide project credit (or assign responsibility for bugs detected by testers) later.%%<br>
  In other words, ==we recommend that the work to be divided primarily based on _features/enhancements_== rather than _components_. The latter has the risk of a team member becoming a _single point of failure_ and you becoming _too reliant_ on other team members %%e.g., what if the person assigned to an important component doesn't deliver on time?%%.

<div tags="m--cs2103">

* **Recommended: Divide the components of the product among team members**. Notwithstanding the above, you are still recommended to divide the components of the product among team members so that each team member is _in charge_ of one or more components. While others will be modifying those components to fit their features, your role as the _in charge_ of a component is to guide others modifying that component %%(reason: you are supposed to be the most knowledgeable about that component)%% and protect that component from degrading %%e.g., you can review others' changes to your component and suggest possible changes%%.
</div>


#### <span class="badge bg-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Documentation</span>

* **Objective:** showcase your ability to write both _user-facing documentation_ and _developer-facing documentation_.
* <span class="badge bg-info">Expectation</span> <span class="text-info">**Update the User Guide (UG) and the Developer Guide (DG) parts**</span> that are related to the enhancements you added.
* **Optional: If the UG/DG updates for your enhancements are not enough to reach the above requirements**, you can make up the shortfall by documenting 'proposed' features and alternative designs/implementations.{% if cs2113 %}
* <span class="badge bg-info">Expectation</span> <span class="text-info">**Use at least {{ uml_diagrams_per_person }} UML diagrams in your DG updates**</span> i.e., diagrams you added yourself or those you modified significantly.{% endif %}

#### <span class="badge bg-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Testing</span>

<div id="testing-expectations">

* <span class="badge bg-info">Expectation</span> <span class="text-info">**Write _some_ automated tests**</span> so that there is evidence that you _can_ write automated tests.

<div class="indented-level2">

<box>

**:thinking: How much testing is enough?** We expect you to decide. As you learn different types of testing and what they try to achieve, you should decide how much of each type is worth having. Similarly, you can decide to what extent you want to automate tests, depending on the benefits and the effort required.<br>
There is no requirement for a minimum test coverage level. Note that in a high-end production environment you might be required to have high levels of test coverage (e.g., 90%). In this project, it can be less. ==Caveat: The weaker your tests are, the higher the risk of undetected bugs/regressions, which will cost you marks if not detected/fixed before the final submission.==
</box>
</div>

</div>

#### <span class="badge bg-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Teamwork</span>

* <span class="badge bg-info">Expectation</span> <span class="text-info">**Do a non-trivial share of the _team-tasks_**.</span>

<div id="team-tasks" class="indented-level2">

<box>

_Team-tasks_ are the tasks that _someone_ in the team has to do.

<panel type="seamless" header="{{ icon_example }} Examples of team-tasks">

<span id="example-team-tasks">

Here is a non-exhaustive list of team-tasks:

1. Setting up the GitHub team org/repo
1. Necessary general code enhancements{% if cs2103 %} e.g.,
   1. Work related to renaming the product
   1. Work related to changing the product icon{% endif %}
1. Setting up tools e.g., GitHub, Gradle
1. Maintaining the issue tracker
1. Release management
1. Updating user/developer docs that are not specific to a feature %%e.g. documenting the target user profile%%
1. Incorporating more useful tools/libraries/frameworks into the product or the project workflow %%(e.g. automate more aspects of the project workflow using a GitHub plugin)%%

</span>
</panel><p/>
</box>
</div>

* <span class="badge bg-info">Expectation</span> <span class="text-info">**Carry a non-trivial share of project roles and responsibilities**.</span>

<div class="indented-level2">

<box>
<span id="roles">

_Roles_ indicate aspects you are in charge of and responsible for. %%E.g., if you are in charge of documentation, you are the person who should allocate which parts of the documentation is to be done by whom, ensure the document is in right format, ensure consistency etc.%%

<panel type="seamless" header="{{ icon_example }} Example roles and responsibilities">

This is a non-exhaustive list; you may define additional roles.

* _Team lead_: Responsible for overall project coordination.
* _Documentation_ (short for ‘in charge of documentation’): Responsible for the quality of various project documents.
* _Testing_: Ensures the testing of the project is done properly and on time.
* _Code quality_: Looks after code quality, ensures adherence to coding standards, etc.
* _Deliverables and deadlines_: Ensure project deliverables are done on time and in the right format.
* _Integration_: In charge of versioning of the code, maintaining the code repository, integrating various parts of the software to create a whole.
* _Scheduling and tracking_: In charge of defining, assigning, and tracking project tasks.
* _[Tool ABC] expert_: %%e.g. IntelliJ expert, Git expert, etc.%% Helps other team member with matters related to the specific tool.

<div tags="m--cs2103">

* _In charge of [Component XYZ]_: %%e.g. In charge of `Model`, `UI`, `Storage`, etc.%% Note that being _in charge_ of a component doesn't mean you are the only one who should be modifying that component. Rather, you are the one who's expected to, know that component best, review changes done to that component in {{ version_penultimate }}-{{ version_final }}, act as the gate keeper of its quality, help others when they face difficulties while modifying that component etc.
</div>
<div tags="m--cs2113">

* _In charge of[Area XYZ]_ of the code: %%e.g. In charge of the code that deals with storage, etc.%% If you are in charge of an area, you are expected to know that area well, and review changes done to that code.
</div>
</panel><p/>

{{ icon_tip }} Ensure each of the important roles are assigned to one person in the team. It is OK to have a 'backup' for each role, but **for each aspect there should be one person who is unequivocally the person responsible for it**. %%Reason: when _everyone is responsible for everything_, no one is.%%
</span>
</box>
</div>

* <span class="badge bg-info">Expectation</span> <span class="text-info">**Review each others work**.</span> %%Reason: reviewing skills is a learning outcome, and it is mutually beneficial.%%

</div>
<!-- ==================================================================================================== -->

</div>
{% endcall %}
