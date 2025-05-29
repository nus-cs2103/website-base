{% from "common/macros.njk" import embed_topic, get_date, show_as_tab, timing_badge with context %}

<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="about-summary-tab">

<box type="info" header="++OK, I'm here. What am I looking at? What should I do next? ...++" icon=":fas-circle-info:">

**This is the <span class="text-primary">{{ show_as_tab('Summary', icon_tab_summary) }}</span> tab** of the weekly schedule page of this week. It contains a summary of the week, and announcements relevant to that week.

**In each week, you are expected to go through all the tabs for that week** (i.e., <span class="text-primary">{{ show_as_tab('Topics', icon_tab_topics) }}</span>, <span class="text-primary">{{ show_as_tab('Admin Info', icon_tab_admin_info) }}</span>, ...) given at the top of the weekly schedule page and follow the instructions in them. FYI, a **[full timeline](../schedule/timeline.html)** is available too.

**Before you move to other tabs, take note of any important information in this summary tab**, such as announcements relevant to this week{% if cs2103 %} and briefing videos to watch{% endif %}.

{% if not cs2103 %}This week, ==there are things for you to do before the upcoming {{ lecture_name }}== (refer the above tabs for details).{% endif %}

</box>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="semester-start">

<box type="tip" header="++Now, some announcements relevant to this week ...++" icon=":fas-bullhorn:">

* {% if cs2103 %}**There is no lecture in week 1**. In lieu of that, we are giving you a series of pre-recorded briefing videos (given in the panel below), so that you can get started early.<br>
  **Our first lecture will be on week 2** ({{ get_date(date_first_lecture, 7, time="1600-1800") }}), delivered in hybrid mode. {% else %}**Our first {{ lecture_name }}** will be on {{ get_date(date_first_lecture, time="") }}. {% endif %}
* **Our tutorials start on week 3.**
* **If you are bookmarking the course website in your browser**, bookmark the URL `{{ url_course_website }}` (i.e., the base URL, without pointing to any specific page).<br>
   Reason: This base URL will take you to the schedule page of the current week automatically.{% if cs2103 %}
* **[{{ course }}T Students]**: Of the many weekly sessions that appear under {{ course }}T, only two actually belong to {{ course }}T. Those are, the lecture slot on {{ day_lecture }} {{ time_t_lecture_start }}-{{ time_t_lecture_end }}, and the 1-hour tutorial slot. The other 3-hour slots belong to the CS2101 course.<br>
  ==All CS2101 sessions start in week 1==.{% endif %}
</box><p/>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="tutorial-start">

<box type="warning">
{% if semester=="AY2425S2" %}
We start tutorials this week. But due to CNY holidays, we will not follow the [regular tutorial timetable]({{ url_course_website }}/admin/tutorials.html#tutorial-timetable) this week. See the <span class="text-primary">{{ show_as_tab('Tutorial', icon_tab_tutorial) }}</span> tab for more details.
{% else %}
We start tutorials this week, starting from {{ get_date(date_w3_start, 2, time="") }}. The [tutorial timetable]({{ url_course_website }}/admin/tutorials.html#tutorial-timetable) is on the course website.
{% endif %}
</box>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="try-tutorial-task-before">

<box type="info">

You are encouraged to ==try this week's tutorial questions _before_ the actual tutorial==. Otherwise, we might not have enough time to finish all the questions during the tutorial hour.
</box>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
