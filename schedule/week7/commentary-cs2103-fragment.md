{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}


{{ topic_preamble("Requirements: Use Cases") }}
{{ topic_followup("Requirements: Use Cases") }}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Design: High-Level View", reuse=false) %}

In the tP, you start with a code base that already has a certain design. What if there is no such design for you to start with? The next few topics look at how one can come up with such a design yourself.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_followup("design-introduction-what") }}
{{ topic_preamble("Design: Fundamentals") }}
{{ topic_preamble("IDEs: Advanced Features") }}
{{ topic_preamble("Integration Approaches") }}
{{ topic_preamble("Project Mgt: Scheduling and Tracking") }}
{{ topic_preamble("Project Mgt: Workflows") }}
<!-- ---------------------------------------------------------------------------- -->
