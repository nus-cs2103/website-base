{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 10: GUI**" var-fragment="text.md#level10" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Varargs**" var-fragment="extensions.mbdf#A-Varargs" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Lambdas**" var-fragment="extensions.mbdf#A-Lambdas" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Streams**" var-fragment="extensions.mbdf#A-Streams" />

Add extension [to be specified nearer to the date]

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-w04", show_main_text) }}