{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs with context %}

{% set admin_sections = [
  {policy_id: "policy-workDistribution"},
  {policy_id: "policy-responseTime"},
  {policy_id: "policy-teamSize"},
  {faq_id: "admin-faq-beanCounting"}
]%}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_sections) }}