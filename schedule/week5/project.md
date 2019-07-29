{% from "schedule/index.md" import show_week_pagetop, show_project_summary with context%}
{{ show_week_pagetop(5, "project") }}

{{ show_project_summary(ip_file="ip-w05.md", tp_file="project-w05-v10.md") }}

# iP

<include src="../../admin/ip-w05.md#body" />

<br>
{{ hr_double }}

# tP: v1.0

<include src="../../admin/project-w05-v10.md#body" />