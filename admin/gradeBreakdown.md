{% macro show_main_text() %}
<div id="main">

<img src="{{baseUrl}}/admin/images/gradeBreakdown.png" width="600"/>
<p/>
<span class="flat"><markdown>
%%Related: [[Admin: Participation Marks](#admin-participation-anchor)][[Admin: Exams](#admin-exams-anchor)][[Admin: Project: Assessment](#admin-project-assessment-anchor)]%%
</markdown></span>
<panel src="participation.md#main" header="Admin {{ icon_embedding }} Participation Marks" class="embedding" minimized  />
<panel src="exams.md#main" header="Admin {{ icon_embedding }} Exams" class="embedding" minimized  />
<panel src="project-assessment.md#main" header="Admin {{ icon_embedding }} Project Assessment" class="embedding" minimized  />

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("gradeBreakdown", show_main_text) }}