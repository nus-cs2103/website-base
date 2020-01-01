{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}
{% from "admin/ip-tasks.mbdf" import fininsh_leftover_tasks, create_pr_to_upstream, do_as_parallel_branches with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Create a PR to the upstream repo
1. Do as parallel branches: `Level-7` and `Level-8`
1. Do increments `A-MoreOOP`, `A-Packages`, `A-JUnit`, `A-Jar`
1. Do as parallel branches: `A-JavaDoc`, `A-CodingStandard`, `Level-9`
{% endcall %}

<div id="body">

In this week, we try to practice git branching as we do the iP.

{{ fininsh_leftover_tasks(0) }}

{{ create_pr_to_upstream(1) }}

{{ do_as_parallel_branches(2) }}

#### {{ thumb(3) }} Do increments `A-MoreOOP`, `A-Packages`, `A-JUnit`, `A-Jar`

As in the previous week, commit, tag, and push, as you do the following increments in the `master` branch (no need to use separate branches).
<include src="dukeFragment.md" boilerplate var-header="**`A-MoreOOP`: More OOP**" var-fragment="extensions.mbdf#A-MoreOOP" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Packages`: Java Packages**" var-tag="optional" var-fragment="extensions.mbdf#A-Packages" />
<include src="dukeFragment.md" boilerplate var-header="**`A-JUnit`: JUnit Testing**" var-fragment="extensions.mbdf#A-JUnit" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Jar`: JAR file**" var-fragment="extensions.mbdf#A-Jar" />

<p/>

#### {{ thumb(4) }} Do as parallel branches: `A-JavaDoc`, `A-CodingStandard`, `Level-9`

As in the step 1 above, implement these three increments as three parallel branches first (branch names: `branch-A-JavaDoc`, `branch-A-CodingStandard`, `branch-Level-9`), and then merge them one-by-one. Hopefully, you will encounter some merge conflicts so that you get to practice de-conflicting branches.
<include src="dukeFragment.md" boilerplate var-header="**`A-JavaDoc`: JavaDoc**" var-fragment="extensions.mbdf#A-JavaDoc" />
<include src="dukeFragment.md" boilerplate var-header="**`A-CodingStandard`: Coding Standard**" var-fragment="extensions.mbdf#A-CodingStandard" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-9`: Find**" var-fragment="text.md#Level-9" />

<p/>

<br>
</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w03", show_main_text) }}