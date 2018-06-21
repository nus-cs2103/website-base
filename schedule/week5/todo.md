{% import "common/macros.md" as macros with context %}

{% set admin_sections = [
  {heading: "Policy on project work distribution", priority: "2", source: "appendixB-policies.md#policy-workDistribution"},
  {heading: "Policy on email response time", priority: "3", source: "appendixB-policies.md#policy-responseTime"},
  {heading: "Policy on grading smaller/larger teams", priority: "4", source: "appendixB-policies.md#policy-teamSize"},
  {heading: "FAQ: Why so much bean counting?", priority: "4", source: "appendixC-faq.md#admin-faq-beanCounting"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}