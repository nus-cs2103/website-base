{% from "common/macros.njk" import embed_topic, timing_badge, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(3, "notices") }}

<box type="warning">

* The **deadline to achieve weekly tasks is the midnight before your tutorial**, unless mentioned otherwise. Our scripts that detect your work run at midnight and only the work that's done by midnight will be eligible for marks (for cases where the task is graded).
* We start tutorials this week. The [tutorial time table]({{ module_website }}/admin/tutorials.html#tutorial-timetable) is on the module website.
</box>

##### {{ timing_badge("by <tooltip content='2359 immediately _before_ your tutorial'>weekly deadline</tooltip>") }}

* **Post-lecture quiz**: As usual, read weekly topics allocated for this week. Submit the post-lecture quiz to test your knowledge of those topics. The quiz link will be emailed to you on the previous week's Friday.
* **Individual Project(iP)**: Complete the iP increments allocated for this week. See the [{{ show_as_tab("Project", icon_project) }}](project.html)&nbsp;tab for more info.

##### {{ timing_badge("in the tutorial", "info") }}

* **CS2103 students only:** ==forming project teams will happen at the _start_ of this week's tutorial==. See the [{{ show_as_tab("Tutorial", icon_tutorial) }}](project.html)&nbsp;tab for more info.
