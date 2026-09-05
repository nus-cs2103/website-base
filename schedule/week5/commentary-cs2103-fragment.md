{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}
{% from "common/macros.njk" import show_ai_impact with context %}


<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Requirements: Intro", reuse=false) %}

As you will be dealing with the _requirements_ aspects of the tP soon, this is a good time to learn a bit about tools and techniques used for managing requirements. Let's start with a higher-level introduction first.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Requirements: Gathering") }}
{{ topic_preamble("Requirements: Specifying") }}

{% call topic_followup("Requirements: Specifying", reuse=false) %}

{% call show_ai_impact("Software Requirements") %}
**AI makes drafting and organizing requirements easier, but makes clear, validated requirements more important.** Agents can quickly suggest features, summarize stakeholder input, create prototypes, and turn notes into user stories, acceptance criteria, and glossaries. This reduces the effort needed for brainstorming and routine documentation.

**An AI agent cannot authoritatively decide what stakeholders truly need, which trade-offs matter, or whether conflicting needs have been resolved.** Because AI can turn vague instructions into plausible software very quickly, teams must put more effort into gathering evidence from real users, recording important constraints and non-functional requirements, and stating acceptance criteria precisely—otherwise, AI merely helps them build the wrong product faster.

**Thanks to AI, prototyping is now becoming the cheapest way to gather requirements.** Stakeholders work out what they want by reacting to something concrete. Building that concrete thing used to be slow, so teams asked in surveys and interviews instead. Now you can put a rough version in front of people in an afternoon.

{% endcall %}

{% endcall %}

<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Refactoring", reuse=false) %}

We've already started learning ways to improve the code quality e.g., following a coding standard. The next topic introduces you to a systematic way of changing the code to improve its quality.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Code Quality", reuse=false) %}

Next, we switch our focus to the topic of _code quality_, and learn a few more guidelines you can apply to improve the quality of your code.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Assertions", reuse=false) %}

Given next are two prerequisite topics that you'll encounter in the tP. They are shown here in case you haven't learned them before or if you would like to refresh your memory.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("RCS: Managing Pull Requests", reuse=false) %}

In the tP, you will be using pull request heavily, and you'll have to manage them yourselves. Let's start learning the ropes now itself to get ready for tP.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->

