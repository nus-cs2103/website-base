{% macro show_main_text() %}
<div id="main">

<iframe src="{{ instructors_page }}" width="800" height="1000" ></iframe>

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("instructors", show_main_text) }}