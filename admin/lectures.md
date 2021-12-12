{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("lectures") %}
<div id="main">

<img src="{{baseUrl}}/admin/images/Lecture photo.png" width="100%">

****Timing/venue****:

<include src="../_module-{{ module }}/timetables.mbdf#lectures-s{{ S }}" />

<div tags="m--tic4001 m--tic4002" class="indented">

**The lecture+tutorial slot ({{ day_lecture }} 6.30pm-9.30pm) will be repurposed** as follows, due to this being a 100% project module:

* **6.30-7pm**: No formal activities. Work with team members and consult instructors (using the MS Teams app) if you need help with the previous week's tasks.
* **7-7.30pm**: Weekly briefing.
* **7-30-9.30pm**:
  * Do the lecture activities (if any) or work with team members to do weekly project activities.
  * The tutor will observe or get involved in your team's work as necessary.
  * You may approach instructors (using the MS Teams app) for help during this period.
  * From week 3, we'll be scheduling team meetings during this period, for the team supervisor to discuss the team project progress with you.
</div>

<div tags="m--cs2103 m--cs2113">

Lectures start on time sharp and end around 10 minutes before official end time.
</div>

****Mode****:
* Will be done using Zoom. Zoom link to the lecture can be found on LumiNUS.
* You need to register first before you receive the actual session link.

<div tags="m--cs2113 m--cs2103 m--tic4001 m--tic4002">

* Some topics come with pre-recorded lecture videos.
</div>

<div id="tip-about-lecture-videos" class="indented">

<box type="tip" seamless>

##### Tips for watching lecture videos

* ==You can watch video lectures at faster speeds== (`x1.25` or even `x1.5`) to save time.
* Lecture videos are distributed from within LumiNUS -> Multimedia channel.
</box>
</div>


****Attendance****: Attendance for the ==first lecture is compulsory==.

****Handouts****: There are no handouts. All learning materials are organized around topics, are given in Web format, can be found in the [Textbook]({{baseUrl}}/se-book-adapted/index.html) section (organized by topics), and are also embedded in the {{ url_schedule }} (organized in the order they are covered).

****Slides****: Our lecture slides are not suited for printing or to be used as a reference during the lecture/exams. They are only an aid for lecture delivery. Slides will be uploaded to LumiNUS *after* the lecture.

</div>

{% endcall %}
