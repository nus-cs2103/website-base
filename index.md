<frontmatter>
title: "Home"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 4
</frontmatter>

{% from "schedule/index.md" import weeks, current_weeks with context %}
{% if "-1" in current_weeks or "14" in current_weeks %}
<include src="admin/index.md" />
{% else %}
<include src="schedule/index.md" />
{% endif %}
