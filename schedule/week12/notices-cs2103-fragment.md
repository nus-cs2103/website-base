{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}
<!--box type="info" header="****This week's lecture (and the PE Dry Run) ==rescheduled!==****">

As this week's lecture falls on a public holiday, it will be moved to the day after i.e., Saturday Apr 3rd 2-4pm.
==Attendance is compulsory==, as the lecture slot is also used for the Practical Exam Dry Run (<span class="text-danger">graded</span>).

</box-->

{% if pe_week == '12' %}
<box type="tip" seamless icon=":fas-link:">

**Quick Links:** [Practical Exam info](../../admin/tp-pe.html)
</box>
{% endif %}
