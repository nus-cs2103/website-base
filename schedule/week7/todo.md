{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs with context %}

{% set admin_sections = [
  {topic_id: "project-w07-v11"},
  {topic_id: "appendixF-teamworkIssues"},
  {faq_id: "admin-faq-favoriteTool"}
]%}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_sections) }}