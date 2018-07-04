<div id="1kloc">

{{ icon_important_big_red }} This is a compulsory LO. If you miss this LO, your participation marks will be affected. However, you can make up for missing this LO by doing double work for the following LO **(in Week 5)**:

<panel header="[For Reference] details of the Week 5 LO mentioned above">

{{evidence}}

<include src="project.md#2kloc"/>

</panel>

{{ dashed_line | safe}}

{{evidence}}

**Acceptable**: Evidence that you have worked with a code base larger than 1KLoC. %%e.g. a project in a previous module or a pet project%%

**Suggested**: Do an enhancement to [[AddressBook - Level1]({{module_org}}/addressbook-level1)]  %%e.g. add a new command%%

* The size of the enhancement does not matter.
* Change the code in small steps and commit after each significant change.
* Remember to update all relevant documentation and tests.
* Try to follow the coding standard in your new code.
* Try to stay within the procedural (not OOP) style of the code base.
* [Optional] Fork address [AddressBook - Level1]({{module_org}}/addressbook-level1) to your GitHub account and push your changes to your fork.

  <tip-box type="tip">
  
  Note that you can reuse the code you write here in your final project, if applicable.
 
  </tip-box>

**Submission**: demo during tutorial.

</div>


<div id="2kloc">

<tip-box type="important"> 
  This LO requires coordination and cooperation among team members. It also requires a few days to complete; we recommend that you start it early in the week rather than just before the tutorial day.
</tip-box>

:bulb: **Those who failed to produce working code at 1KLoC milestone** (in week 3) can recover the lost marks by doing _two_ enhancements at this milestone.

:bulb: When working with existing code, a safe approach is to **change the code in very small steps, each resulting in a verifiable change** without breaking the app. For example, when adding a new `sort` command, the first few steps can be,
1. Teach the app to accept a `sort` command but ignore it.
2. Next, teach the app to direct the `sort` command to an existing command e.g. `sort` command simply invokes the `list` command internally.
3. Add a `SortCommand` class but make it simply a copy of the the existing `ListCommand`. Direct the `sort` command to the new `SortCommand`.
4. ...

:bulb: Note that you can reuse the code you write here in your final project, if applicable.
 

#### Individual component:

**You can omit this individual component if** you have worked with a code base that meets the following criteria:
* more than 2KLoC of the code base was written by other developers
* your code included automated tests
* your code was contributed via a proper revision control workflow e.g. pull requests

**Requirements**: Do an enhancement to [[AddressBook - Level2]({{module_org}}/addressbook-level2)]  %%e.g. add a new command%%. It can be the same enhancement you did to AddressBook Level1 (at the 1KLoC milestone in week 3). The size of the enhancement does not matter but you must,
* update the User Guide
* update existing tests and add new tests if necessary, for both JUnit tests and I/O tests
* follow the coding standard
* follow the OOP style

Optional but encouraged:
* Update the Developer Guide

<include src="project.md#submission_PR_optional" />

#### Team component:

The team component is ==to be done by all members==, including those who were allowed to omit the individual component.

* Review PRs created by team members in the _Individual Component_ above %%i.e. add review comments in the PR created against module repo%%. You can either give suggestions to improve, or ask questions to understand, the code written by the team member. 

* **Requirements**: Try to ensure that each PR reviewed by _at least_ one team member and each team member's PR is reviewed by at least one other team member.  

* **Submission**: Just update PR created in the individual component by adding comments/commits to it.

</div>


<div id="submission_PR_optional">

**Submission**: 
* Options 1 (discouraged): Show the relevant code during the tutorial.
* Options 2 (preferred): Create a pull request by following the instructions below.

<include src="../../admin/appendixE-gitHub.md#tutorial-pr-instructions" name="%%Admin {{ icon_embedding }} Appendix E: Using GitHub Project Hosting → Submitting Pull Requests as evidence of an LO%%" dynamic />

If you choose option 2, we recommend that you complete this week's _Project Management_ LOs first; there are many ways to create PRs but we expect you to create PRs in a specific way, as specified in the LOs. 

</div>


<div id="PR_to_AB2">

**Submission**: Create a PR against [Addressbook-Level2]({{module_org}}/addressbook-level2).  ==Only clean PRs== (i.e. free of unrelated code modifications) will be accepted. 

<include src="../../admin/appendixE-gitHub.md#tutorial-pr-instructions" name="%%Admin {{ icon_embedding }} Appendix E: Using GitHub Project Hosting → Submitting Pull Requests as evidence of an LO%%" dynamic />

</div>


<div id="PR_to_AB3">

**Submission**: Create a PR against [Addressbook-Level3]({{module_org}}/addressbook-level3).  ==Remember to use phase B team ID== (e.g. _W09-==B==2_) in your PR name. 

<include src="../../admin/appendixE-gitHub.md#tutorial-pr-instructions" name="%%Admin {{ icon_embedding }} Appendix E: Using GitHub Project Hosting → Submitting Pull Requests as evidence of an LO%%" dynamic />

</div>


<div id="requirements">

Covered by the 'Documentation' component of v1.1:

<dynamic-panel src="../../admin/project-w07-v11.md#main" header="%%Admin {{ icon_embedding }} Project → v1.1%%" no-close />

</div>


<div id="local_impact_changes">

Covered by the 'Product' component of v1.1:

<dynamic-panel src="../../admin/project-w07-v11.md#main" header="%%Admin {{ icon_embedding }} Project → v1.1%%" no-close />

</div>


<div id="product_design">

No textbook section. To be covered during the lecture.

{{ evidence }}

Apply the discussed guidelines when designing the product (covered by v1.1 deliverables).

</div>


<div id="user_guide">

Covered by the 'Documentation' of component v1.1:

<dynamic-panel src="../../admin/project-w08-mid-v12.md#main" header="%%Admin {{ icon_embedding }} Project → mid-v1.2%%" no-close />

</div>


<div id="global_impact_change">

Covered by the 'Product' component of mid-v1.2:

<dynamic-panel src="../../admin/project-w08-mid-v12.md#main" header="%%Admin {{ icon_embedding }} Project → mid-v1.2%%" no-close />

</div>


<div id="dev_guide">

Covered by 'Documentation' component of v1.2:

<include src="../../admin/project-w09-v12.md#main" name="%%Admin {{ icon_embedding }} Project → v1.2%%" dynamic />

</div>


<div id="track_progress">

Covered by the 'Project Management' component of v1.2:

<include src="../../admin/project-w09-v12.md#main" name="%%Admin {{ icon_embedding }} Project → v1.2%%" dynamic />

</div>


<div id="release_produt">

Covered by v1.3:

<include src="../../admin/project-w10-mid-v13.md#main" name="%%Admin {{ icon_embedding }} Project → v1.3%%" dynamic no-close/>

</div>


<div id="acceptance_testing">


Covered by the 'Acceptance Testing' component of v1.4:

<include src="../../admin/project-w11-v13.md#main" name="%%Admin {{ icon_embedding }} Project → v1.4%%" dynamic />

</div>


<div id="relate_process">

Relate this model and some of its practices to the project. %%&nbsp;e.g. Are you doing something similar? Will it help if you adopt those practices? If they are not applicable, why?%%

</div>


<div id="describe_contribution">

Covered by the 'Project Portfolio Page' component of mid-v1.4:

<include src="../../admin/project-w12-mid-v14.md#main" name="%%Admin {{ icon_embedding }} Project → mid-v1.4%%" dynamic />

</div>


<div id="demo">

Covered by the 'Demo' component of v1.4:

<include src="../../admin/project-w13-v14.md#main" name="%%Admin {{ icon_embedding }} Project → v1.4%%" dynamic />

</div>


<div id="iterative_delivery">

Covered by v1.0-v1.4:

</div>


<div id="brownfield">

Covered by v1.0-v1.4:

</div>


<div id="evaluate_peers">

Covered by the 'Peer Evaluations' component of the module:

<include src="../../admin/peer-evaluations.md#main" name="%%Admin {{ icon_embedding }} Peer Evaluations%%" dynamic />

Also covered by the 'Practical Exam' of v1.4:

<include src="../../admin/project-w13-v14.md#main" name="%%Admin {{ icon_embedding }} Project → v1.4%%" dynamic />

</div>