{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Submit weekly exercises
1. Submit the quiz

{{ icon_project }} **Project:**
1. Implement increments `Level-6`, `A-Enums` <span class="badge rounded-pill bg-secondary">if-applicable</span>
{% endcall %}

<!-- ==================================================================================================== -->
{{ heading_project }}
<div id="project">

#### {{ thumb(1) }} Implement increments `Level-6`, `A-Enums` <span class="badge rounded-pill bg-secondary">if-applicable</span>

<div class="indented">
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-6`: Delete**" var-fragment="text.md#Level-6" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-Enums`: Enums**" var-tag="if-applicable" var-fragment="extensions-fragment.md#A-Enums" />
</div>
</div>
