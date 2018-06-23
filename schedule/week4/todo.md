{% import "common/macros.njk" as macros with context %}

{% set admin_sections = [
  {heading: "Policy on plagiarism", priority: "1", source: "appendixB-policies.md#policy-plagiarism"},
  {heading: "Policy on reuse", priority: "1", source: "appendixB-policies.md#policy-reuse"},
  {heading: "Policy on help from outsiders", priority: "1", source: "appendixB-policies.md#policy-outsiderHelp"},
  {heading: "Exams", priority: "3", source: "exams.md"},
  {heading: "FAQ: What if I don't carry around a laptop", priority: "4", source: "appendixC-faq.md#admin-faq-noLaptop"},
  {heading: "Policy on publishing submissions", priority: "4", source: "appendixB-policies.md#policy-publishingSubmissions"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}