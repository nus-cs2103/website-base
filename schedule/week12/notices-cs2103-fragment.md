{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}
<!--box type="info" header="****This week's lecture (and the PE Dry Run) ==rescheduled!==****">

As this week's lecture falls on a public holiday, it will be moved to the day after i.e., Saturday Apr 3rd 2-4pm.
==Attendance is compulsory==, as the lecture slot is also used for the Practical Exam Dry Run (<span class="text-danger">graded</span>).

</box-->

{% if ped_week == '12' %}
<box type="info" header="****PE Dry Run coming up!****">

**[Practical Exam Dry Run](../../admin/tp-ped.md) is coming up** on {{ get_date(date_w12_start, 4, time='1200-1800') }} (<span class="text-danger">graded</span>).

</box>
<p/>
{% endif %}
{% if pe_week == '12' %}
<box type="tip" seamless icon=":fas-link:">

**Quick Links:** [Practical Exam info](../../admin/tp-pe.html)
</box>
{% endif %}
