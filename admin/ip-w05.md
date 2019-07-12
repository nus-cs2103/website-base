{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Assertions**" var-fragment="extensions.mbdf#A-Assertions" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-CodeQuality**" var-fragment="extensions.mbdf#A-CodeQuality" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Gradle**" var-fragment="extensions.mbdf#A-Gradle" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Travis**" var-fragment="extensions.mbdf#A-Travis" />

Add extension [to be specified nearer to the date]

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-w05", show_main_text) }}