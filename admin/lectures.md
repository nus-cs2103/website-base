{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("lectures") %}
<div id="main">

<div tags="m--cs2113">
<pic eager src="{{baseUrl}}/admin/images/Lecture photo.png" width="100%"></pic>
</div>

<div tags="m--cs2103">

<p class="lead text-secondary"><em>Weekly briefing</em> are short weekly sessions (>1hr) conducted by the course lecturer(s) to brief you about the upcoming week.</p>

****This course does not have _lectures_****, as the course is using the _blended learning_ mode. Course content are delivered as an online textbook accompanied by pre-recorded videos, instead of using lectures as the main method of content delivery. We still have a lecture slot/venue though.

**In most weeks we use the lecture slot/venue for _weekly briefings_.** In some weeks we use it for important events such as the practical exam.
</div>

****Timing/venue****: <include src="../_course-{{ course }}/timetables-fragment.md#lectures-s{{ S }}" inline/>

<div tags="m--cs2113">

* The lecture recording will be made available later during the same day.
* Lectures start on time sharp and end around 10-15 minutes before official end time.
</div>

****Mode****:
{% if cs2103 %}
* The first {{ lecture_name }} will be done using Zoom. The Zoom link will be available in [Canvas course homepage]({{ url_canvas_home }}). You can attend the live Zoom meeting or watch the recording later.
* We expect to switch to the _hybrid_ mode (i.e., you can attend F2F or via Zoom or watch the recording later) from the 2nd week onwards.
{% elseif cs2113 %}
* Lectures will be conducted on-campus (i.e., F2F)
{% else %}
* As mentioned above, the {{ lecture_name }} will be delivered via Zoom (see [Canvas course homepage]({{ url_canvas_home }}) for the Zoom link).
{% endif %}

<div tags="m--cs2103">

****Scope****: A weekly briefing is usually about 1 hour, and aims to,

* **recap** the past week, clarify common doubts
* **preview** the next week
* **motivate** you to tackle the weekly tasks coming up
* **contextualize** various 'moving parts' of the course and keep you anchored to the 'big picture'

****Slides****: Briefing slides will be uploaded to Canvas *after* the briefing. Note that those slides are not suited for printing or to be used as a reference during the lecture/exams. They are only an aid for briefing delivery.

****Attendance****: Attendance for the ==first weekly briefing is compulsory== (i.e., you may join the Zoom meeting or watch the recording later).<br>
 Subsequent weekly briefings are optional to attend. You are free to speed-watch the recording to save time (instead of joining live) or skip them altogether (if you are already saturated by the rest of the course activities).

</div>
<div tags="m--cs2113">

****Attendance****: Attendance for the ==first lecture is compulsory== (i.e., attend online or watch the recording).

****Handouts****: There are no lecture handouts. All learning materials are organized around topics, are given in Web format, can be found in the [Textbook]({{baseUrl}}/se-book-adapted/index.html) section (organized by topics), and are also embedded in the {{ url_schedule }} (organized in the order they are covered).

****Slides****: Our lecture slides are not suited for printing or to be used as a reference during the lecture/exams. They are only an aid for lecture delivery. Slides will be uploaded to Canvas *after* the lecture.

</div>

</div>
{% endcall %}
