{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import embed_topic, show_admin_sections_to_read, show_as_tab, timing_badge with context %}
{% from "common/admin.njk" import topics, policies, faqs, admin_topics_to_read, show_admin_summary with context %}

{{ show_week_pagetop(2, "admin") }}

{% call show_admin_summary() %}
1. Submit post-lecture quiz {{ timing_badge("by Thursday 2359") }}
1. Get connected with the module's communication channels {{ timing_badge("by this week", "secondary") }}
{% endcall %}

<div id="additional">

##### {{ timing_badge("by Thursday 2359") }}

* **Read weekly topics** allocated for this week. **Submit the post-lecture quiz** to test your knowledge of those topics. The quiz link will be emailed to you on the previous week's Friday.


##### {{ timing_badge("by this week", "secondary") }}

* **Get connected**: Follow the 'Preparation' instructions of the following tools.

<div class="indented-level3">
{{ embed_topic("../../admin/tools.md#communication", "Admin " + icon_embedding + " **Tools - Communication**", "-", "3") }}
</div>

</div>


{{ show_admin_sections_to_read(topics, policies, faqs, admin_topics_to_read.week2, is_flat=false ) }}
