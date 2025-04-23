{% if current_week in ["-1", "0", "15"] %}
<div id="website-content">

<include src="admin/index.md" />
</div>
{% elseif current_week in ["14"] %}
<include src="admin/exams.md" />
{% else %}
<include src="schedule/index.md" />
{% endif %}
