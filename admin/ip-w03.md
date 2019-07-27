{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Do as parallel branches: `Level-7` and `Level-8`
1. Do increments `A-MoreOOP`, `A-Packages`, `A-JUnit`, `A-Jar`
1. Do as parallel branches: `A-JavaDoc`, `A-CodingStandard`, `Level-9`
1. Create a PR to the upstream repo
{% endcall %}

<div id="body">

In this week, we try to practice git branching as we do the iP.

#### {{ thumb(1) }} Do as parallel branches: `Level-7` and `Level-8`

Do Level 7 in a branch named `branch-level7`. Without merging that branch, go back to the `master` branch and implement Level 8 in a separate branch named `branch-level8`. Now, go back to the `master` branch and merge the two branches one after the other. As before, tag the commit (in the `master` branch, after merging) that achieves the respective deliverable, and push to your fork.

<include src="dukeFragment.md" boilerplate var-header="**`Level-7`: Save**" var-fragment="text.md#level7" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-8`: Dates and Times**" var-fragment="text.md#level8" />

<p/>

#### {{ thumb(2) }} Do increments `A-MoreOOP`, `A-Packages`, `A-JUnit`, `A-Jar`

As in the previous week, commit, tag, and push, as you do the following increments in the `master` branch (no need to use separate branches).
<include src="dukeFragment.md" boilerplate var-header="**`A-MoreOOP`: More OOP**" var-fragment="extensions.mbdf#A-MoreOOP" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Packages`: Java Packages**" var-tag="optional" var-fragment="extensions.mbdf#A-Packages" />
<include src="dukeFragment.md" boilerplate var-header="**`A-JUnit`: JUnit Testing**" var-fragment="extensions.mbdf#A-JUnit" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Jar`: JAR file**" var-fragment="extensions.mbdf#A-Jar" />

<p/>

#### {{ thumb(3) }} Do as parallel branches: `A-JavaDoc`, `A-CodingStandard`, `Level-9`

As in the step 1 above, implement these three increments as three parallel branches first, and then merge them one-by-one. Hopefully, you will encounter some merge conflicts so that you get to practice de-conflicting branches.
<include src="dukeFragment.md" boilerplate var-header="**`A-JavaDoc`: JavaDoc**" var-fragment="extensions.mbdf#A-JavaDoc" />
<include src="dukeFragment.md" boilerplate var-header="**`A-CodingStandard`: Coding Standard**" var-fragment="extensions.mbdf#A-CodingStandard" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-9`: Find**" var-fragment="text.md#level9" />

<p/>

#### {{ thumb(4) }} Create a PR to the upstream repo

Create a pull request (PR) from the `master` branch of your fork to the upstream repo.
* PR name: `[Your name] Duke Increments` e.g., `[John Doe] Duke Increments` %%If you are reluctant to give full name, you may give the first half of your name only%%

<br>
</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w03", show_main_text) }}