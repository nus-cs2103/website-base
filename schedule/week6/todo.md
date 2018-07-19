{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs with context %}

{% set admin_sections = [
  {policy_id: "policy-submissionLength"},
  {faq_id: "admin-faq-narrowScope"},
  {faq_id: "admin-faq-vagueRequirements"}
]%}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_sections) }}