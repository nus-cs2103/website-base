{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs with context %}

{% set admin_sections = [
  {topic_id: "project-w12-mid-v14"}
]%}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_sections) }}