{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}

<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Design Patterns") }}
{{ topic_preamble("Singleton pattern") }}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_followup("Design Patterns", reuse=false) %}

A couple of more design patterns will be covered next week.
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Defensive Programming") }}
{{ topic_preamble("Test Cases: Intro") }}
{{ topic_preamble("Test Cases: Equivalence Partitioning") }}
{{ topic_preamble("Test Cases: Boundary Value Analysis") }}
<!-- ---------------------------------------------------------------------------- -->
