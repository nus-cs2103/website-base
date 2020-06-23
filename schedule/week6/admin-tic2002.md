{% from "schedule/index.md" import show_week_pagetop with context%}
{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}

{{ show_week_pagetop(6, "admin") }}

{% call show_admin_summary() %}
1. Submit weekly exercises
1. Implement increment `Level-5`
{% endcall %}

{{ thumb(1) }} Submit weekly exercises

* As usual.

{{ thumb(2) }} Implement increment `Level-5`

<div class="indented">
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-5`: Handle Errors**" var-fragment="text.md#Level-5" />
</div>
