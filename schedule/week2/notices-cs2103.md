{% from "common/macros.njk" import embed_topic, timing_badge, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(2, "notices") }}

##### {{ timing_badge("by Thursday 2359") }}

* **Read weekly topics** allocated for this week. **Submit the post-lecture quiz** to test your knowledge of those topics. The quiz link will be emailed to you on the previous week's Friday.

* **Individual Project(iP)**: **Complete the eight iP increments** allocated for this week. See the [{{ show_as_tab("Project", icon_project) }}](project.html)&nbsp;tab for more info.

##### {{ timing_badge("sometime this week", "secondary") }}

* **Get connected**: Follow the 'Preparation' instructions of the following tools. 

<div class="indented-level3">
{{ embed_topic("../../admin/tools.md#communication", "Admin " + icon_embedding + " **Tools - Communication**", "-", "3") }}
</div>
