{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Start weekly project meetings
1. Decide on a overall project direction %%(user profile, problem addressed).%%
1. Start a collaborative doc to take project notes
{% endcall %}

<div id="body">

Given below are some guidance on the recommended progress at this point of the project

#### {{ thumb(1) }} Start weekly project meetings

* We recommend you start weekly project meetings now. You can use the meeting to do tP tasks, but also help each other do iP tasks.

#### {{ thumb(2) }} Decide on a overall project direction %%(user profile, problem addressed)%%

* **Decide project direction, target user profile, and problem addressed**

  Use your first project meeting to discuss with your team members and decide your project direction, target user profile, and the value proposition of the product, as described in <trigger trigger="click" for="modal:v10-scope">[Admin {{ icon_embedding }} Project Scope]</trigger>

<modal large title="Admin {{ icon_embedding }} Project Scope (Extract)" id="modal:v10-scope">
  <include src="project-scope.md#project-direction"/>
</modal>

#### {{ thumb(3) }} Start a collaborative doc to take project notes

* We recommend you keep project notes in a easy-to-use collaborative docs such as GoogleDocs/sheets. Document the decisions taken above in the collaborative docs.

</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w04-inception", show_main_text) }}