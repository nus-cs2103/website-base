{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}

{{ topic_preamble("OOP: Intro") }}
{{ topic_preamble("oop-objects-abstraction") }}
{{ topic_preamble("Java: Objects") }}
{{ topic_preamble("Java: Classes") }}
{{ topic_preamble("OOP: Class-level members") }}
{% call topic_preamble("RCS: Getting started", reuse=false) %}

<include src="{{ baseUrl }}/book/gitAndGithub/trail/text.md#trail-intro" />
<p/>

This week, we start with first three tours, to get started with Git and GitHub.

{% endcall %}
