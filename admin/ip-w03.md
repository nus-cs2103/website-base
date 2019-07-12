{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 7: Save**" var-fragment="text.md#level7" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 8: Dates and Times**" var-fragment="text.md#level8" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-MoreOOP**" var-fragment="extensions.mbdf#A-MoreOOP" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 9: Find**" var-fragment="text.md#level9" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-JUnit**" var-fragment="extensions.mbdf#A-JUnit" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Packages**" var-fragment="extensions.mbdf#A-Packages" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-JavaDoc**" var-fragment="extensions.mbdf#A-JavaDoc" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-CodingStandard**" var-fragment="extensions.mbdf#A-CodingStandard" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Jar**" var-fragment="extensions.mbdf#A-Jar" />

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-w03", show_main_text) }}