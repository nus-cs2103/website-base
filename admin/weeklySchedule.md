{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("weeklySchedule") %}
<div id="main">

<box type="info">

<span id="week-definition">

**Each {{ module_pair }} week starts with the lecture** on the date given in the timeline below and end just before the following week's lecture. The only exception is week 1, which starts on the Monday of the first week of the semester.
</span>
</box>

{{ icon_calendar }} **[{{ day_lecture }} (previous week)]**<br>

* Attend the lecture to, 
  * see a recap of the preceding week's topics
  * get an introduction to the current week's topics
  * submit the in-lecture quiz/activities (if any)

<div class="indented-level2">
{{ embed_topic("lectures.md#main", "Admin " + icon_embedding + " Lectures", "3") }}
</div>

<p/>

{{ icon_calendar }} **[End of lecture - Start of tutorial]**<br>
 
 * Use the relevant learning resources to learn the topics.
 * Self-test your knowledge using exercises given in the learning resources. 
 * ==Submit the post-lecture quiz/exercises== (if any)
 * ==Do project tasks== %%(e.g., attend weekly project meeting, finish weekly deliverables)%%
 * If you don't have time to learn all topics assigned to the week, use the star rating system to decide which ones to do first.

<p/>

{{ icon_calendar }} **[During tutorial]**<br>
 
* Attend the tutorial to,
  * demonstrate evidence of your learning weekly topics to the tutor
  * learn from peer demos of showing evidence of their own learning

<div class="indented-level2">
{{ embed_topic("tutorials.md#main", "Admin " + icon_embedding + " Tutorials", "2") }}
</div>
<p/>

{{ icon_calendar }} **[End of tutorial - Start of lecture]**<br>

* Downtime (or catch-up with missed tasks)


</div>

{% endcall %}
