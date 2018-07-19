{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs with context %}

{% set admin_sections = [
  {policy_id: "policy-plagiarism"},
  {policy_id: "policy-reuse"},
  {policy_id: "policy-outsiderHelp"},
  {topic_id: "exams"},
  {faq_id: "admin-faq-noLaptop"},
  {policy_id: "policy-publishingSubmissions"}
]%}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_sections) }}