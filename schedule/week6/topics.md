{% from "schedule/index.md" import show_week_pagetop with context %}
{{ show_week_pagetop(6, "topics") }}

{% import "common/topics.njk" as topics with context %}
{% from "schedule/index.md" import all_topics with context %}
{{ topics.show_week_schedule("6", all_topics) }}