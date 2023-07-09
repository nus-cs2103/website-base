{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}


{{ topic_preamble("RCS: Branching") }}
{{ topic_preamble("RCS: Creating Pull Requests") }}
{{ topic_preamble("Automating the Build Process") }}

<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Java: JavaDoc, file I/O, packages, JARs", reuse=false) %}

Next, we have a few more Java topics that you need as you move from a 'programming exercise' mode to a 'production code' mode.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->

{{ topic_preamble("Code Quality: Coding Standards") }}
{{ topic_preamble("codeQuality-introduction-basic") }}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Developer Testing", reuse=false) %}

As promised last week, let's learn some more sophisticated ways of testing.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("cppToJava-junit-intermediate") }}
