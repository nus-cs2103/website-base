{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("moduleOverview") %} 


<div id="admin-moduleOverview-anchor"></div>
<div id="admin-moduleOverview">
  <include src="moduleOverview.md#main" />
</div>


{% endcall %}
