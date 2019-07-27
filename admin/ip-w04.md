{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Review some peer PRs
1. Add increments: `A-Gradle`,`A-CheckStyle`, `Level-10`, `A-Varargs`
1. Add another extension
{% endcall %}

<div id="body">


#### {{ thumb(1) }} Review some peer PRs

**Review two PRs** created by your classmates. You will be notified separately which PRs to review.

<br/>

#### {{ thumb(2) }} Add increments: `A-Gradle`,`A-CheckStyle`, `Level-10`, `A-Varargs`

**Add the following increments**. As before, do each enhancement in a separate branch and merge to the `master` branch only when ready (if you push incomplete features into the `master` branch, it can confuse others reviewing your PR).
<br>

<include src="dukeFragment.md" boilerplate var-header="**`A-Gradle`: Gradle**" var-fragment="extensions.mbdf#A-Gradle" />
<include src="dukeFragment.md" boilerplate var-header="**`A-CheckStyle`: CheckStyle**" var-tag="optional" var-fragment="extensions.mbdf#A-CheckStyle" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-10`: GUI**" var-fragment="text.md#level10" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Varargs`: Varargs**" var-tag="if-applicable" var-fragment="extensions.mbdf#A-Varargs" />


<p/>

#### {{ thumb(3) }} Add another extension

**Add another extension** [to be specified nearer to the date]

<br>
</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w04", show_main_text) }}