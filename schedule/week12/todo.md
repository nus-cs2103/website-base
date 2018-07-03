{% import "common/macros.njk" as macros with context %}

{% set admin_sections = [
  {heading: "Project: mid-v1.4", priority: "1", source: "project-w12-mid-v14.md"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}