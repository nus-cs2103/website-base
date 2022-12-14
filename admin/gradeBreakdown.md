{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("gradeBreakdown") %}
<div id="main">

<puml name="gradeBreakdown.png">
@startwbs
skinparam backgroundcolor transparent
+ <b><color:red>100</color></b> marks
 + Participation: <b><color:red>{{ marks_participation }}</color></b> marks
 + Individual Project (iP): <b><color:red>{{ marks_ip }}</color></b> marks
  + Implementation: <b><color:red>{{ marks_ip_implementation }}</color></b> marks
  + Documentation: <b><color:red>{{ marks_ip_documentation }}</color></b> marks
  + Project Management: <b><color:red>{{ marks_ip_pm }}</color></b> marks
 + Team Project (tP): <b><color:red>{{ marks_tp }}</color></b> marks
  + Design:<b><color:red>5</color></b> marks
  + Implementation: <b><color:red>{{ marks_tp_implementation }}</color></b> marks
  + Documentation: <b><color:red>{{ marks_tp_documentation }}</color></b> marks
  + QA: <b><color:red>{{ marks_tp_qa }}</color></b> marks
  + Project Management: <b><color:red>{{ marks_tp_pm }}</color></b> marks{% if not (tic4001 or tic4002)%}
 + MCQ + Essay : <b><color:red>{{ marks_exam_mcq }}</color></b> marks {% endif %}
@endwbs
</puml>

{{ embed_topic("participation.md#main", "Admin " + icon_embedding + " Participation Marks", "3") }}
<p/>
{{ embed_topic("ip-grading.md#main", "Admin " + icon_embedding + " Individual Project (iP) Grading", "3") }}
<p/>
{{ embed_topic("tp-grading.md#main", "Admin " + icon_embedding + " Team Project (tP) Grading", "3") }}
<p/>
{{ embed_topic("exams.md#main", "Admin " + icon_embedding + " Exams", "3") if module not in ["TIC4001", "TIC4002"] else "" }}

</div>

{% endcall %}
