{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}
{% from "common/macros.njk" import embed_topic with context %}


{{ topic_preamble("SE: Intro") }}
{{ topic_preamble("SDLC Process Models: Basics") }}
{% call topic_followup("processModels-introduction-iterativeModels", reuse=false) %}

****Scanning a TLDR version of a topic:**** As mentioned in ['Using this Website' page](../../admin/usingThisWebsite.html#:~:text=using%20Chrome.-,Information%20layers,-This%20book%20tries), the more important layer of information is given in bold text. For example, **you can quickly scan the essential points of a topic by reading the bold text only** (this could be useful when you want to quickly recap a previous topic, or to get an idea of what a topic covers without reading all the details).

{% endcall %}
{{ topic_preamble("RCS: Revision History", id="rcs-intro") }}
{{ topic_preamble("RCS: Remote Repos") }}
{{ topic_preamble("IDEs: Basic Features") }}
{{ topic_preamble("Automated Testing of Text UIs") }}
<!-- ---------------------------------------------------------------------------- -->

{% call topic_followup("testing-testAutomation-testingTextUis", reuse=false) %}

Congrats! You've made it to the end of this week's topics. It feels like a lot right now but now that we got an early start, this stuff will be second nature to you by the time you are done with the semester. :-)

{% endcall %}

<!-- ---------------------------------------------------------------------------- -->
