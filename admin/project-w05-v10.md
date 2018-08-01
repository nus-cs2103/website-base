{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<tip-box>

Overview: <include src="project-timeline.md#v10-overview" inline />
</tip-box>

**v1.0 Summary of Milestone**

Here is a summary of items you need to deliver to _reach_ v1.1 individual ({{ icon_individual }}) and team ({{ icon_team }}) milestones. See sections below for more details of each item. 

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
{{ icon_team }} requirements documented | a draft of v2.0 requirements in some form
{{ icon_individual }} [optional] product survey documented | none
{{ icon_team }} v2.0 conceptualized | a draft of v2.0 user guide in some form
{{ icon_team }} feature releases planned | a rough feature release plan

:exclamation: ==Reaching individual and team milestones are considered for grading== the _project management_ component of your project grade (expand the panel below for more info).

:exclamation: The deadline for reaching a milestone is ==the midnight before your tutorial== %%e.g., if your tutorial is on Wednesday, you need to reach the milestone by Tuesday midnight.%%

<panel src="project-assessment.md#project-management-grading" header="Admin {{ icon_embedding }} Project Assessment → Project Management" class="embedding" minimized />

### v1.0 Documentation

* **Developer Guide**:
  Have a draft of the requirements of your project, as described in mid-v1.0 progress guide.
  
* **User Guide**:  
  Draft a user guide in a convenient format (e.g., a GoogleDoc) to describe what the product would be like when it is at 2.0.  We recommend that you follow the existing <tooltip content="AddressBook-Level4">AB4</tooltip> User Guide in terms of structure and format.

  <tip-box> 
  
  :bulb: It is highly recommended that you **divide documentation work (in the User Guide and the Developer Guide) among team members based on enhancements/features each person would be adding** %%&nbsp;e.g., If you are the person planing to add a feature X, you should be the person to describe the feature X in the User Guide and in the Developer Guide%%. For features that are not planned to be implemented by v1.4, you can divide them based on who will be implementing them _if_ the project were to continue until v2.0 (hypothetically).
  
  %%Reason: In the final project evaluation your documentation skills will be graded based on sections of the User/Developer Guide you have written.%%
    
  </tip-box>


**Suggested length**: Follow the existing user guide and developer guides in terms of the level of details.

**Submission**: Save your draft a single pdf file, name it `{Your Team ID}.pdf` %%e.g., `W09-3.pdf`%% and upload to IVLE.

### v1.0 Project Management

* After the v2.0 is conceptualized, decide which features each member will do by v1.4. %%We realize that it will be hard for you to estimate the effort required for each feature as you are not familiar with the code base. Nevertheless, come up with a project plan as per your best estimate; this plan can be revised at later stages. It is better to start with _some_ plan rather than no plan at all. If in doubt, choose to do _less_ than _more_; we don't expect you to deliver a lot of big features.%%
* Divide each of those features into three increments, to be released at v1.1, v1.2, v1.3 (v1.4 omitted deliberately as a buffer). Ideally, each increment should deliver a end-user testable enhancement.
* Document the above two items somewhere e.g., in a Google doc/sheet

**Submission**: Include in the pdf file you upload to IVLE.

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w05-v10", show_main_text) }}