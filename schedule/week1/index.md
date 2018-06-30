{% from "schedule/index.md" import show_week_todos, show_week_tutorial, show_week_lecture with context%}

{{ show_week_todos(1) }}

{{ show_week_tutorial(1) }}

{{ show_week_lecture(1) }}
