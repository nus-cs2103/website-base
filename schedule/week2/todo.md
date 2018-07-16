{% import "common/macros.njk" as macros with context %}

{% set admin_sections = [
  {heading: "Policy on Tech Help", priority: "2", source: "appendixB-policies.md#policy-techHelp"},
  {heading: "Module Tools", priority: "3", source: "tools.md#main"},
  {heading: "Project: Overview", priority: "1", source: "project-overview.md#main"},
  {heading: "Project: The Product", priority: "1", source: "project-product.md#main"},
  {heading: "Project: Scope", priority: "1", source: "project-scope.md#main"},
  {heading: "Project: Constraints", priority: "2", source: "project-constraints.md#main"},
  {heading: "Project: Timeline", priority: "2", source: "project-timeline.md#main"},
  {heading: "Module Principles", priority: "4", source: "appendixA-principles.md#main"},
  {heading: "FAQ: Why you force me to visit a separate website instead of using IVLE?", priority: "4", source: "appendixC-faq.md#admin-faq-separateWebsite"},
  {heading: "FAQ: Why slides are not detailed?", priority: "4", source: "appendixC-faq.md#admin-faq-slideFormat"},
  {heading: "FAQ: Why so much self-study?", priority: "4", source: "appendixC-faq.md#admin-faq-selfStudy"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}