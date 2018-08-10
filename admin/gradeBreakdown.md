{% macro show_main_text() %}
<div id="main">

<img src="{{baseUrl}}/admin/images/gradeBreakdown.png" width="600"/>
<p/>
<span class="flat"><markdown>
%%Related: [[Admin: Participation Marks]({{baseUrl}}/admin/index-flat.html#admin-participation-anchor)][[Admin: Exams]({{baseUrl}}/admin/index-flat.html#admin-exams-anchor)][[Admin: Project: Assessment]({{baseUrl}}/admin/index-flat.html#admin-project-assessment-anchor)]%%
</markdown></span>
{{ embed_topic("participation.md#main", "Admin " + icon_embedding + " Participation Marks", "gradeBreakdown-participation", "3") }}
{{ embed_topic("exams.md#main", "Admin " + icon_embedding + " Exams", "gradeBreakdown-exams", "3") }}
{{ embed_topic("project-assessment.md#main", "Admin " + icon_embedding + " Project Assessment", "gradeBreakdown-projectAssessment", "3") }}

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("gradeBreakdown", show_main_text) }}
