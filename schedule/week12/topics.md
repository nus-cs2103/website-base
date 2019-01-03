{% import "common/outcomes.njk" as outcomes with context %}
{% from "schedule/index.md" import all_outcomes with context %}
{{ outcomes.show_week_schedule("12", all_outcomes) }}