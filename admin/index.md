{% macro show_main_text() %} 


<div id="admin-moduleOverview-anchor"></div>
<div id="admin-moduleOverview">
  <include src="moduleOverview.md#main" />
</div>

{% endmacro %} 

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("moduleOverview", show_main_text) }}
