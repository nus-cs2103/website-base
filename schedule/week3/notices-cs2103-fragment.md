{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}
{% from "common/topics.njk" import  panopto with context %}

<include src="../../admin/common-notices-fragment.md#tutorial-start" />

<box type="info" header="**In-video quizzes can earn you bonus participation marks!**" dismissible >

<include src="../../admin/participation.md#in-video-quiz-info" />

Answering in-video quizzes can earn you [bonus participation marks](../../admin/participation.md).
</box>

{% if S == "2" %}
<!--
<box type="important" dismissible>

**Heads up: PE rescheduled!**{.text-danger}

Due to the Good Friday holiday, the [team project practical exam](../../admin/tp-pe.html) that we usually do on the last lecture day ({{ get_date(date_w13_start, 4, format=format_normal, time="1400-1600") }}) has been ==rescheduled on the following day (**{{ get_date(date_w13_start, 5, format=format_normal, time="1400-1600") }}**)==. Please keep your calendar clear on that slot.
</box>
-->
{% endif %}
{% if cs2103 %}

{{ embed_topic(baseUrl+"/admin/gradeBreakdown.md#marks-for-peer-support", "Admin " + icon_embedding + " Grade Breakdown → Extract", "2", indent="0", status="peek", type="danger") }}

{% endif %}

<panel type="info" header="##### ==[MUST-WATCH]== Course Briefing Videos" expanded >

One course briefing video to watch this week, given below:

<include src="../../admin/courseBriefings.md#course-briefing-w3" />

As usual, the _weekly_ briefing (i.e., Week 3->4 transition, covering a recap of Week 3 and a preview of Week 4) will be in hybrid mode.{% if semester=="AY2425S2" %} But it will start around 5pm, to make room for the mass tutorial that starts at 4pm.{% endif %}
</panel>
<p/>