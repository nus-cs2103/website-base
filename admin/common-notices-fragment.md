{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}

<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="about-summary-tab">

<box type="info" dismissible>

A summary of the week, and announcements relevant to that week, will appear in this <span class="text-primary">{{ show_as_tab('Summary', icon_tab_summary) }}</span> tab.

**In each week**, go through all the tabs for that week (i.e., <span class="text-primary">{{ show_as_tab('Topics', icon_tab_topics) }}</span>, <span class="text-primary">{{ show_as_tab('Admin Info', icon_tab_admin_info) }}</span>, ...) given at the top of this page and follow the instructions in them. FYI, a **[full timeline](../schedule/timeline.html)** is available too.

This week, ==there are things for you to do before the upcoming lecture== (refer the above tabs for details).

</box>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="semester-start">

<box type="tip">

* **Our first lecture** will be on {{ get_date(date_first_lecture, time="") }}. It will be fully online. Subsequent lectures will be hybrid.
* **Our tutorials** start on week 3.
* **[{{ course }}T Students]**: Of the many weekly sessions that appear under {{ course }}T, only two actually belong to {{ course }}T. Those are, the lecture on {{ day_lecture }} {{ time_t_lecture_start }}-{{ time_t_lecture_end }}, and the 1-hour tutorial slot. The other two 2-hour slots belong to the CS2101 course.<br>
  ==CS2101 tutorials start in week 1==.
</box><p/>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="tutorial-start">

<box type="warning" dismissible>

We start tutorials this week. The [tutorial time table]({{ url_course_website }}/admin/tutorials.html#tutorial-timetable) is on the course website.
</box>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="try-tutorial-task-before">

<box type="info">

You are encouraged to ==try this week's tutorial questions _before_ the actual tutorial==. Otherwise we might not have enough time to finish all the questions during the tutorial hour.
</box>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
