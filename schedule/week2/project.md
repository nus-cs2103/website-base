{% from "common/macros.njk" import embed_topic, thumb with context %}
{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(2, "project") }}

We'll be starting the individual project (iP) this week.

<box type="important">

* Please try to **follow instructions closely**. If you deviate, our grading scripts will not be able to detect your work.
* The deadline to complete weekly project work is the **midnight before your tutorial day** %%e.g., if your tutorial is on Thursday, you should finish your project work by Wednesday 23.59%%.
* You may have to **go through the weekly topics before attempting weekly iP tasks** as the knowlege from those topics may be needed to complete the iP tasks.

</box>

{{ thumb(0) }} Read the following two sections, if you haven't done so already:

<div class="indented">

{{ embed_topic("../../admin/ip-overview.md#main", "Admin " + icon_embedding + " **iP - Overview**", "ipW02-overview", "3") }}
{{ embed_topic("../../admin/ip-grading.md#main", "Admin " + icon_embedding + " **iP - Grading**", "ipW02-overview", "1") }}
</div>

<include src="../../admin/ip-w02.md#body" />
