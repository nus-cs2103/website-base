{% import "common/macros.njk" as macros with context %}

{% set admin_sections = [
  {heading: "Project: mid-v1.2", priority: "1", source: "project-mid-v12.md"},
  {heading: "FAQ: Why aren't we allowed to build a new product from scratch?", priority: "4", source: "appendixC-faq.md#admin-faq-fromScratch"},
  {heading: "FAQ: Why so many submissions?", priority: "4", source: "appendixC-faq.md#admin-faq-manySubmissions"},
  {heading: "FAQ: Why submission requirements differ between CS2103T and CS2101?", priority: "4", source: "appendixC-faq.md#admin-faq-cs2101Differences"}
]%}

{{ macros.show_admin_sections_to_read(admin_sections) }}