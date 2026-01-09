{% from "common/topics.njk" import topic_followup, topic_preamble with context %}

{{ topic_preamble("SE: Intro") }}
{{ topic_preamble("SDLC Process Models: Basics") }}
{{ topic_preamble("Java: Intro") }}
{{ topic_preamble("Java: HelloWorld") }}
{{ topic_preamble("Java: Data Types") }}
{{ topic_preamble("Java: Control Flow") }}
{% call topic_preamble("RCS: Getting Started with Git", reuse=false) %}

<include src="../../admin/common-commentary-fragment.md#git-mastery-preamble" />

This week, we start with first three tours, to get started with Git and GitHub.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("RCS: Getting Started with Git and GitHub", reuse=false) %}

<include src="../../admin/common-commentary-fragment.md#git-mastery-preamble" />

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("IDEs: Basic Features") }}
{{ topic_preamble("Code Quality: Coding Standards") }}
