{% from "common/macros.njk" import thumb with context %}

{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

{{ thumb(1) }} Add the following feature in branch, push to fork, create PR in fork, self-review, merge, sync.

<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Assertions**" var-fragment="extensions.mbdf#A-Assertions" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-CodeQuality**" var-fragment="extensions.mbdf#A-CodeQuality" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Lambdas** `[optional]`" var-fragment="extensions.mbdf#A-Lambdas" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Streams** `[optional]`" var-fragment="extensions.mbdf#A-Streams" />

<p/>
{{ thumb(2) }} We recommend that at least some member of the team attempt the following.

<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Travis** `[optional]`" var-fragment="extensions.mbdf#A-Travis" />

<p/>
{{ thumb(3) }} Add the extension [to be specified nearer to the date]

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-w05", show_main_text) }}