{% from "common/macros.njk" import thumb with context %}
{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">


{{ thumb(1) }} **Review two PRs** created by your classmates. You will be notified separately which PRs to review.

<br/>

{{ thumb(2) }} **Add the following enhancements**.
<br>

<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 10: GUI**" var-fragment="text.md#level10" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Varargs**" var-fragment="extensions.mbdf#A-Varargs" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Lambdas**" var-fragment="extensions.mbdf#A-Lambdas" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Streams**" var-fragment="extensions.mbdf#A-Streams" />

<p/>

{{ thumb(3) }} **Add another extension** [to be specified nearer to the date]

<br>
</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-w04", show_main_text) }}