{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("gradeBreakdown") %}
<div id="main">

<mermaid>
pie title
"Participation" : {{ marks_participation }}
"Individual Project (iP)" : {{ marks_ip }}
"Team Project (tP)" : {{ marks_tp }}
"exam" : {{ marks_exam }}
</mermaid>

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
  + Project Management: <b><color:red>{{ marks_tp_pm }}</color></b> marks
 + Exam: <b><color:red>{{ marks_exam }}</color></b> marks
@endwbs
</puml>

<div id="marks-for-peer-support">
<box type="important" seamless tags="m--cs2103">

****HEADS UP: 5 extra marks for community engagement!****{.text-danger}

****Aim:**** **A student who does well in <tooltip content="i.e., activities that engages with, and benefits, fellow students in the class">peer-support activities</tooltip> should receive one letter grade higher** than another student who doesn't do well in this aspect, all other things being equal.<br>
Rationale: Such activities are mutually beneficial, and enhances learning of you and your classmates.

****How**** **does it work? There are at least 5 bonus marks allocated for such activities**. These marks are embedded inside various grade components (i.e., iP, tP, participation).

****Examples of eligible activities**** (non-exhaustive):

* Engaging in forum discussions.
* Helping others to test their iP/tP, as requested via the forum.
* Giving peer feedback via pull request reviews of team members (in the tP) and other students (in the iP).
* Peer evaluations in iP and tP.
* Helping to find bugs in another teams product (in the tP practical exam dry run).

****What qualifies for bonus marks:**** While most of the eligible activities already have participation points attached to them, the **bonus marks are earned by going the extra mile to help peers**. Some examples:
* Providing more useful/thoughtful inputs.
* Doing notably more than the minimum requirement.

****What doesn't qualify?**** Obvious attempts to grab bonus marks by gaming the system will not earn bonus marks though. Some examples:

* Only a short burst of activity (instead of consistent activity over the semester).
* Spammy/trivial posts/response.
* Regurgitating useless AI slop as feedback/responses.
* 'Manufacturing' bogus activities (e.g., starting superfluous forum threads)
</box>
</div>

{{ embed_topic(baseUrl+"/admin/participation.md#main", "Admin " + icon_embedding + " Participation Marks", "3") }}
<p/>
{{ embed_topic(baseUrl+"/admin/ip-grading.md#main", "Admin " + icon_embedding + " Individual Project (iP) Grading", "3") }}
<p/>
{{ embed_topic(baseUrl+"/admin/tp-grading.md#main", "Admin " + icon_embedding + " Team Project (tP) Grading", "3") }}
<p/>
{{ embed_topic(baseUrl+"/admin/exams.md#main", "Admin " + icon_embedding + " Exams", "3") }}

</div>

{% endcall %}
