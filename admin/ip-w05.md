{% from "common/macros.njk" import thumb with context %}

{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

{{ thumb(1) }} Add the following deliverables, doing each in the following manner:
1. add the extension in a separate branch
1. push the branch to your fork
1. create PR within your fork (i.e., from the new branch, to the `master` branch)
1. merge the PR; you can try various merge options such as `Squash and Merge`, `Rebase and Merge`
1. sync your local clone with the fork

<include src="dukeFragment.md" boilerplate var-header="**`A-Assertions`**" var-fragment="extensions.mbdf#A-Assertions" />
<include src="dukeFragment.md" boilerplate var-header="**`A-CodeQuality`**" var-fragment="extensions.mbdf#A-CodeQuality" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Lambdas`**" var-tag="optional" var-fragment="extensions.mbdf#A-Lambdas" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Streams`**" var-tag="optional" var-fragment="extensions.mbdf#A-Streams" />

<p/>
{{ thumb(2) }} We recommend that at least some member of the team attempt the following.

<include src="dukeFragment.md" boilerplate var-header="**`A-Travis`: Travis**" var-tag="optional" var-fragment="extensions.mbdf#A-Travis" />

<p/>
{{ thumb(3) }} Add the extension [to be specified nearer to the date]

<p/>
</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-w05", show_main_text) }}