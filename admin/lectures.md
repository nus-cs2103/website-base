{% macro show_main_text() %}
<div id="main">

<img src="{{baseUrl}}/admin/images/Lecture photo.png" width="100%">

**Timing/venue**: 

Semester               | Module   | Venue            | Time 
---------------------- | -------- | ---------------- |---------------
Semester 1 (Aug-Nov)   | CS2103   | LT19             | **1200**-1400
Semester 1 (Aug-Nov)   | CS2103T  | ICube Auditorium | **1600**-1800
Semester 2 (Jan-April) | CS2103/T | ICube Auditorium | **1400**-1600

Lectures start on time sharp and end around 15 minutes before official end time.

**Attendance**: Attendance for the ==first lecture is compulsory==.

**Handouts**: There are no handouts. All learning materials are organized around topics, are given in Web format, can be found in the [Textbook]({{baseUrl}}/se-book-adapted/index.html) section (organized by topics), and are also embedded in from the {{ schedule_link }} (organized by order of coverage).

**Slides**: Our lecture slides are not suited for printing or to be used as a reference during the lecture/exams. They are only an aid for lecture delivery. Slides will be uploaded to LumiNUS *after* the lecture.


</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("lectures", show_main_text) }}