{% from "schedule/index.md" import show_week_pagetop with context %}
{{ show_week_pagetop(10, "topics") }}

{% import "common/topics.njk" as topics with context %}
{% from "schedule/index.md" import all_topics with context %}
{{ topics.show_week_schedule("10", all_topics) }}