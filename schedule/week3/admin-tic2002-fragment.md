{% from "common/macros.njk" import embed_topic, show_as_tab, thumb, timing_badge with context %}
{% from "common/admin.njk" import show_admin_summary with context %}


{% call show_admin_summary() %}
1. Install IntelliJ IDEA {{ timing_badge("before the lecture") }}
1. Submit weekly exercises

{{ icon_project }} **Project:**
1. Setup Duke project on your computer {{ timing_badge("during/after the lecture", "info") }}
1. Implement project increments `Level-1`, `Level-2`
{% endcall %}


#### {{ thumb(1) }} Install IntelliJ IDEA {{ timing_badge("before the lecture", "secondary") }}

* See the panel below:

{{ embed_topic("../../admin/index-tic2002-fragment.md#intellij-info", "Admin " + icon_embedding + " Tools → IntelliJ IDEA", "week2Admin-intellij", "2") }}


#### {{ thumb(2) }} Submit weekly exercises

* As usual, submit weekly programming exercise.

<!-- ==================================================================================================== -->

{{ heading_project }}

#### {{ thumb(0) }} Learn about the project

{{ embed_topic("../../admin/index-tic2002-fragment.md#project-info", "Admin " + icon_embedding + " Project", "week1Admin-java", "2") }}
<div class="indented">
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**Overview**" var-fragment="text.md#intro" />
</div>
<p/>

<div id="project">

#### {{ thumb(1) }} Setup Duke project on your computer {{ timing_badge("during/after the lecture", "secondary") }}

1. **Fork** [{{ url_course_org }}/duke]({{ url_course_org }}/duke). The relevant textbook topic is given below for your reference.<br>
   {{ icon_important_big_red }} Please ==retain the repo name `duke`== when forking. If you name your fork as something else, our grading scripts will not be able to find your fork.<br>
   {{ embed_topic("../../book/gitAndGithub/fork/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Forking**", "1", indent=2) }}

2. **Clone** the fork onto your computer.

   {{ embed_topic("../../book/gitAndGithub/clone/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Cloning**", "1", indent=2) }}

3. **Set up** the project in your IDE as explained in [the README file]({{ url_course_org }}/duke).

<!-- ------------------------------------------------------------------------------------------------------ -->

#### {{ thumb(2) }} Implement Duke increments `Level-1`, `Level-2`

* Take note of our plagiarism policies

{{ embed_topic("../../admin/index-tic2002-fragment.md#plagiarism-policy", "Admin " + icon_embedding + " Policies -> **Plagiarism**", "1", indent=2, type="danger") }}

* Implement the following <tooltip content="in this context, an _increment_ is a Duke _level_ or a Duke _extension_">increments</tooltip> in the given order.
  * **Commit** code at important points. ==Minimally, commit after completing each increment==.
  * After completing each increment,
     * **Tag** the commit with the exact increment ID e.g., `Level-0`, `Level-1`, `Level-2`.
     * **Push** the code to your fork.
  * The relevant textbook topics are:
     {{ embed_topic("../../book/gitAndGithub/commit/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Committing**", "1", indent=2) }}
     {{ embed_topic("../../book/gitAndGithub/tag/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Tagging**", "1", indent=2) }}
     {{ embed_topic("../../book/gitAndGithub/push/text.md#simple-push", "Textbook " + icon_embedding + " Git & GitHub → **Pushing**", "1", indent=2) }}
  * {{ icon_tip }} If you encounter issues connecting Sourcetree with your GitHub account, refer to these [Sourcetree Tips](https://se-education.org/guides/tutorials/sourcetree.html).
<div class="indented-level2">

<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-0`: Rename, Greet, Exit**" var-fragment="text.md#Level-0" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-1`: Echo**" var-fragment="text.md#Level-1" />
<include src="dukeFragment.md" boilerplate var-displacement="../.." var-header="**`Level-2`: Add, List**" var-fragment="text.md#Level-2" />
</div>

</div>
