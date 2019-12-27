<frontmatter>
title: "Home"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 4
</frontmatter>

{% from "schedule/index.md" import weeks, current_week with context %}
{% if current_week == "-1" or current_week == "14" %}
<include src="admin/index.md" />
{% else %}
<include src="schedule/index.md" />
{% endif %}
