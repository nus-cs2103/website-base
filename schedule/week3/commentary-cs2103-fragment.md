{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}


{{ topic_preamble("RCS: Branching") }}
{{ topic_preamble("RCS: Creating Pull Requests") }}

<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Java", reuse=false) %}

Let's start by going through some Java topics that is relevant to the iP. You can skim through or skip topics that you are familiar with already.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Code Quality: Coding Standards") }}
{{ topic_preamble("codeQuality-introduction-basic") }}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Developer Testing", reuse=false) %}

As promised last week, let's learn some more sophisticated ways of testing.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->