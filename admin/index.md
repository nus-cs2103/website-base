{% if module in ["TIC2002", "TEE3201"] %}

<include src="index-{{ module | lower }}.mbdf" />

{% else %}
  {% from "common/admin.njk" import show_admin_page with context %}
  {% call show_admin_page("moduleOverview") %}

<div id="admin-moduleOverview-anchor"></div>
<div id="admin-moduleOverview">
  <include src="moduleOverview.md#main" />
</div>

  {% endcall %}
{% endif %}
