{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body"> 

<p class="lead" style="color: purple"><md>{{ far_calendar_check }} <include src="project-timeline.md#v11-overview" inline /></md></p>

{{ icon_important_big_red }} **Milestone progress is graded**. Be reminded that reaching individual and team milestones are considered for <trigger trigger="click" for="modal:v11-projectMgtGrading">grading the _project management_ component</trigger> of your project grade.

{{ icon_important_big_red }} **Most aspects project progress are tracked using automated scripts.** ==lease follow our instructions closely or else the script will not be able to detect your progress==. We prefer not to spend admin resources processing requests for partial credit for work that did not follow the instructions precisely, unless the progress was not detected due to a bug in the script.

{{ icon_important_big_red }} **Milestone requirements are cumulative**. The recommended progress for the mid-milestone is an implicit requirement for the actual milestone unless a milestone requirement overrides a mid-milestone requirement %%e.g., mid-milestone requires a document to be in a temp format while the actual milestone requires it to be in the proper format%%. Similarly, a requirement for milestone `n` is also an implicit requirement for milestone `n+1` unless `n+1` overrides the `n` requirement. This means ==if you miss some requirement at milestone `n`, you should try to achieve it before milestone `n+1`== or else it could be noted again as a 'missed requirement' at milestone `n+1`.

**v1.1 Summary of Milestone**

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
{{ icon_team }} Team org/repo set up | as stated in <trigger trigger="click" for="modal:v11summary-midv11">mid-v1.1</trigger> (i.e., _team PR_ created, _auto-publishing_ of docs set up)
{{ icon_individual }} Some code enhancements done | created PRs to do local/global changes
{{ icon_individual }} Photo uploaded | a photo complying to <trigger trigger="click" for="modal:v11-photo">our guidelines</trigger> is in the master branch of your team repo
{{ icon_team }} Project docs updated | updated docs are merged to the master branch
{{ icon_team }} Milestone wrapped up | a commit in the master branch tagged as `v1.1`


<modal large title="Admin {{ icon_embedding }} Project: mid-v1.1" id="modal:v11summary-midv11">
  <include src="project-w06-mid-v11.md#body"/>
</modal>

<modal large title="Admin {{ icon_embedding }} Project Assessment → Project Management" id="modal:v11-projectMgtGrading">
  <include src="project-assessment.md#project-management-grading"/>
</modal>

<modal large title="Admin {{ icon_embedding }} Choosing a profile photo" id="modal:v11-photo">
  <include src="project-deliverables.md#profile-photo"/>
</modal>

<div id="documentation">

### v1.1 Project Management

* {{ icon_team }} Fix any errors in org/repo set up %%&nbsp;(e.g. wrong repo name)%%.
* **Wrap up the milestone using a git tag `v1.1`** as explained below:
  * When the milestone deadline is near (e.g., 0.5 days before the deadline), if you think some of the ongoing work intended for the current milestone may not finish in time, reassign them to a future milestone.
  * After all changes that _can_ be merged before the milestone deadline has been merged, use `git tag` feature to tag the current version with the milestone and push the tag to the team repo.


### v1.1 Documentation

* Update User Guide, Developer Guide, README, and About Us pages as described earlier in <trigger trigger="click" for="modal:v11docs-midv11">mid-v1.1 progress guide</trigger>.

  **Submission**: merge your changes to the master branch of your repo.

<modal large title="Admin {{ icon_embedding }} Project: mid-v1.1" id="modal:v11docs-midv11">
  <include src="project-w06-mid-v11.md#body"/>
</modal>

</div>
<div id="product">

### v1.1 Product

* Each member should try to add some enhancements that are in line with the vision for v2.0. After adding some _local-impact_ changes as recommended in <trigger trigger="click" for="modal:v11docs-midv11">mid-v1.1 progress guide</trigger>, attempt to do some ==<tooltip content="should go beyond the component you are in charge of">_global-impact_</tooltip> enhancements==, touching as many other components as possible. Refer to the AddressBook-Level4 Developer Guide has [some guidance on how to implement a new feature end-to-end](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/addressbook-level4/DeveloperGuide.html#creating-a-new-command-code-remark-code).

</div>

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w07-v11", show_main_text) }}