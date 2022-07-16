{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Submit weekly exercises

{{ icon_project }} **Project:**
1. Create a Pull Request {{ timing_badge("during/after the lecture", "info") }}
1. Implement project increments `Level-3`, `A-TextUiTesting` <span class="badge badge-pill badge-secondary">optional</span>
{% endcall %}

#### {{ thumb(1) }} Submit weekly exercises

* As usual.

<!-- ==================================================================================================== -->
{{ heading_project }}

<div id="project">

#### {{ thumb(1) }} Create a Pull Request {{ timing_badge("during/after the lecture", "secondary") }}

* **Create a pull request (PR)** from your fork to [{{ url_module_org }}/duke]({{ url_module_org }}/duke)
  * To be done only after you have pushed some code to your fork.
  * PR name should be your name (you may leave out the family name if you wish).
  * PR description can be left blank.
  * [GitHub's help page about creating PRs](https://help.github.com/en/articles/creating-a-pull-request).{% if tic2002 %}
  * ==Use Option A== in the step 3 of the instructions in the panel below, as you guys haven't learned about git branching yet.{% endif %}

{{ embed_topic("../../book/gitAndGithub/createPRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Creating PRs**", "1", indent=2) }}
<!-- ------------------------------------------------------------------------------------------------------ -->

#### {{ thumb(2) }} Implement project increments `Level-3`, `A-TextUiTesting` <span class="badge badge-pill badge-secondary">optional</span>

* **As before, implement these increments** while committing at regular intervals, and tag + push to your fork when an increment is done. Your PR will update automatically to reflect the new commits. ==Follow the same procedure for future Duke increments too.==

<div class="indented">

<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-3`: Mark as Done**" var-fragment="text.md#Level-3" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`A-TextUiTesting`: Text UI Testing**" var-tag="optional" var-fragment="extensions.mbdf#A-TextUiTesting" />

</div>
</div>