{% macro show_main_text() %} 


<div id="admin-preliminaries-anchor"></div>
<div id="admin-preliminaries">
  <include src="preliminaries.md#main" />
</div>

{% endmacro %} 

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("preliminaries", show_main_text) }}
