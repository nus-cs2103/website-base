{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}
{% from "common/macros.njk" import show_ai_impact with context %}

<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("OO Domain Models") }}
{{ topic_followup("OO Domain Models") }}
{{ topic_preamble("Activity Diagrams") }}
{{ topic_followup("Activity Diagrams") }}
{{ topic_preamble("Conceptualizing a Design") }}
{{ topic_preamble("Architecture Diagrams: Drawing") }}
{{ topic_preamble("Design Principles") }}
{{ topic_preamble("principles-interfaceSegregationPrinciple") }}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("[Revisiting] SDLC Process Models", reuse=false) %}
Remember these three topics that we covered early in the course?
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("SDLC Process Models (continued)", reuse=false) %}
Let's continue that thread to learn about some SDLC process models that are commonly used in the industry.
{% endcall %}

{% call topic_followup("SDLC Process Models (continued)", reuse=false) %}
{% call show_ai_impact("SDLC process models") %}
**AI changes the cost of the work, not the need for a plan.**

* **Picking the right process model matters less now.** Building a version of the software used to take weeks, so it was worth arguing about how to order the stages. When an agent can produce a version in hours, less rides on that choice, and _code-and-fix_ starts to look tempting again.
* **Knowing what you want, and checking what you got, matter more.** Those are the two things an agent cannot do for you. **So the useful part of a process model is now its outputs, not its stages**: a clear requirement, an agreed design, and a test that says what 'done' means. These are also what you hand to an agent. Give it a vague one, and you will get the wrong thing built quickly and confidently.
* **Short iterations matter more, not less.** When a wrong turn takes minutes, you want frequent points where a human looks at real output.
{% endcall %}
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Writing Developer Documents") }}
<!-- ---------------------------------------------------------------------------- -->
