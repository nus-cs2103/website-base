{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

The objective of the individual project (iP):
* Refresh programming skills you learned in CS2030
* Learn some skills required for the team project

All skills you will learn when doing the iP will be useful in the team project (tP). Furthermore, some of the code you will write in iP can be adapted for the tP.

The iP is based on the generic project [_Project Duke_](../se-book-adapted/projectDuke/index.html), the overview of which is given below.

<include src="dukeFragment.md" boilerplate var-header="**Duke - Overview**" var-fragment="text.md#intro" />
<br>

The project is to be **done over weeks 2-6**. The work to be done in each week is explained in separate sections.

<box type="warning">

Some requirements will only be released later (or could be changed along the way), to simulate how requirements of a project may not be available at the start or stay the same during the project.
</box>

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-overview", show_main_text) }}