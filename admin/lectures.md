{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("lectures") %}
<div id="main">

<img src="{{baseUrl}}/admin/images/Lecture photo.png" width="100%">

****Timing/venue****:

<include src="../_module-{{ module }}/timetables-fragment.md#lectures-s{{ S }}" />

<div tags="m--tic4001 m--tic4002" class="indented">

**The lecture+tutorial slot ({{ day_lecture }} 6.30pm-9.30pm) will be repurposed** as follows, due to this being a 100% project module:

* **6.30-7pm**: No formal activities. Work with team members and consult instructors (using the MS Teams app) if you need help with the previous week's tasks.
* **7-7.30pm**: Weekly briefing, done via Zoom. The Zoom link can be found in [LumiNUS WebLinks](https://luminus.nus.edu.sg/modules/{{ luminus_module_id }}/details/web-links).
* **7.30-9.30pm**:
  * Do the lecture activities (if any) or weekly project activities.
  * You may approach instructors (using the MS Teams app) for help during this period.
  * After the team project has started, we'll be scheduling team meetings during this period, for the teaching team to discuss the project progress with you.<br>
    These meetings will be done through MS Teams app. ==If your team prefer face-to-face team meetings instead==, let us know in advance so that the teaching team can meet your team in COM1-02-13 (Video Conference Room) instead.
</div>

<div tags="m--cs2103 m--cs2113">

Lectures start on time sharp and end around 10-15 minutes before official end time.
</div>

****Mode****:
{% if cs2103 or cs2113 %}
* Lectures will be conducted on-campus (i.e., F2F) 
{% else %}
* As mentioned above, the lecture briefing will be delivered via Zoom (see [LumiNUS WebLinks](https://luminus.nus.edu.sg/modules/{{ luminus_module_id }}/details/web-links) for the Zoom link).
{% endif %}

<div tags="m--cs2103 m--cs2113 m--tic4001 m--tic4002">

* Some topics come with pre-recorded lecture videos.
</div>

<div id="tip-about-lecture-videos" class="indented">

<box type="tip" seamless>

##### Tips for watching lecture videos

* ==You can watch video lectures at faster speeds== (`x1.25` or even `x1.5`) to save time.{% if cs2113 %}
* Lecture videos are distributed from within LumiNUS -> Multimedia channel.{% else %}
* Lecture videos require NUSNET login.{% endif %}
</box>
</div>


****Attendance****: Attendance for the ==first lecture is compulsory== (i.e., attend online or watch the recording).

****Handouts****: There are no handouts. All learning materials are organized around topics, are given in Web format, can be found in the [Textbook]({{baseUrl}}/se-book-adapted/index.html) section (organized by topics), and are also embedded in the {{ url_schedule }} (organized in the order they are covered).
{% if not tic4001 and not tic4002 %}

****Slides****: Our lecture slides are not suited for printing or to be used as a reference during the lecture/exams. They are only an aid for lecture delivery. Slides will be uploaded to LumiNUS ***after*** the lecture.
{% endif %}
</div>

{% endcall %}
