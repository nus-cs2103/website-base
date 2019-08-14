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

iP is a new addition to the module. And we have done some major changes to tP too. As such, it is possible that there will be some teething issues. If you encounter any problem while doing iP/tP, please post in the [forum]({{ forum_link }}) so that we can take necessary actions.
</box>

#### {{ thumb(1) }} Set up prerequisites

**Ensure you have met the following prerequisites:**

<box>

**Prerequisites**:

* Install Git in your computer.
* Have a GitHub account.
* Recommended: Installed an IDE in your computer.

{{ embed_topic("tools.md#main", "Admin " + icon_embedding + " **Tools**", "ipW02-tools", "2") }}

</box>
<br>

#### {{ thumb(2) }} Set up the project in your computer

1. Fork [{{ module_org }}/duke]({{ module_org }}/duke).
1.  ==Ensure the issue tracker of your fork is enabled.== %%Reason: our bots will be posting your weekly progress reports on the issue tracker of your fork.%%
1. Clone the fork onto your computer.
1. Set up the project in your IDE as explained in the README file.

#### {{ thumb(3) }} Implement increments while committing code frequently

Implement the following <tooltip content="in this context, an _increment_ is a Duke _level_ or a Duke _extension_">increments</tooltip> in the given order.
   * Commit code at important points. ==Minimally, commit after completing each increment==.
   * After completing each increment,
     * **`git tag`** the commit with the exact increment ID e.g., `Level-2`, `A-TextUiTesting`
     * **`git push`** the code to your fork ({{ icon_tip }} git doesn't push tags unless you specifically ask it to)
<include src="dukeFragment.md" boilerplate var-header="**`Level-1`: Greet, Echo, Exit**" var-fragment="text.md#level1" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-2`: Add, List**" var-fragment="text.md#level2" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-3`: Mark as Done**" var-fragment="text.md#level3" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-4`: ToDo, Event, Deadline**" var-fragment="text.md#level4" />
<include src="dukeFragment.md" boilerplate var-header="**`A-TextUiTesting`: Text UI Testing**" var-tag="optional" var-fragment="extensions.mbdf#A-TextUiTesting" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-5`: Handle Errors**" var-fragment="text.md#level5" />
<include src="dukeFragment.md" boilerplate var-header="**`Level-6`: Delete**" var-fragment="text.md#level6" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Enums`: Enums**" var-tag="if-applicable" var-fragment="extensions.mbdf#A-Enums" />

</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w02", show_main_text) }}