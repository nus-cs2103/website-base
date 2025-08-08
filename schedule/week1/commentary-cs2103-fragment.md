{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}

{% call topic_preamble("OOP: Classes & Objects", reuse=false) %}

Topics for this week form two sections:

1. **%%[W1.1 - W1.5]%% Some OOP and Java ==<tooltip content="i.e., topics you are expected to know already">prereq topics</tooltip>==** (icon %%{{ icon_prereq }}{{ icon_prereq }}%% indicates prereq topics): Go through these topics to refresh your memory, and demonstrate your knowledge by submitting the _Week 1 Quiz (aka prereq topics quiz)_ on Canvas.
1. **%%[[W1.6](#W1-6)]%% Getting Started with Git:** The start of a series of lessons on Git and GitHub — two tools that will be used heavily in this course.

Let's start with the prereq topics.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("RCS: Getting Started with Git", reuse=false) %}

Now it's time to move to the second section of this week's topics:

<include src="{{ baseUrl }}/book/gitAndGithub/trail/text.md#trail-intro" />
<p/>

This week, we start with tour 1.

{{ icon_important_big_red }} **These Git lessons are brand new, added this semester — teething issues are expected!** Please help us improve it by reporting any issues, bugs, unclear parts, suggestions — even minor/cosmetic ones — in the {{ link_forum }}. You can earn bonus participation points by doing so too.
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
