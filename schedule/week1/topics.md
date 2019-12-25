{% from "schedule/index.md" import show_week_pagetop with context %}
{{ show_week_pagetop(1, "topics") }}

<box type="info" dismissible>

Topics allocated to the week will appear in this tab.
</box>

{% import "common/topics.njk" as topics with context %}
{% from "schedule/index.md" import all_topics with context %}
{{ topics.show_week_schedule("1", all_topics) }}

