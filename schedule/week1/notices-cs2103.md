{% from "common/macros.njk" import embed_topic, timing_badge, show_as_tab with context %}
{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(1, "notices") }}

##### {{ timing_badge("before the lecture") }}
* **Read prerequisite topics** allocated for week 1. **Submit week 1 quiz** to test your knowledge of those topics. The quiz link will be emailed to you by Monday.

* **Set up the tools**: Follow the 'Preparation' instructions of the following tools. 

<div class="indented-level3">
{{ embed_topic("../../admin/tools.md#ide", "Admin " + icon_embedding + " **Tools - IDE**", "-", "2") }}
{{ embed_topic("../../admin/tools.md#rcs", "Admin " + icon_embedding + " **Tools - RCS**", "-", "2") }}
{{ embed_topic("../../admin/tools.md#github", "Admin " + icon_embedding + " **Tools - GitHub**", "-", "2") }}
</div>

##### {{ timing_badge("Friday afternoon", "info") }}

* Attend the Week 1 lecture (Week 1 lecture is ==**compulsory**==).
  * Bring your Computer to the lecture. Some lecture activities will require you to use it.


##### {{ timing_badge("by Friday 2359") }}
* **Submit the pre-module survey ==(compulsory)==**<br>
  _Pre-Module Survey_ will be available on LumiNUS **Week 1 Monday - Friday 2359**. %%We need all of you to submit it because it tells us some important information about you, especially your GitHub username.%%

##### {{ timing_badge("within the week", "secondary") }} 

* **See the [{{ show_as_tab("Admin", icon_info) }}](admin.html)&nbsp;tab (above)** for some important admin info you need to know at the start of the semester.
