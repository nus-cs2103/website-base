{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}
{% from "common/macros.njk" import embed_topic, show_ai_impact with context %}


{{ topic_preamble("SDLC Process Models: Basics") }}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("RCS: Getting Started with GitHub", reuse=false) %}

{% call show_ai_impact("Git and GitHub") %}
**Git is becoming less something you type and more something you lean on.**

* **Remembering commands matters less now.** An agent can run `git` for you, so you no longer need to recall the exact command for undoing a change or tidying up a messy history. You do still need to know what those commands *do*, or you cannot tell whether the agent did the right thing.
* **Being able to go back matters more.** An agent can change many files in seconds, and not every change will be one you wanted. If you committed your work first, getting back is easy; if you did not, the version that worked may be gone for good.
* **Reading changes matters more, too.** More of your time on Git and GitHub now goes into looking at diffs and pull requests, checking work you did not write yourself. That is why **small commits with clear messages are worth the trouble**: they are easier to read, easier to undo one at a time, and they record *why* something was done, which the code alone never tells you.
{% endcall %}

With that in mind, let's resume our Git-Mastery journey, covering a few more tours. the first two focus on working with GitHub, while the other two focus on getting more out of the Git revision history.
{% endcall %}
{{ topic_preamble("IDEs: Basic Features") }}
{{ topic_preamble("Intro to Automated Testing") }}
{{ topic_followup("testing-testAutomation-testingTextUis") }}
<!-- ---------------------------------------------------------------------------- -->
