<frontmatter>
title: "Timeline"
header: header.md
footer: footer.md
head: scheduleHead.md
pageNav: 3
</frontmatter>

{% import "common/topics.njk" as topics with context %}
{% from "schedule/index.md" import all_topics with context %}


# Summary of the Module Timeline

{% for week_num in range(1, 14) %}

### <span class="badge badge-pill badge-dark"><small>**Week {{ week_num }}**</small></span>

<include src="week{{ week_num }}/notices-{{ module }}.md#summary" optional />
{% endfor %}



