{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

To get full marks, you should achieve **at least some deliverables in each week** (i.e., weeks 2-6) and achieve **more than 80% of all deliverables** by the end.
* Requirements marked as `optional` or `if applicable` are not counted when calculating the percentage of achievements.
* When a requirement specifies a `minimal` version of it, simply reaching that minimal version of the requirement is enough for it to be counted for grading -- however, we recommend you to go beyond the minimal; the farther you go, the more practice you get.

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("ip-grading", show_main_text) }}