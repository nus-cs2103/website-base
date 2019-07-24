{% from "common/macros.njk" import embed_topic, timing_badge, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(3, "notices") }}

##### {{ timing_badge("by <tooltip content='2359 immediately _before_ your tutorial'>weekly deadline</tooltip>") }}

* We start formal tutorials this week. The [tutorial time table]({{ module_website }}/admin/tutorials.html#tutorial-timetable) is on the module website.

* Note that the official {{ icon_deadline }} **deadline to achieve weekly project tasks is the midnight before your tutorial**. Our scripts that detect your work run at midnight and only the work that's done by midnight will be eligible for marks (for cases where the task is graded).

**CS2103 students only:**<br>

* **forming project teams will happen at the _start_ of this week's tutorial**; please try to arrive on time. If you are not there at the team forming time and others in the class are unaware which team you wanted to be in, we'll have to put you into a team randomly.