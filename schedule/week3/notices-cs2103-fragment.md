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

Due to the Good Friday holiday, the [team project practical exam](../../admin/tp-pe.html) that we usually do on the last lecture day ({{ get_date(date_w13_start, 7, format=format_normal, time="1400-1600") }}) has been ==rescheduled on the following day (**{{ get_date(date_w13_start, 8, format=format_normal, time="1400-1600") }}**)==. Please keep your calendar clear on that slot.
</box>
-->
{% endif %}

<panel type="info" header="##### ==[MUST-WATCH]== One More Course Briefing Segment (9 minutes)" expanded >

**One more course briefing segment to watch this week**: The bulk of the course briefing was released as pre-recorded videos last week. There are few more remaining parts which will be released closer to events they cover %%(e.g., the part covering the exam will be released closer to the exam)%%. This week, we cover one more course briefing segment, given below:

<include src="../../admin/courseBriefings.md#course-briefing-w3" />

**The _weekly_ briefing for this week will be done in hybrid mode** -- you can attend it F2F %%(@{{ lecture_venue }} {{ get_date(date_w3_start, 0, format=format_normal, time="from 4pm") }})%%, join via Zoom, watch the recording later, or skip it altogether).<br>
==**iP Help Session**==: This week's' briefing will be followed by a F2F help session for those who are stuck in the iP due to technical difficulties. To attend that help session, be in {{ lecture_venue }} at least by 4.50pm.
</panel>
<p/>