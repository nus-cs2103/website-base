{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs with context %}

{% set admin_sections = [
  {topic_id: "project-w08-mid-v12"},
  {faq_id: "admin-faq-fromScratch"},
  {faq_id: "admin-faq-manySubmissions"},
  {faq_id: "admin-faq-cs2101Differences"}
]%}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_sections) }}