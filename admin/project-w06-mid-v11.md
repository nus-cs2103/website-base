{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<p class="lead" style="color: purple"><md>{{ far_calendar_check }} <include src="project-timeline.md#mid-v11-overview" inline /></md><p/>

<div id="product">

**<big>Project Management:</big>**

Set up the team org and the team repo as explained below:

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#organization-setup", "Admin " + icon_embedding + " Appendix E(extract): **Organization setup**", "midv11-orgSetup", "1") }}
</div>

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#repo-setup", "Admin " + icon_embedding + " Appendix E(extract): **Repo setup**", "midv11-repoSetup", "1") }}
</div>


When updating code in the repo, follow the workflow explained below:

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#workflow", "Admin " + icon_embedding + " Appendix E(extract): **Workflow**", "midv11-workflow", "1") }}
</div>


</div>
<div id="documentation">

**<big>Documentation:</big>** 

<tip-box>

**Recommended procedure for updating docs**:

1. Divide among yourselves who will update which parts of the document(s).
1. Update the team repo by following the workflow mentioned above.

</tip-box>

<div class="indented">

  Update the following pages in your project repo:
</div> 
 
* **About Us page**:  
  This page is used for module admin purposes. ==Please follow the format closely== or else our scripts will not be able to give credit for your work.
  * Replace info of SE-EDU developers with info of your team, including a ==suitable photo== as described <trigger trigger="click" for="modal:mid-v12-photo">here</trigger>.  
  * Including the name/photo of the supervisor/lecturer is optional. 
  * The photo of a team member should be `doc/images/githbub_username_in_lower_case.png` %%e.g. `docs/images/damithc.png`%%. ==If you photo is in jpg format, name the file as `.png` anyway==.
  * Indicate the different roles played and responsibilities held by each team member. You can reassign these <trigger trigger="click" for="modal:midv11-rolesAndResponsibilities">roles and responsibilities %%(as explained in Admin {{ icon_embedding }} Project Scope)%%</trigger> later in the project, if necessary.

<modal large title="Admin {{ icon_embedding }} Choosing a profile photo" id="modal:mid-v12-photo">
  <include src="project-deliverables.md#profile-photo"/>
</modal>

<modal large title="Admin {{ icon_embedding }} Project Scope (extract): roles and responsibilities" id="modal:midv11-rolesAndResponsibilities">
  <include src="project-scope.md#roles"/>
</modal>

* **README.adoc** page: Update it to match your project.

  * Add a UI mockup of your intended final product.   
    Note that the ==image of the UI should be `docs/images/Ui.png`== so that it can be downloaded by our scripts. Limit the file to contain one screenshot/mockup only and ensure the new image is roughly the same `height x width` proportions as the original one. %%Reason: when we compile these images from all teams into one page ([example](https://nus-cs2103-ay1819s1.github.io/cs2103-website/admin/projectList.html)), yours should not look out of place.%%

  * The original `README.adoc` file (which doubles as the landing page of your project website) is written to read like the introduction to an SE learning/teaching resource. You should ==restructure this page to look like the home page of a real product== (not a school project) targeting real users %%&nbsp;e.g. remove references to addressbook-level3, Learning Outcomes etc. mention target users, add a marketing blurb etc.%% On a related note, also remove `Learning Outcomes` link and related pages.

  * Update the link of the Travis _build status badge_ (<img src="https://travis-ci.org/se-edu/addressbook-level4.svg?branch=master" alt="Build Status">) so that it reflects the build status of your team repo.<br>
    For the other badges,
    * either set up the respective tool for your project (AB-4 Developer Guide has instructions on how to set up AppVeyor and Coveralls) and update the badges accordingly,
    * or remove the badge.

  * Acknowledge the original source of the code i.e. AddressBook-Level4 project created by SE-EDU initiative at `https://github.com/se-edu/`

* **User Guide**: Start moving the content from your User Guide (draft created in previous weeks) into the User Guide page in your repository. If a feature is not implemented, mark it as 'Coming in v2.0' ([example](https://se-edu.github.io/addressbook-level4/UserGuide.html#encrypting-data-files-code-coming-in-v2-0-code)).

* **Developer Guide**: Similar to the User Guide, start moving the content from your Developer Guide (draft created in previous weeks) into the Developer Guide page in your team repository.

**<big>Product:</big>**

* Each member can attempt to do a <tooltip content="a change impacting only one component">local-impact</tooltip> change to the code base.

  **Objective**: To familiarize yourself with at least one <tooltip content="components as stated in the [Developer Guide: Architecture]">components</tooltip> of the product.

  **Description**: Divide the components among yourselves. Each member can do some small enhancements to their component(s) to learn the code of that component. Some suggested enhancements are given in the [AddressBook-Level4 developer guide](https://nus-{{ module | lower }}-{{ semester }}.github.io/addressbook-level4/DeveloperGuide.html#improving-each-component).

  **Submission**: Create PRs from your own fork to your team repo. Get it merged by following your team's workflow.


</div>

</div>
</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w06-mid-v11", show_main_text) }}