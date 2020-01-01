{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}
{% from "admin/ip-tasks.mbdf" import duke_increments as d, implement_increments, finish_leftover_tasks, create_pr_to_upstream with context %}

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

{{ finish_leftover_tasks(0) }}

{{ create_pr_to_upstream(1) }}

{% call implement_increments(2, [d.Level_7, d.Level_8]) %}
* Do Level 7 in a branch named `branch-Level-7`. Without merging that branch, go back to the `master` branch and implement Level 8 in a separate branch named `branch-Level-8`. Now, go back to the `master` branch and merge the two branches one after the other. As before, tag the commit (in the `master` branch, after merging) that achieves the respective deliverable, and push to your fork.<br>
 {{ icon_important_big_red }} Remember to push the branches to your fork so that the bot can detect them.<br>
 {{ icon_important_big_red }} Advanced git users: do not delete the branch after merging.<br>
 {{ icon_tip }} Merge without a _fast-forward_ so that git creates a separate commit for the merge.
{% endcall %}

{% call implement_increments(3, [d.A_MoreOOP, d.A_Packages, d.A_JUnit, d.A_Jar]) %}
* As in the previous week, commit, tag, and push, as you do the following increments in the `master` branch (no need to use separate branches).
{% endcall %}

{% call implement_increments(4, [d.A_JavaDoc, d.A_CodingStandard, d.Level_9]) %}
* As in the step 1 above, implement these three increments as three parallel branches first (branch names: `branch-A-JavaDoc`, `branch-A-CodingStandard`, `branch-Level-9`), and then merge them one-by-one. Hopefully, you will encounter some merge conflicts so that you get to practice de-conflicting branches.
{% endcall %}

<br>
</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w03", show_main_text) }}