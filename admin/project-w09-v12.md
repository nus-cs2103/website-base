{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. {{ icon_individual }} Deliver an intermediate version of the new features
1. {{ icon_team }} Wrap up milestone
1. {{ icon_individual }} Demo new features
{% endcall %}

<div id="body">

#### {{ icon_individual }} Deliver an intermediate version of the new features

* The feature should be merged and user visible, although simpler than the version you intend to deliver at v1.4.

#### {{ icon_team }} Wrap up milestone

* {{ icon_team }} Manage the milestone v1.2 as explained in <trigger trigger="click" for="modal:v12-projectTracking">[Admin {{ icon_embedding }} Appendix E: GitHub: Project Schedule Tracking]</trigger>.
* **Wrap up the milestone using a git tag `v1.1`** as explained below:
  * When the milestone deadline is near (e.g., 0.5 days before the deadline), if you think some of the ongoing work intended for the current milestone may not finish in time, reassign them to a future milestone.

#### {{ icon_individual }} Demo new features

* Do an informal demo of the new feature during the tutorial. ==To save time, we recommend that one member demos all new features, using the commit tagged as `v1.2` in the `master` branch== %%i.e. only features included in the current release should be demoed%%.

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w09-v12", show_main_text) }}