{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}

{{ topic_preamble("Class Diagrams: Intermediate-Level") }}
{{ topic_preamble("Logging") }}
{{ topic_preamble("Design Principles") }}
{{ topic_preamble("designFundamentals-abstraction-what") }}
{{ topic_preamble("Some Principles") }}
{{ topic_preamble("Testing: Intermediate Techniques") }}

<!-- ---------------------------------------------------------------------------- -->
{% call topic_followup("principles-separationOfConcernsPrinciple", reuse=false) %}
As you may have realized already, the two principles given above are somewhat similar, one is specific to OOP and applied at class level while the other is not specific to OOP and can be applied at any level.

To learn more principles, you can go to [https://se-education.org/se-book/principles/](https://se-education.org/se-book/principles/).
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
