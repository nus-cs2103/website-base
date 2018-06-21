{% import "common/macros.md" as macros with context %}

{% set admin_sections = [
  {heading: "Policy on suggested length for submissions", priority: "3", source: "appendixB-policies.md#policy-submissionLength"},
  {heading: "FAQ: Why very narrow project scope?", priority: "4", source: "appendixC-faq.md#admin-faq-narrowScope"},
  {heading: "FAQ: Why project requirements are so vague?", priority: "4", source: "appendixC-faq.md#admin-faq-vagueRequirements"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}