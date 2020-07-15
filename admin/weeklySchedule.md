{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("weeklySchedule") %}
<div id="main">

<include src="common-notices.mbdf#fully-online" />
<p/>
</div>

<div id="week-definition">

### {{ module_pair }} week vs normal academic week

**Each {{ module_pair }} week starts with the lecture** and ends just before the following week's lecture. The only exception is week 1, which starts on the Monday of the first week of the semester. <div tags="m--cs2103 m--cs2113 m--tic4001">As our lecture is on {{ day_lecture }}, =={{ module_pair }} week starts a few days earlier than the normal NUS academic week==. For example, {{ module_pair }} week 2 starts on the {{ day_lecture }} of NUS week 1.</div>
</div>
<p/>
<div tags="m--cs2103 m--cs2113 m--tic4001" id="deadline-definition">

### Deadline for weekly tasks

<div tags="m--cs2103 m--cs2113">

**The deadline to complete tasks allocated to the week** is the <tooltip content="e.g., if your tutorial is on Thursday, the deadline is Wednesday 23.59">midnight before your tutorial day</tooltip>, unless stated otherwise. Our grading scripts that detect your work run at midnight and only the work that's done by midnight will be eligible for marks (for cases where the task is graded).
</div>
<div tags="m--tic4001">

**The deadline to complete tasks allocated to the week** is the midnight before the following lecture.
</div>
</div>

<div tags="m--cs2103 m--cs2113">

### The typical weekly cycle

{{ icon_calendar }} **[Lecture day ({{ day_lecture }})]**<br>

* Attend the lecture to, 
  * see a recap of the preceding week's topics
  * get an introduction to the current week's topics
  * submit the in-lecture quiz/activities (if any)

{{ embed_topic("lectures.md#main", "Admin " + icon_embedding + " Lectures", "3", indent=2) }}

<p/>

{{ icon_calendar }} **[End of lecture - Start of tutorial]**<br>
 
 * Use the relevant learning resources to learn the topics.
 * Self-test your knowledge using exercises given in the learning resources. 
 * ==Submit the post-lecture quiz/exercises== (if any)
 * ==Do project tasks== %%(e.g., attend weekly project meeting, finish weekly deliverables)%%
 * If you don't have time to learn all topics assigned to the week, use the star rating system to decide which ones to do first.

<div tags="m--cs2103 m--cs2113 m--tic2002">
<box type="warning">

<span id="before-attempting-tasks">

**Before attempting weekly project tasks,** go through the weekly topics (and do the weekly programming exercises/activities, if any) as the knowledge from those topics may be needed to complete the project tasks.
</span>

</box>
</div>

<p/>

{{ icon_calendar }} **[During tutorial]**<br>
 
* Attend the tutorial to,
  * demonstrate evidence of your learning weekly topics to the tutor
  * learn from peer demos of showing evidence of their own learning

{{ embed_topic("tutorials.md#main", "Admin " + icon_embedding + " Tutorials", "2", indent=2) }}
<p/>

{{ icon_calendar }} **[End of tutorial - Start of lecture]**<br>

* Downtime (or catch-up with missed tasks)

</div>

</div>

{% endcall %}
