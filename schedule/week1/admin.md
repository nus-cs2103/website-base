{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import embed_topic, show_admin_sections_to_read, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(1, "admin") }}

<box type="info" dismissible>

Admin info relevant to the week's will appear in this tab.
</box>

{% call show_admin_summary() %}
1. Submit pre-lecture quiz {{ timing_badge("before the lecture") }}
1. Set up the tools {{ timing_badge("before the lecture") }}
1. Attend the lecture
1. Submit the pre-module survey {{ timing_badge("by Friday 2359") }}
1. Learn how to use the module website
1. Learn about the module
{% endcall %}

<div id="additional">

#### {{ thumb(1) }} Submit pre-lecture quiz {{ timing_badge("before the lecture", "secondary") }}

* **Read prerequisite topics** allocated for week 1. **Submit week 1 quiz** to test your knowledge of those topics. The quiz link will be emailed to you by Monday.


#### {{ thumb(2) }} Set up the tools {{ timing_badge("before the lecture", "secondary") }}

  * Follow the <span class="border" style="color:purple">&nbsp;**:fas-hard-hat: Preparation**&nbsp;</span> instructions of the following tools.

<div class="indented-level2">
{{ embed_topic("../../admin/tools.md#ide", "Admin " + icon_embedding + " **Tools - IDE**", "-", "2") }}
{{ embed_topic("../../admin/tools.md#rcs", "Admin " + icon_embedding + " **Tools - RCS**", "-", "2") }}
{{ embed_topic("../../admin/tools.md#github", "Admin " + icon_embedding + " **Tools - GitHub**", "-", "2") }}
</div>

#### {{ thumb(3) }} Attend the lecture
* Attend the Week 1 lecture (Week 1 lecture is ==**compulsory**==).
* Bring your computer to the lecture. Some lecture activities will require you to use it.

#### {{ thumb(4) }} Submit the pre-module survey {{ timing_badge("by Friday 2359", "secondary") }}
* **Submit the pre-module survey ==(compulsory)==**<br>
  _Pre-Module Survey_ will be available on LumiNUS **Week 1 Monday - Friday 2359**. %%We need all of you to submit it because it tells us some important information about you, especially your GitHub username.%%

#### {{ thumb(5) }} Learn how to use the module website

* **See the** [{{ show_as_tab("Admin Info", icon_info) }}](admin.html)&nbsp;**tab (above)** for some important admin info you need to know at the start of the semester.
<div class="indented-level2">

<panel type="danger" header="**Admin {{icon_embedding }} Using this website [essential info]** :glyphicon-star:" minimized>
  <include src="../../admin/usingThisWebsite.md#essential"/>
</panel><p/>
<panel type="info" header="**Admin {{icon_embedding }} Using this website [more info]** :glyphicon-star::glyphicon-star::glyphicon-star:" minimized>
  <include src="../../admin/usingThisWebsite.md#more"/>
</panel><p/>
<panel type="warning" header="**Admin {{icon_embedding }} Weekly schedule** :glyphicon-star::glyphicon-star:" minimized>
  <include src="../../admin/weeklySchedule.md#main"/>
</panel><p/>
<panel type="success" header="**Admin {{icon_embedding }} Module overview** :glyphicon-star::glyphicon-star::glyphicon-star::glyphicon-star:" minimized>
  <include src="../../admin/moduleOverview.md#main"/>
</panel><p/>
</div>

</div>

#### {{ thumb(6) }} Learn about the module

{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week1, is_flat=false ) }}

