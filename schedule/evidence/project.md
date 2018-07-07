<div id="1kloc">

{{ icon_important_big_red }} This LO can earn you <trigger trigger="click" for="modal:project1kloc-participation">1 participation mark</trigger>. 
 
<modal large title="%%Admin {{ icon_embedding }} Participation Marks%%" id="modal:project1kloc-participation">
  <include src="../../admin/participation.md#main"/>
</modal>

{{ dashed_line | safe}}

{{evidence}}

Do an enhancement to [[AddressBook - Level1]({{module_org}}/addressbook-level1)]  %%e.g. add a new command%%

* The size of the enhancement does not matter.
* Change the code in small steps and commit after each significant change.
* Try to stay within the procedural (not OOP) style of the code base. %%Reason: in this LO, we try to stretch ourselves to the limits of the procedural approach%%.
* Update all relevant tests.
* [Optional] Update all relevant documentation.
* [Optional] Try to follow [our coding standard]({{baseUrl}}/admin/programming-languages.html#java-coding-standard) in your new code.
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

This LO can earn you 2 participation marks, 1 mark for the individual component and 1 for the team component. You can omit either one of them.

:bulb: When working with existing code, a safe approach is to **change the code in very small steps, each resulting in a verifiable change** without breaking the app. For example, when adding a new `sort` command, the first few steps can be,
1. Teach the app to accept a `sort` command but ignore it.
2. Next, teach the app to direct the `sort` command to an existing command e.g. `sort` command simply invokes the `list` command internally.
3. Add a `SortCommand` class but make it simply a copy of the the existing `ListCommand`. Direct the `sort` command to the new `SortCommand`.
4. ...

:bulb: Note that you can reuse the code you write here in your final project, if applicable.
 

#### Individual component:

**Requirements**: Do an enhancement to [[AddressBook - Level2]({{module_org}}/addressbook-level2)]  %%e.g. add a new command%%. It can be the same enhancement you did to AddressBook Level1 (at the 1KLoC milestone in week 3). The size of the enhancement does not matter but you must,
* update the User Guide
* update existing tests and add new tests if necessary, for both JUnit tests and I/O tests
* follow the coding standard
* follow the OOP style

Optional but encouraged:
* Update the Developer Guide

<include src="project.md#submission_PR_optional" />

#### Team component:

The team component is ==to be done by all members==, including those who didn't do the individual component.

* Review PRs created by team members in the _Individual Component_ above %%i.e. add review comments in the PR created against module repo%%. You can either give suggestions to improve, or ask questions to understand, the code written by the team member. 

* **Requirements**: Try to ensure that each PR reviewed by _at least_ one team member and each team member's PR is reviewed by at least one other team member.  

* **Submission**: Just update PR created in the individual component by adding comments/commits to it.

</div>


<div id="submission_PR_optional">

**Submission**: 
* Options 1 (discouraged): Show the relevant code during the tutorial.
* Options 2 (preferred): Create a pull request by following the instructions below.

<panel src="../../admin/appendixE-gitHub.md#tutorial-pr-instructions" header="%%Admin {{ icon_embedding }} Appendix E: Using GitHub Project Hosting → Submitting Pull Requests as evidence of an LO%%" />

If you choose option 2, we recommend that you complete this week's _Project Management_ LOs first; there are many ways to create PRs but we expect you to create PRs in a specific way, as specified in the LOs. 

</div>


<div id="PR_to_AB2">

**Submission**: Create a PR against [Addressbook-Level2]({{module_org}}/addressbook-level2).  ==Only clean PRs== (i.e. free of unrelated code modifications) will be accepted. 

<panel src="../../admin/appendixE-gitHub.md#tutorial-pr-instructions" header="%%Admin {{ icon_embedding }} Appendix E: Using GitHub Project Hosting → Submitting Pull Requests as evidence of an LO%%" />

</div>


<div id="PR_to_AB3">

**Submission**: Create a PR against [Addressbook-Level3]({{module_org}}/addressbook-level3).  ==Remember to use team ID== (e.g. _W09-2_) in your PR name. 

<panel src="../../admin/appendixE-gitHub.md#tutorial-pr-instructions" header="%%Admin {{ icon_embedding }} Appendix E: Using GitHub Project Hosting → Submitting Pull Requests as evidence of an LO%%" />

</div>

<div id="inception">

Covered by:

<panel src="../../admin/project-w03-inception.md#main" header="%%Admin {{ icon_embedding }} Project → Inception%%" no-close />

</div>


<div id="mid-v10">

Covered by:

<panel src="../../admin/project-w04-mid-v10.md#main" header="%%Admin {{ icon_embedding }} Project → mid-v1.0%%" no-close />

</div>


<div id="v10">

Covered by:

<panel src="../../admin/project-w05-v10.md#main" header="%%Admin {{ icon_embedding }} Project → v1.0%%" no-close />

</div>


<div id="mid-v11">

Covered by:

<panel src="../../admin/project-w06-mid-v11.md#main" header="%%Admin {{ icon_embedding }} Project → mid-v1.1%%" no-close />

</div>


<div id="v11">

Covered by the 'Product' component of v1.1:

<panel src="../../admin/project-w07-v11.md#main" header="%%Admin {{ icon_embedding }} Project → v1.1%%" no-close />

</div>


<div id="product_design">

No textbook section. To be covered during the lecture.

{{ evidence }}

Apply the discussed guidelines when designing the product (covered by v1.1 deliverables).

</div>


<div id="mid-v12">

Covered by:

<panel src="../../admin/project-w08-mid-v12.md#main" header="%%Admin {{ icon_embedding }} Project → mid-v1.2%%" no-close />

</div>


<div id="v12">

Covered by:

<panel src="../../admin/project-w09-v12.md#main" header="%%Admin {{ icon_embedding }} Project → v1.2%%" />

</div>


<div id="mid-v13">

Covered by:

<panel src="../../admin/project-w10-mid-v13.md#main" header="%%Admin {{ icon_embedding }} Project → mid-v1.3%%" />

</div>


<div id="v13">

Covered by:

<panel src="../../admin/project-w11-v13.md#main" header="%%Admin {{ icon_embedding }} Project → v1.3%%" no-close/>

</div>


<div id="mid-v14">

Covered by:

<panel src="../../admin/project-w12-mid-v14.md#main" header="%%Admin {{ icon_embedding }} Project → mid-v1.4%%" />

</div>


<div id="v14">

Covered by:

<panel src="../../admin/project-w13-v14.md#main" header="%%Admin {{ icon_embedding }} Project → v1.4%%" />

</div>


<div id="relate_process">

Relate this model and some of its practices to the project. %%&nbsp;e.g. Are you doing something similar? Will it help if you adopt those practices? If they are not applicable, why?%%

</div>


<div id="demo">

Covered by the 'Demo' component of v1.4:

<panel src="../../admin/project-w13-v14.md#main" header="%%Admin {{ icon_embedding }} Project → v1.4%%" />

</div>
