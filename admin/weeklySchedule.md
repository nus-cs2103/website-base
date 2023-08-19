{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("weeklySchedule") %}
<div id="main">

<div id="week-definition">

### {{ course_pair }} week vs normal academic week

**Each {{ course_pair }} week starts with the lecture** and ends just before the following week's lecture. The only exception is week 1, which starts on the Monday of the first week of the semester. <div tags="m--cs2103 m--cs2113 m--tic4001 m--tic4002">As our lecture is on {{ day_lecture }}, =={{ course_pair }} week starts a few days earlier than the normal NUS academic week==. For example, {{ course_pair }} week 2 starts on the {{ day_lecture }} of NUS week 1. See the [full timeline](../schedule/timeline.html) for exact dates.</div>
</div>
<p/>
<div tags="m--cs2103 m--cs2113 m--tic4001 m--tic4002" id="deadline-definition">

### Deadline for weekly tasks

<div tags="m--cs2103 m--cs2113">

**The soft deadline to complete tasks allocated to a week** is the <tooltip content="e.g., if your tutorial is on Thursday, the deadline is Wednesday 23.59">midnight before your tutorial day</tooltip>, unless a specific deadline is given. You are strongly encouraged to finish most weekly tasks before the soft deadline because some tutorial tasks are done best _after_ weekly tasks have been completed, for the best learning experience.

<span class="text-danger">**The hard deadline** for weekly tasks is the following lecture</span> i.e., do this week's task before the next week's lecture.

{% if not cs2113 %}**We are not strict with most interim weekly project deadlines** i.e., we'll not penalize you even if you occasionally miss those deadlines, as long as you catch up soon enough (within a few days after the hard deadline). This flexibility does not apply if a task description states a specific deadline.<br>
{% endif %}

**It's OK to make occasional mistakes in weekly tasks** (making mistakes is a natural part of learning new things after all). If a weekly task was not accepted as 'done' due to a mistake you made, go ahead and rectify the mistake as soon as you can -- our grading scripts will not penalize such mistakes if they are corrected soon after.

**We wont wait forever though.** Note that for most interim deliverables, we stop checking about one week after the deadline is over. So, work/corrections done more than one week after the deadline might not get noticed at all by our grading scripts, even as late submissions.
</div>
<div tags="m--tic4001 m--tic4002">

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

{{ embed_topic(baseUrl+"/admin/lectures.md#main", "Admin " + icon_embedding + " Lectures", "3", indent=2) }}

<p/>

{{ icon_calendar }} **[End of lecture - Start of tutorial]**<br>

 * Use the relevant learning resources to learn the topics.
 * Self-test your knowledge using exercises given in the learning resources.
 * ==Submit the post-lecture quiz/exercises== (if any)
 * ==Do project tasks== %%(e.g., attend weekly project meeting, finish weekly deliverables)%%
 * If you don't have time to learn all topics assigned to the week, use the topic levels system to decide which ones to do first.

<div tags="m--cs2103 m--cs2113 m--tic2002">
<box type="warning">

<span id="before-attempting-tasks">

{{ icon_important_big_red }} **Before attempting weekly project tasks,** go through the weekly topics{% if not cs2103 %} (and do the weekly programming exercises/activities, if any){% endif %} as the knowledge from those topics may be needed to complete the project tasks.
</span>

</box>
</div>

<p/>

{{ icon_calendar }} **[During tutorial]**<br>

* Attend the tutorial to,
  * demonstrate evidence of your learning weekly topics to the tutor
  * learn from peer demos of showing evidence of their own learning

{{ embed_topic(baseUrl+"/admin/tutorials.md#main", "Admin " + icon_embedding + " Tutorials", "2", indent=2) }}
<p/>

{{ icon_calendar }} **[End of tutorial - Start of lecture]**<br>

* Downtime (or catch-up with missed tasks)

</div>

</div>

{% endcall %}
