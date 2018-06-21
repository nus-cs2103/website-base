{% import "common/macros.md" as macros with context %}

{% set admin_sections = [
  {heading: "Policy on Tech Help", priority: "2", source: "appendixB-policies.md#policy-techHelp"},
  {heading: "Module Tools", priority: "3", source: "tools.md"},
  {heading: "Module Principles", priority: "4", source: "appendixA-principles.md"},
  {heading: "FAQ: Why you force me to visit a separate website instead of using IVLE?", priority: "4", source: "appendixC-faq.md#admin-faq-separateWebsite"},
  {heading: "FAQ: Why slides are not detailed?", priority: "4", source: "appendixC-faq.md#admin-faq-slideFormat"},
  {heading: "FAQ: Why so much self-study?", priority: "4", source: "appendixC-faq.md#admin-faq-selfStudy"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}