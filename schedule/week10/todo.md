{% import "common/macros.njk" as macros with context %}

{% set admin_sections = [
  {heading: "Project: mid-v1.3", priority: "1", source: "project-w10-mid-v13.md"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}