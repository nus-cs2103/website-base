{% import "common/macros.md" as macros with context %}

{% set admin_sections = [
  {heading: "Project: v1.5", priority: "1", source: "project-v15.md"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}