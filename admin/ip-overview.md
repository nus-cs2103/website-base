{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

The objective of the individual project (iP) is ...

The iP is based on the generic project [_Project Duke_](../se-book-adapted/projectDuke/index.html), the overview of which is given below.


<include src="dukeFragment.md" boilerplate var-header="**Duke - Overview**" var-fragment="text.md#intro" />
<br>

The project is to be done over weeks 2-6.
Each week: selected levels/extensions, additional requirements. Some extensions will be specific to each student and will be emailed to you during that week.

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-overview", show_main_text) }}