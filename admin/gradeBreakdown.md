{% macro show_main_text() %}
<div id="main">

<puml src="images/grade-breakdown.puml" />

{{ embed_topic("participation.md#main", "Admin " + icon_embedding + " Participation Marks", "3") }}
{{ embed_topic("exams.md#main", "Admin " + icon_embedding + " Exams", "3") }}
{{ embed_topic("ip-grading.md#main", "Admin " + icon_embedding + " Individual Project (iP) Grading", "3") }}
{{ embed_topic("project-grading.md#main", "Admin " + icon_embedding + " Team Project (tP) Grading", "3") }}

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("gradeBreakdown", show_main_text) }}
