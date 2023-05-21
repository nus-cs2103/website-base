{% if course in ["TIC2002", "TEE3201"] %}

<include src="index-{{ course | lower }}-fragment.md" />

{% else %}
  {% from "common/admin.njk" import show_admin_page with context %}
  {% call show_admin_page("courseOverview") %}

<div id="admin-courseOverview-anchor"></div>
<div id="admin-courseOverview">
  <include src="courseOverview.md#main" />
</div>

  {% endcall %}
{% endif %}
