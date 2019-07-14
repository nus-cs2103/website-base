{% from "common/macros.njk" import thumb with context %}
{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">


{{ thumb(1) }} **Review two PRs** created by your classmates. You will be notified separately which PRs to review.

<br/>

{{ thumb(2) }} **Add the following enhancements**. As before, do each enhancement in a separate branch and merge to the `master` branch only when ready (if you push incomplete features into the `master` branch, it can confuse others reviewing your PR).
<br>

<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 10: GUI**" var-fragment="text.md#level10" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Varargs** `[if applicable]`" var-fragment="extensions.mbdf#A-Varargs" />

{{ thumb(3) }} We recommend that at least some member of the team attempt the following.

<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-CheckStyle** `[optional]`" var-fragment="extensions.mbdf#A-CheckStyle" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Gradle** `[optional]`" var-fragment="extensions.mbdf#A-Gradle" />

<p/>

{{ thumb(4) }} **Add another extension** [to be specified nearer to the date]

<br>
</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-w04", show_main_text) }}