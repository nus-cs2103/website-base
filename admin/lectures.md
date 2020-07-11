{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("lectures") %}
<div id="main">

<img src="{{baseUrl}}/admin/images/Lecture photo.png" width="100%">

**Timing/venue**:

<include src="../_module-{{ module | lower }}/timetables.mbdf#lectures-s{{ S }}" inline />

<div tags="m--cs2103 m--cs2113">

Lectures start on time sharp and end around 15 minutes before official end time.
</div>

**Mode**:
* Will be done using Zoom. More information coming soon.


**Attendance**: Attendance for the ==first lecture is compulsory==.

**Handouts**: There are no handouts. All learning materials are organized around topics, are given in Web format, can be found in the [Textbook]({{baseUrl}}/se-book-adapted/index.html) section (organized by topics), and are also embedded in the {{ url_schedule }} (organized by order of coverage).

**Slides**: Our lecture slides are not suited for printing or to be used as a reference during the lecture/exams. They are only an aid for lecture delivery. Slides will be uploaded to LumiNUS *after* the lecture.

</div>

{% endcall %}
