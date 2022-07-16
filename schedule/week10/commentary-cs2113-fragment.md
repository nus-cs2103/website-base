{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}

{{ topic_preamble("Sequence Diagrams: Basics") }}

<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Design Patterns") }}
{{ topic_preamble("designPatterns-introduction-what") }}
{{ topic_preamble("Singleton pattern") }}

<!-- ---------------------------------------------------------------------------- -->
{% call topic_followup("designPatterns-facade-what", reuse=false) %}
To learn more design patterns, you can refer to [https://se-education.org/se-book/designPatterns/](https://se-education.org/se-book/designPatterns/)
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Testing: Test Coverage") }}
{{ topic_preamble("testing-testCoverage-how") }}
<!-- ---------------------------------------------------------------------------- -->
