{% import "common/macros.njk" as macros with context %}
{% from "common/admin.njk" import topics, policies, faqs with context %}

{% set admin_sections = [
  {topic_id: "project-assessment"},
  {policy_id: "policy-followingInstructions"},
  {topic_id: "peerEvaluations"},
  {topic_id: "gradeBreakdown"},
  {topic_id: "participation"},
  {topic_id: "project-supervision"},
  {faq_id: "admin-faq-noLaptop"}
]%}

{{ macros.show_admin_sections_to_read(topics, policies, faqs, admin_sections) }}