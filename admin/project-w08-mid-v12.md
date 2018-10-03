{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<p class="lead" style="color: purple"><md>{{ far_calendar_check }} <include src="project-timeline.md#mid-v12-overview" inline /></md><p/>

**<big>Project Management:</big>**

<box>

:bulb: **You are free to adjust _process rigor_ and _project plan_ at any future time in the project**, starting from v1.2. If you are not sure if a certain adjustment is allowed, you can check with the teaching team first.
</box>

* **Switch to AB-3 or AB-2 if AB-4 is not working out for you**.

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#notes-for-ab23", "Admin " + icon_embedding + " Project Deliverables → Notes for Those Using AB-2 or AB-3 for the Project", "midv12-notesForAb23", "3") }}
</div>


* **Adjust process rigor to suit your team's pace**, as explained in the panel below.

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#workflow-after-v11", "Admin " + icon_embedding + " Appendix E(extract): **Workflow (after v1.1)**", "midv12-workflowAfterV11", "3") }}
</div>


* **Adjust project plan if necessary**. Now that you have a some idea about the code base, revisit the feature release plan and adjust it if necessary.

* **Set up the issue tracker** as described in the panel below, if you haven't done so already.

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#issue-tracker-setup", "Admin " + icon_embedding + " Appendix E(extract): **Setting up the issue tracker**", "midv12-issueTrackerSetup", "1") }}
</div>


* **Start proper schedule tracking and milestone management** as explained in the panel below.

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#project-schedule-tracking", "Admin " + icon_embedding + " Appendix E(extract): **Project schedule tracking**", "midv12-projectScheduleTracking", "1") }}
</div>

<div id="product">

**<big>Product:</big>**

* **From v1.2 onwards each member is expected to contribute <tooltip content="the amount of code does not matter; even small contributions are acceptable">some</tooltip> code to each <tooltip content="v1.3, v1.4"> milestone</tooltip>, preferably each week; only merged code is considered as contributions** %%<popover content="The ability to deliver code incrementally is an important LO of this module because incremental delivery improves the _visibility_ of your work.">(Reason)</popover>%%. <br>
 If an enhancement is too big to complete in one milestone, try to deliver it in smaller incremental steps e.g. deliver a basic version of the enhancement first.


</div>

</div>

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w08-mid-v12", show_main_text) }}