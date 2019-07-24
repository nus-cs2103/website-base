{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

{{ thumb(1) }} **Ensure you have met the following prerequisites:**

<box>

**Prerequisites**:

* Install Git in your Computer.
* Have a GitHub account.
* Recommended: Installed an IDE in your Computer.

{{ embed_topic("tools.md#main", "Admin " + icon_embedding + " **Tools**", "ipW02-tools", "2") }}

</box>
<br>

{{ thumb(2) }} **Set up the project in your Computer:**
1. Fork [this repo: TBD], and clone it into your Computer.
1. Set up the project in your IDE as explained in the README file.

{{ thumb(3) }} **Implement the following <tooltip content="in this context, an _increment_ is a Duke _level_ or a Duke _extension_">increments</tooltip>** in the given order.
   * Commit code at important points. ==Minimally, commit after completing each increment==.
   * After completing each increment,
     * **`git tag`** the commit with the exact increment ID e.g., `Level-2`, `A-TextUiTesting`
     * **`git push`** the code to your fork
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

{% from "common/macros.njk" import embed_topic, thumb with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-w02", show_main_text) }}