{% macro show_main_text() %}
<div id="main">

{{ icon_calendar }} **[Friday (previous week)]**<br>

* Attend the lecture to, 
  * see a recap of the preceding week's topics
  * get an introduction to the current week's topics
  * submit the in-lecture quiz

<div class="indented-level2">
{{ embed_topic("lectures.md#main", "Admin " + icon_embedding + " Lectures", "3") }}
</div>

<p/>

{{ icon_calendar }} **[Saturday (previous week) - Tutorial day]**<br>
 
 * Use the relevant learning resources to learn the topics.
 * Self-test your knowledge using exercises given in the learning resources. 
 * ==Submit the post-lecture quiz==
 * ==Do project tasks== %%(e.g., attend weekly project meeting, finish weekly deliverables)%%
 * If you don't have time to learn all topics assigned to the week, use the star rating system to decide which ones to do first.

<p/>

{{ icon_calendar }} **[Tutorial Day (Wednesday - Friday)]**<br>
 
* Attend the tutorial to,
  * demonstrate evidence of your learning weekly topics to the tutor
  * learn from peer demos of showing evidence of their own learning

<div class="indented-level2">
{{ embed_topic("tutorials.md#main", "Admin " + icon_embedding + " Tutorials", "2") }}
</div>


</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("weeklySchedule", show_main_text) }}