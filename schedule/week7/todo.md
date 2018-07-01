{% import "common/macros.njk" as macros with context %}

{% set admin_sections = [
  {heading: "Project: v1.1", priority: "1", source: "project-v11.md"},
  {heading: "Appedix F: Handling Teamwork Issues", priority: "3", source: "appendixF-teamworkIssues.md"},
  {heading: "FAQ: Why I'm not allowed to use my favorite tool/framework/language etc.?", priority: "4", source: "appendixC-faq.md#admin-faq-favoriteTool"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}