{% macro show_main_text() %}
<div id="main">

:calendar: **[Friday (previous week)]**<br>

Attend the lecture for, 
* a recap of the preceding week's Learning Outcomes (LOs)
* an introduction to the current week's LOs

{{ embed_topic("lectures.md#main", "Admin " + icon_embedding + " Lectures", "weeklySchedule-lectures", "3") }}

<p/>

:calendar: **[Saturday (previous week) - Tuesday]**<br>
 
 * Use the relevant learning resources to achieve the LOs. 
 * Self-test your knowledge using exercises given in the learning resources. 
 * If you don't have time to achieve all LOs assigned to the week, use the star rating system to decide which ones to do first.

{{ embed_topic("learningOutcomes.md#main", "Admin " + icon_embedding + " Learning Outcomes", "weeklySchedule-learningOutcomes", "2") }}

<p/>

:calendar: **[Wednesday - Friday]**<br>
 
Attend the tutorial to,

* demonstrate evidence of your achieving weekly LOs to the tutor
* learn from peer demos of their own LO evidence

{{ embed_topic("tutorials.md#main", "Admin " + icon_embedding + " Tutorials", "weeklySchedule-tutorials", "2") }}


</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("weeklySchedule", show_main_text) }}