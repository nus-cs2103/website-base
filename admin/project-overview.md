{% macro show_main_text() %}
<div id="main">

The high-level learning outcome of the project (and to a large degree, the entire module):

<tip-box> {{ icon_outcome }} Can contribute production quality SE work to a small/medium software project </tip-box>

Accordingly, the module project is structured to resemble an intermediate stage of a non-trivial real-life software project. In this project you will,
 1. conceptualize and implement enhancements to a given product,
 1. and have it ready to be continued by future developers.




</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-overview", show_main_text) }}