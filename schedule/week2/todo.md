{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs with context %}

{% set admin_sections = [
  {policy_id: "policy-techHelp"},
  {topic_id: "tools"},
  {topic_id: "project-overview"},
  {topic_id: "project-product"},
  {topic_id: "project-scope"},
  {topic_id: "project-constraints"},
  {topic_id: "project-timeline"},
  {topic_id: "appendixA-principles"},
  {faq_id: "admin-faq-separateWebsite"},
  {faq_id: "admin-faq-slideFormat"},
  {faq_id: "admin-faq-selfStudy"}
]%}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_sections) }}