{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Submit the quiz

{{ icon_project }} **Project:**
1. Implement increments `Level-7`, `A-MoreOOP`, `A-Packages`
{% endcall %}

<!-- ==================================================================================================== -->
{{ heading_project }}
<div id="project">

#### {{ thumb(1) }}  Implement increments `Level-7`, `A-MoreOOP`, `A-Packages`

<div class="indented">
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-7`: Save**" var-fragment="text.md#Level-7" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-MoreOOP`: More OOP**" var-fragment="extensions-fragment.md#A-MoreOOP" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-Packages`: Java Packages**" var-fragment="extensions-fragment.md#A-Packages" />


</div>
</div>