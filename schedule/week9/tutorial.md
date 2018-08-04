<include src="tutorial-{{ module | lower }}.md" />

{% from "schedule/index.md" import all_outcomes with context %}
{% from "common/tutorial.njk" import  show_week_evidences with context %}
{{ show_week_evidences("9", all_outcomes) }}