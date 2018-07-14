{% macro show_main_text() %}
<div id="main">

# Grade Breakdown

<img src="{{baseUrl}}/admin/images/gradeBreakdown.png" width="600"/>
<p/>

<panel src="participation.md#main" header="Admin {{ icon_embedding }} Participation Marks" minimized  />
<panel src="exams.md#main" header="Admin {{ icon_embedding }} Exams" minimized  />
<panel src="project-assessment.md#main" header="Admin {{ icon_embedding }} Project Assessment" minimized  />

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("gradeBreakdown", show_main_text) }}