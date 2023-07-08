{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("lectures") %}
<div id="main">

<pic src="{{baseUrl}}/admin/images/Lecture photo.png" width="100%"></pic>

****Timing/venue****: <include src="../_course-{{ course }}/timetables-fragment.md#lectures-s{{ S }}" inline/>

<div tags="m--tic4001 m--tic4002" class="indented">

**The lecture+tutorial slot ({{ day_lecture }} 6.30pm-9.30pm) will be repurposed** as follows, due to this being a 100% project course:

* **6.30-7pm**: No formal activities. Work with team members and consult instructors (using the MS Teams app) if you need help with the previous week's tasks.
* **7-7.30pm**: Weekly briefing, done via Zoom. The Zoom link can be found in [Canvas course homepage]({{ url_canvas_home }}).
* **7.30-9.30pm**:
  * Do the lecture activities (if any) or weekly project activities.
  * You may approach instructors (using the MS Teams app) for help during this period.
  * After the team project has started, we'll be scheduling team meetings during this period, for the teaching team to discuss the project progress with you.<br>
    These meetings will be done through MS Teams app.
</div>

<div tags="m--cs2103 m--cs2113">

* The lecture recording will be made available later during the same day.
* Lectures start on time sharp and end around 10-15 minutes before official end time.
</div>

****Mode****:
{% if cs2103 %}
* The first lecture will be done using Zoom. The Zoom link will be available in [Canvas course homepage]({{ url_canvas_home }}). You can attend the live Zoom lecture or watch the recording later.
* We expect to switch to the _hybrid_ mode (i.e., you can attend F2F or via Zoom or watch the recording later) from the 2nd lecture onwards.
{% elseif cs2113 %}
* Lectures will be conducted on-campus (i.e., F2F)
{% else %}
* As mentioned above, the lecture briefing will be delivered via Zoom (see [Canvas course homepage]({{ url_canvas_home }}) for the Zoom link).
{% endif %}

<div tags="m--cs2103 m--cs2113 m--tic4001 m--tic4002">

* Some topics come with pre-recorded lecture videos.
</div>

<div id="tip-about-lecture-videos" class="indented">

<box type="tip" seamless>

##### Tips for watching lecture videos

* ==You are recommended to watch <span class="badge rounded-pill bg-danger">++{{ icon_video }} Videos++</span> provided at faster speeds== (`x1.25` or even `x1.5`) to save time.{% if cs2113 %}
* Lecture videos are distributed via Canvas.{% else %}
* You'll need to use your NUSNET login to access them.{% endif %}
</box>
</div>


****Attendance****: Attendance for the ==first lecture is compulsory== (i.e., attend online or watch the recording).

****Handouts****: There are no lecture handouts. All learning materials are organized around topics, are given in Web format, can be found in the [Textbook]({{baseUrl}}/se-book-adapted/index.html) section (organized by topics), and are also embedded in the {{ url_schedule }} (organized in the order they are covered).
{% if not tic4001 and not tic4002 %}

****Slides****: Our lecture slides are not suited for printing or to be used as a reference during the lecture/exams. They are only an aid for lecture delivery. Slides will be uploaded to Canvas *after* the lecture.
{% endif %}

<box type="info"  header="A caveat about your expectations from the lecture" tags="m--cs2103" light>

In a traditional course, the lecture is the _primary_ means of content delivery. However, {{ course_pair }} is delivered in the _blended learning_ mode, and accordingly, the contents are delivered primarily via the online textbook and pre-recorded videos that you can consume at your own pace.

Hence, ==the lecture is only a _complementary_ component== that aims to,
* **recap** the past week, clarify common doubts
* **preview** the next week
* **motivate** you to tackle the weekly tasks coming up
* **contextualize** various 'moving parts' of the course and keep you anchored to the 'big picture'

Given that lectures are complementary, you are free to speed-watch the recording to save time (instead of attending the live lecture) or skip them altogether (if you are already saturated by the rest of the course activities). That said, live attendance (F2F or via Zoom) is recommended as it makes it easier to follow the same schedule every week.
</box>
</div>

{% endcall %}
