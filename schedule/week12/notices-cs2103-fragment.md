{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}
<!--box type="info" header="****This week's lecture (and the PE Dry Run) ==rescheduled!==****">

As this week's lecture falls on a public holiday, it will be moved to the day after i.e., Saturday Apr 3rd 2-4pm.
==Attendance is compulsory==, as the lecture slot is also used for the Practical Exam Dry Run (<span class="text-danger">graded</span>).

</box-->

{% if ped_week == '12' %}
<box type="info" header="****Next week's briefing (and the PE Dry Run)****">

Heads up! ==Attendance is compulsory== for the weekly briefing coming up on {{ get_date(date_w12_start, 4, time='') }}, as we use that time slot for the [Practical Exam Dry Run](../../admin/tp-ped.md) (<span class="text-danger">graded</span>).

</box>
<p/>
{% endif %}
