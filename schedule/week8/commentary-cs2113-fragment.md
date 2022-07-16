{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}

{{ topic_preamble("Developer Testing") }}
{{ topic_preamble("testing-testAutomation-usingTestDrivers") }}
{{ topic_preamble("cppToJava-junit-basic") }}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_followup("cppToJava-junit-basic", reuse=false) %}
Quoting from tP instructions:
<blockquote>

<include src="../../admin/tp-tasks.mbdf#desc_add_junit_tests" />
</blockquote>
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Writing Developer Documents") }}
{{ topic_preamble("Design: Models") }}
{{ topic_preamble("Class/Object Diagrams: Basics") }}
{{ topic_preamble("modeling-modelingStructures-objectDiagrams") }}
{{ topic_preamble("Project Mgt: Scheduling and Tracking") }}
{{ topic_preamble("projectPlanning-ganttCharts") }}
{{ topic_preamble("teamwork-teamStructures") }}
