{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}
{% from "common/topics.njk" import panopto with context %}
<!--box type="info" header="****Next week's lecture (and the PE Dry Run) ==rescheduled!==****">

Heads up! As the following lecture (not this week's one) falls on a public holiday, it will be moved to the day after i.e., Saturday Apr 3rd 2-4pm.
==Attendance is compulsory==, as the lecture slot is also used for the Practical Exam Dry Run (<span class="text-danger">graded</span>).

</box-->
<box type="important" light>

Due to holidays, **this week's tutorial is released as a pre-recorded video**.

More info coming soon ...

<!--

{{ panopto("6c3474d0-0e20-4416-ad74-b13c0138d3a6", desc="Week 10 - Tutorial") }}

What you need to do:

1. Have a look at the three tutorial tasks given below in this page. It's best if you attempt them first, before you start watching the video.
1. Watch the video, and do the tasks as the video instructs you %%(e.g., answer in-video questions, post screenshots in workspace file)%%.
1. If you have doubts or questions, post in your tutorials MSTeam channel (and tag the tutor), or post in the course forum.

**:fas-clock: Period to watch the video** (to be ==counted for tutorial participation==): {{ get_date(date_w10_start, 1, time="")}} -- <span class="text-danger">{{ get_date(date_w10_start, 7, time="23:59")}}</span>
-->
</box>
{% if ped_week == '11' %}
<box type="info" header="****Next week's briefing (and the PE Dry Run)****">

Heads up! ==Attendance is compulsory== for the weekly briefing coming up on {{ get_date(date_w11_start, 4, time='') }}, as we use that time slot for the [Practical Exam Dry Run](../../admin/tp-ped.md) (<span class="text-danger">graded</span>).

</box>
<p/>
{% endif %}
