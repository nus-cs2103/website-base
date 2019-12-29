{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Set up prerequisites
1. Set up the project in your computer
3. Implement increments while committing code frequently: `Level-1`, `Level-2`, `Level-3`, `Level-4`, `A-TextUiTesting`, `Level-5`, `Level-6`, `A-Enums` {{ timing_badge("by Thursday 2359") }}
{% endcall %}
<div id="body">

<box type="info">

iP (and the tP) undergoes changes after each semester. As such, teething issues are a possibility. If you encounter any problem while doing iP/tP, please post in the [forum]({{ forum_link }}) so that we can take necessary actions.
</box>

#### {{ thumb(0) }} Learn about the project

**Read the following two sections**, if you haven't done so already:

<div class="indented">

{{ embed_topic("ip-overview.md#main", "Admin " + icon_embedding + " **iP - Overview**", "3") }}
{{ embed_topic("ip-grading.md#main", "Admin " + icon_embedding + " **iP - Grading**", "1") }}
</div>

#### {{ thumb(1) }} Set up prerequisites

**Ensure you have met the following prerequisites:**

<box>

**Prerequisites**:

* Install Git in your computer.
* Have a GitHub account.
* Recommended: Installed an IDE in your computer.

{{ embed_topic("tools.md#main", "Admin " + icon_embedding + " **Tools**", "2") }}

</box>
<br>

#### {{ thumb(2) }} Set up the project in your computer

1. Fork [{{ module_org }}/duke]({{ module_org }}/duke).
1.  ==Enable the issue tracker of your fork== (Go to `Settings` of your fork, scroll to the `Features` section, and tick the `Issues` checkbox). %%Reason: our bots will be posting your weekly progress reports on the issue tracker of your fork.%%<br>
    {{ icon_tip }} If the issue tracker is enabled, you should be able to visit the following URL `https://github.com/{your_user_name}/duke/issues` e.g., `https://github.com/johnDoe/duke/issues`
1. Clone the fork onto your computer.
1. Set up the project in your IDE as explained in [the README file]({{ module_org }}/duke/blob/master/README.md).<br>
   {{ icon_tip }} If you are somewhat familiar with build tools such as Gradle, you are free to go ahead and start using Gradle from the beginning by following [the Gradle tutorial]({{ module_org }}/duke/blob/master/tutorials/gradleTutorial.md).

#### {{ thumb(3) }} Implement increments while committing code frequently

Implement the following <tooltip content="in this context, an _increment_ is a Duke _level_ or a Duke _extension_">increments</tooltip> ==in the given order==.
   * Commit code at important points. ==Minimally, commit after completing each increment==.
   * After completing each increment,
     * **`git tag`** the commit with the exact increment ID e.g., `Level-2`, `A-TextUiTesting`
     * **`git push`** the code to your fork ({{ icon_tip }} git doesn't push tags unless you specifically ask it to)

<box>

{{ icon_important_big_red }} We discourage you from doing project tasks allocated to future weeks. Reasons:
1. In order to help you gain <tooltip content="the ability to apply knowledge or do tasks effortlessly as if you have been doing them for a long time">_fluency_</tooltip> (and also to better simulate real projects), **we want the project work to be <tooltip content="done at multiple times with time gaps in between">_spaced_</tooltip> and spread over a longer period**, rather than to be done as a short burst. Reminder: as per iP grading criteria, _some_ increments need to to be done in each week for you to get full marks.
1. As a further incentive to not jump ahead, we have left some future project requirements unspecified, and we might change some requirements along the way too.
</box>

<include src="dukeFragment.md" boilerplate var-header="**`Level-1`: Greet, Echo, Exit**" var-fragment="text.md#level1" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-2`: Add, List**" var-fragment="text.md#level2" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-3`: Mark as Done**" var-fragment="text.md#level3" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-4`: ToDo, Event, Deadline**" var-fragment="text.md#level4" />
<include src="dukeFragment.md" boilerplate var-header="**`A-TextUiTesting`: Text UI Testing**" var-tag="optional" var-fragment="extensions.mbdf#A-TextUiTesting" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-5`: Handle Errors**" var-fragment="text.md#level5" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-6`: Delete**" var-fragment="text.md#level6" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Enums`: Enums**" var-tag="if-applicable" var-fragment="extensions.mbdf#A-Enums" />

<p/>

</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w02", show_main_text) }}