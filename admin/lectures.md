{% macro show_main_text() %}
<div id="main">

<img src="{{baseUrl}}/admin/images/Lecture photo.png" width="100%">

**Timing/venue**: 

Semester | Venue | Time 
-------- | ----- | ----
Semester 1 (Aug-Nov) | ICube Auditorium | **1600**-1800
Semester 2 (Jan-April) | ICube Auditorium | **1600**-1800

Lectures start on time sharp and end around 15 minutes before official end time.

<panel header="**Clarification: {{ module }}T Lecture Timinig** :exclamation: %%(not applicable to {{ module }})%%"> 

{{ module }}T lectures are same as that for {{ module }}. Please ignore the CS2101 session scheduled at the same slot. That is a dummy slot used to work around a limitation on the CORS IT system. %%The system doesn't allow lectures of two modules to be scheduled in the same venue at the same time.%%
  
</panel><p/>

**Attendance**: Attendance for the ==first lecture is compulsory==.

**Webcast**: All lectures will be webcast. However, some things are not captured well in the webcast recording. You are advised to treat the webcast as a 'backup' for you to catch up anything missed during the lecture. ==Webcast lectures will be available on LumiNUS instead fo IVLE== (IVLE no longer supports webcasts).

**Handouts**: There are no handouts. All learning materials are organized around learning outcomes (not lectures or topics), are given in Web format, and can be found in the [Textbook]({{baseUrl}}/se-book-adapted/index.html) section and are also hyperlinked from the {{ schedule_link }}.

**Slides**: Our lecture slides are not suited for printing or using as a reference during the lecture/exams. They are only an aid for lecture delivery. Slides will be uploaded *after* the lecture (link available in the {{ schedule_link }}).


</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("lectures", show_main_text) }}