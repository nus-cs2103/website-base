{% from "common/macros.njk" import thumb with context %}
{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

In this week, we try to practice git branching as we do the iP.

{{ thumb(1) }} Do Level 7 in a branch named `branch-level7`. Without merging that branch, go back to the `master` branch and implement Level 8 in a separate branch named `branch-level8`. Now, go back to the `master` branch and merge the two branches one after the other. As before, tag the commit (in the `master` branch, after merging) that achieves the respective milestone, and push to your fork.

<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 7: Save**" var-fragment="text.md#level7" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 8: Dates and Times**" var-fragment="text.md#level8" />

<p/>

{{ thumb(2) }} As in the previous week, commit, tag, and push, as you do the following enhancements in the `master` branch (no need to use separate branches).
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-MoreOOP**" var-fragment="extensions.mbdf#A-MoreOOP" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Packages** `[optional]`" var-fragment="extensions.mbdf#A-Packages" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-JUnit**" var-fragment="extensions.mbdf#A-JUnit" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-Jar**" var-fragment="extensions.mbdf#A-Jar" />

<p/>

{{ thumb(3) }} As in the step 1 above, do these three as three parallel branches first, and then merge them one-by-one. Hopefully, you will encounter some merge conflicts so that you get to practice de-conflicting branches.
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-JavaDoc**" var-fragment="extensions.mbdf#A-JavaDoc" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Ext: A-CodingStandard**" var-fragment="extensions.mbdf#A-CodingStandard" />
<include src="dukeFragment.md" boilerplate var-header="**Duke - Level 9: Find**" var-fragment="text.md#level9" />

<p/>

{{ thumb(4) }} Create a PR from the `master` branch of your fork to the upstream repo.

<br>
</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-w03", show_main_text) }}