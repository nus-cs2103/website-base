{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Submit the quiz

{{ icon_project }} **Project:**
1. Implement increments `Level-7`, `A-MoreOOP`, `A-Packages`
{% endcall %}

<!-- ==================================================================================================== -->
{{ heading_project }}
<div id="project">

#### {{ thumb(1) }}  Implement increments `Level-7`, `A-MoreOOP`, `A-Packages`

<box type="tip" seamless>

Optional, but recommended: To practice Git branching, implement each increment as a separate branch. Given below are the steps:

1. Create a branch with a suitable name e.g., `branch-Level-7`.
1. Checkout that branch, and implement the Level-7 increment in that branch, while committing at appropriate points.
1. Switch back to the `master` branch.
1. Merge the `branch-Level-7` to the `master` branch.<br>
   ...<br>
1. Repeat the above steps for the remaining increments.
</box>

<div class="indented">
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-7`: Save**" var-fragment="text.md#Level-7" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-MoreOOP`: More OOP**" var-fragment="extensions-fragment.md#A-MoreOOP" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-Packages`: Java Packages**" var-fragment="extensions-fragment.md#A-Packages" />


</div>
</div>
