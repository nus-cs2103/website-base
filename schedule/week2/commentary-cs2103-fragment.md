{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}
{% from "common/macros.njk" import embed_topic with context %}


{{ topic_preamble("SE: Intro") }}
{{ topic_preamble("SDLC Process Models: Basics") }}
{{ topic_preamble("RCS: Revision History", id="rcs-intro") }}
{{ topic_preamble("revisionControl-what") }}
{{ topic_preamble("gitAndGithub-init") }}
{{ topic_preamble("revisionControl-savingHistory") }}
{{ topic_preamble("RCS: Remote Repos") }}
{{ topic_preamble("IDEs: Basic Features") }}
{{ topic_preamble("Automated Testing of Text UIs") }}
<!-- ---------------------------------------------------------------------------- -->

{% call topic_followup("testing-testAutomation-testingTextUis", reuse=false) %}

Congrats! You've made it to the end of this week's topics. It feels like a lot right now but now that we got an early start, this stuff will be second nature to you by the time you are done with the semester. :-)

{% endcall %}

<!-- ---------------------------------------------------------------------------- -->
