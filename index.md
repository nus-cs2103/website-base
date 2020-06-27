{% if current_week in ["-1", "0", "14", "15"] %}
<div id="website-content">

<include src="admin/index.md" />
</div>
{% else %}
<include src="schedule/index.md" />
{% endif %}
