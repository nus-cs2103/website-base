{% import "common/macros.njk" as macros with context %}

{% set admin_sections = [
  {heading: "Project: v1.2", priority: "1", source: "project-v12.md"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}