{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body"> 

<p class="lead" style="color: purple"><md>{{ far_calendar_check }} <include src="project-timeline.md#v11-overview" inline /></md></p>

**v1.1 Summary of Milestone**

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
{{ icon_team }} Team org/repo set up | as stated
{{ icon_individual }} Have done some enhancement to the code | at least attempted to enhance the code of a component, even if you did not fully succeed
{{ icon_team }} All project documents updated as required | updated docs are merged to the master branch

{{ icon_important_big_red }} Reminder: Reaching individual and team milestones are considered for <trigger trigger="click" for="modal:v11-projectMgtGrading">grading the _project management_ component</trigger> of your project grade.

<modal large title="Admin {{ icon_embedding }} Project Assessment → Project Management" id="modal:v11-projectMgtGrading">
  <include src="project-assessment.md#project-management-grading"/>
</modal>

<div id="documentation">

### v1.1 Project Management

* {{ icon_team }} Fix any errors in org/repo set up %%&nbsp;(e.g. wrong repo name)%%.

* When all changes intended for v1.1 is merged to the master branch, use `git tag` feature to tag the current version as `v1.1`


### v1.1 Documentation

* Update User Guide, Developer Guide, README, and About Us pages as described earlier.

  **Submission**: merge your changes to the master branch of your repo.

</div>
<div id="product">

### v1.1 Product

* Each member should try to add some enhancements that are in line with the vision for v2.0. Preferably, these ==should be <tooltip content="should go beyond the component you are in charge of">_global-impact_</tooltip> enhancements==, touching as many other components as possible. Refer to the AddressBook-Level4 Developer Guide has [some guidance on how to implement a new feature end-to-end](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/addressbook-level4/DeveloperGuide.html#creating-a-new-command-code-remark-code).

</div>

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w07-v11", show_main_text) }}