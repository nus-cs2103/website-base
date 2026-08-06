{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}

{{ topic_preamble("SE: Intro") }}
{% call topic_preamble("OOP: Classes & Objects", reuse=false) %}

Topics for this week form two sections:

1. **++Revisiting prereq topics++**, covered by **%%[W1.1 - W1.5]%% Some OOP and Java ==<tooltip content="i.e., topics you are expected to know already">prereq topics</tooltip>==** (icon %%{{ icon_prereq }}{{ icon_prereq }}%% indicates prereq topics): Go through these topics to refresh your memory, and demonstrate your knowledge by submitting the _Week 1 Quiz (aka prereq topics quiz)_ on Canvas.
1. **++Getting started with new topics++**, on two fronts:
   * **%%[[W1.6](#W1-6)]%% An intro to SE**: A quick overview of the field of SE itself, before we start learning other SE topics.
   * **%%[[W1.7](#W1-7)]%% Getting Started with Git:** The start of a series of lessons on Git and GitHub — two tools that will be used heavily in this course.

Let's start with the prereq topics.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_followup("errorHandling-exceptions-when", reuse=false) %}

Phew. We are done with the prereq topics. It's time to move to new topics for this semester.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_followup("softwareEngineering-introduction-prosAndCons", reuse=false) %}

****Scanning a TLDR version of a topic:**** As mentioned in ['Using this Website' page](../../admin/usingThisWebsite.html#:~:text=using%20Chrome.-,Information%20layers,-This%20book%20tries), the more important layer of information is given in bold text. For example, **you can quickly scan the essential points of a topic by reading the bold text only** (this could be useful when you want to quickly recap a previous topic, or to get an idea of what a topic covers without reading all the details).

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("RCS: Getting Started with Git", reuse=false) %}

Next is the second of this week's topics:

<include src="../../admin/common-commentary-fragment.md#git-mastery-preamble" />

<box type="important" seamless>

Unless you are an experienced Git user, **you are strongly encouraged to do the Git-Mastery exercises, and enable online tracking of progress via the companion app** so that we can recognise your Git-Mastery progress as an optional [participation]({{ baseUrl }}/admin/participation.md) activity.
</box>

This week, we start with tour 1.
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
