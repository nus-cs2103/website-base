{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("gradeBreakdown") %}
<div id="main">

<puml src="images/grade-breakdown.puml" />

{{ embed_topic("participation.md#main", "Admin " + icon_embedding + " Participation Marks", "3") }}
{{ embed_topic("exams.md#main", "Admin " + icon_embedding + " Exams", "3") }}
{{ embed_topic("ip-grading.md#main", "Admin " + icon_embedding + " Individual Project (iP) Grading", "3") }}
{{ embed_topic("tp-grading.md#main", "Admin " + icon_embedding + " Team Project (tP) Grading", "3") }}

</div>

{% endcall %}
