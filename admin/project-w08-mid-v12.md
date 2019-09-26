{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. {{ icon_team }} Adjust process rigor if necessary
1. {{ icon_team }} Start proper milestone management
1. {{ icon_individual }} Add another increment to your feature
{% endcall %}
<div id="body">


#### {{ thumb(0, "secondary") }} %%{{ icon_individual }} Ensure you know tP expectations%%

* If you haven't done so already, make sure you know individual and team expectations of the tP

<div class="indented-level2">

{{ embed_topic("project-scope.md#individualExpectations", "Admin " + icon_embedding + " tP Scope: Individual Expectations", "midv12-teamScope", "3") }}
{{ embed_topic("project-scope.md#team-expectations", "Admin " + icon_embedding + " tP Scope: Team Expectations", "midv12-individualScope", "3") }}
</div>


#### {{ thumb(1) }} {{ icon_team }} Adjust process rigor if necessary

* **Adjust process rigor to suit your team's pace**, as explained in the panel below.

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#workflow-after-v11", "Admin " + icon_embedding + " Appendix E(extract): **Workflow (after v1.1)**", "midv12-workflowAfterV11", "3") }}

<box type="tip">

**You are free to adjust _process rigor_ and _project plan_ at any future time in the project**, starting from v1.2. If you are not sure if a certain adjustment is allowed, you can check with the teaching team first.
</box>

</div>

#### {{ thumb(2) }} {{ icon_team }} Start proper milestone management

* **Set up the issue tracker** as described in the panel below, if you haven't done so already.

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#issue-tracker-setup", "Admin " + icon_embedding + " Appendix E(extract): **Setting up the issue tracker**", "midv12-issueTrackerSetup", "1") }}
</div>

* **Start proper schedule tracking and milestone management** as explained in the panel below.

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#project-schedule-tracking", "Admin " + icon_embedding + " Appendix E(extract): **Project schedule tracking**", "midv12-projectScheduleTracking", "1") }}
</div>

<div class="indented">

{{ icon_tip }} **Try to achieve all milestone requirements, but do not fret if you miss a few**.  You will get full marks as long as you achieve about 60% of the milestone requirements on average. Yes, that's a pretty low bar, but we have set it low in order to reduce workload and stress. Ideally, you should achieve close to 80-90%.
</div>

#### {{ thumb(3) }} {{ icon_individual }} Add another increment to your feature

* Add an increment to your feature, aiming to deliver a ==user-visible== version of your feature by v1.2 %%i.e., simpler than the feature intended for v1.4, but still usable by the user%%.

* {{ icon_important_big_red }} **From v1.2 onwards each member is expected to contribute <tooltip content="the amount of code does not matter; even small contributions are acceptable">some</tooltip> code to each <tooltip content="v1.3, v1.4"> milestone</tooltip>, preferably each week; only merged code is considered as contributions** %%<popover content="The ability to deliver code incrementally is an important learning outcome of this module because incremental delivery, among other things, improves the _visibility_ of your work.">(Reason)</popover>%%. <br>
 If an enhancement is too big to complete in one milestone, try to deliver it in smaller incremental steps e.g. deliver a basic version of the enhancement first.


</div>

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w08-mid-v12", show_main_text) }}