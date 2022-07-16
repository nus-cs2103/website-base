{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Submit the quiz

{{ icon_project }} **Project:**
1. Improve the individual feature (or add another)
1. Implement increments `Level-10`<span class="badge badge-pill badge-secondary">optional</span>, `A-Assertions`, `A-Jar`
{% endcall %}

<!-- ==================================================================================================== -->
{{ heading_project }}
<div id="project">

#### {{ thumb(1) }} Improve the individual feature (or add another)

* Use this week to improve the individual feature you added in the previous week. Alternatively, you can add another individual feature (i.e., one of the two remaining options from the previous week).

#### {{ thumb(2) }} Implement increments `Level-10`<span class="badge badge-pill badge-secondary">optional</span>, `A-Assertions`, `A-Jar`
<div class="indented">
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-10`: GUI**" var-tag="optional" var-fragment="text.md#Level-10" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-Assertions`: Assertions**" var-fragment="extensions.mbdf#A-Assertions" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-Jar`: JAR File**" var-fragment="extensions.mbdf#A-Jar" />

</div>
</div>
