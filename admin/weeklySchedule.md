{% macro show_main_text() %}
<div id="main">

:calendar: **[Friday (previous week)]**<br>

Attend the lecture for, 
* a recap of the preceding week's Learning Outcomes (LOs)
* an introduction to the current week's LOs

<panel src="lectures.md#main" header="Admin {{ icon_embedding }} Lectures {{ glyphicon_star }}{{ glyphicon_star }}{{ glyphicon_star }}" class="embedding" minimized />

<p/>

:calendar: **[Saturday (previous week) - Tuesday]**<br>
 
 * Use the relevant learning resources to achieve the LOs. 
 * Self-test your knowledge using exercises given in the learning resources. 
 * If you don't have time to achieve all LOs assigned to the week, use the star rating system to decide which ones to do first.

<panel src="learningOutcomes.md#main" header="Admin {{ icon_embedding }} Learning Outcomes {{ glyphicon_star }}{{ glyphicon_star }}" class="embedding" minimized />

<p/>

:calendar: **[Wednesday - Friday]**<br>
 
Attend the tutorial to,

* demonstrate evidence of your achieving weekly LOs to the tutor
* learn from peer demos of their own LO evidence

<panel src="tutorials.md#main" header="Admin {{ icon_embedding }} Tutorials {{ glyphicon_star }}{{ glyphicon_star }}{{ glyphicon_star }}" class="embedding" minimized />


</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("weeklySchedule", show_main_text) }}