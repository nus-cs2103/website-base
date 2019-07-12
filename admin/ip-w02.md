{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 1: Greet, Echo, Exit**" var-fragment="text.md#level1" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 2: Add, List**" var-fragment="text.md#level2" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 3: Mark as Done**" var-fragment="text.md#level3" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 4: ToDo, Event, Deadline**" var-fragment="text.md#level4" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-TextUiTesting**" var-fragment="extensions.mbdf#A-TextUiTesting" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 5: Handle Incorrect Inputs**" var-fragment="text.md#level5" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 6: Delete**" var-fragment="text.md#level6" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Enums**" var-fragment="extensions.mbdf#A-Enums" />

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-w02", show_main_text) }}