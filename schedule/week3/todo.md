{% import "common/macros.md" as macros with context %}

{% set admin_sections = [
  {heading: "Project: Assessment", priority: "1", source: "project-assessment.md"},
  {heading: "Policy on following instructions", priority: "1", source: "appendixB-policies.md#policy-followingInstructions"},
  {heading: "Peer Evaluations", priority: "2", source: "participation.md"},
  {heading: "Grade Breakdown", priority: "2", source: "gradeBreakdown.md"},
  {heading: "Participation Marks", priority: "2", source: "participation.md"},
  {heading: "Supervision", priority: "3", source: "supervision.md"},
  {heading: "FAQ: What if I don't carry around a laptop", priority: "4", source: "appendixC-faq.md#admin-faq-noLaptop"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}