{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}
{% from "common/macros.njk" import show_ai_impact with context %}


{% call topic_preamble("Design: Models", reuse=false) %}

In the tP, you'll be thrown into a codebase of about 6K <tooltip content="Lines of Code">LoC</tooltip>. It would be hard to understand the design simply by reading the code. That's why the codebase comes with a [Developer Guide](https://se-education.org/addressbook-level3/DeveloperGuide.html) containing some design models, i.e., the diagrams. That means, you should be able to interpret those models by the time you start the tP in a few weeks. :fearful:

Let's start getting ready for that today. First, let's go through a high-level explanation of _models_.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Class/Object Diagrams: Basics", reuse=false) %}

Now that we have a high-level understanding of the role played by models, let's start learning some UML models, starting with UML _class diagrams_ (and _object diagrams_ which are like a close cousins of class diagrams).

==Note that we are learning to _interpret_ these models only==, not _draw_ them (that would come later), or _design_ them. Hence, we will be going through these topics fairly rapidly.

<box type="tip" seamless>

**Use the ==[UML Reference Sheet]({{ baseUrl }}/admin/uml-reference-sheet.md)==** to quickly look up UML notation.
</box>

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_followup("Class Diagrams: Beyond Basics", reuse=false) %}

{% call show_ai_impact("Reading UML diagrams") %}
**You will spend far more time reading diagrams than making them.**

* **You no longer need to hold the whole notation in your head.** You can ask a tool what a symbol means at any time, and the rarely used corners of UML are not worth memorizing. An agent can also explain unfamiliar code to you in plain English, so a diagram is no longer the only way into code you have not seen before. **But you still need to be fluent with the basic notations** so that you don't need to ask AI about every bit of the diagram.
* **A diagram shows the shape of a design faster than prose/code can.** When you are handed a large change you did not write, looking at the corresponding UML diagram can be a quicker way to get an initial grasp of the change before diving into the code.
* **Diagrams have become much easier to produce using AI, so you will encounter more of them.** An agent can produce a class diagram of a codebase you have never seen, in seconds. Doing that used to take a lot of effort, which meant it rarely happened.
{% endcall %}

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Java: JavaFX", reuse=false) %}

Switching to Java now, let's learn how to write Java GUIs. Fair warning: GUI programming is hard in any language, especially so in Java. Buckle down and get through it; there's no way around it.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Java: varargs", reuse=false) %}

While we are on the topic of Java, also take note of this lesser-known Java 'syntactic sugar' feature that was introduced not long ago, in case you come across it one day or find some use for it in your coding.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Code Quality: Naming", reuse=false) %}

Last week, we started learning about code quality. Let's continue on that, and learn a few other aspects of code quality.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_followup("Code Reviews", reuse=false) %}
{% call show_ai_impact("Code Reviews") %}

**Someone still has to say yes to the code, and that someone is you.**

* **Reading every line yourself is no longer realistic.** Code arrives faster than any team can read it, so deciding what to leave unread is now part of the job. Spend your attention where a mistake is expensive or hard to undo, such as code that touches stored data or user accounts, or that changes behavior which already worked. Skim the rest.
* **Tools now do the tedious half of reviewing.** They check every line of every pull request without getting bored or running out of time. Style slips, unused variables, and obvious null problems are no longer worth your attention.
* **More focus on some things, less on others.** AI-written code reads well, so tidy code no longer means someone thought carefully about the problem. The real trouble could be elsewhere. For example, the code solves a slightly different problem from the one you asked about, or rebuilds something the codebase already has.
{% endcall %}
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Static Analysis", reuse=false) %}

Next up are two techniques that can be used to improve code quality. You need to learn them as you will be encountering both in your iP soon.

{% endcall %}
{% call topic_followup("Static Analysis", reuse=false) %}
{% call show_ai_impact("Static Analysis") %}

**The value of these tools is that they never guess.**

* **Learning the tools themselves is less of a chore than it used to be.** Setting up CheckStyle, writing a custom rule, or clearing a hundred violations across a codebase is work you can now hand to an agent. AI-written code also rarely breaks style rules to begin with, so tidying up code, which is what linters were mainly for, is a smaller job than it once was.
* **But an analyzer is certain in a way an AI reviewer is not.** When the tool says a variable is unused, it is unused. Ask an AI to review the same file twice and you can get two different answers, with no sign of what it missed the first time. That is why analyzers can block a merge and AI reviews cannot.
* **Analyzers can help AI tools too.** An agent can run the analyzer on its own code and fix what it flags before you ever see the change. A rule a machine can check gets followed, while a rule written in a document may not. The same argument raises the value of strict compiler settings and strong typing.
* **Deciding which rules to enforce is still a human call.** Analyzers report things that might be wrong, and on a large codebase that list gets long. Accept every default and people learn to ignore the output, which is worse than having no tool at all.
{% endcall %}
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("RCS: Managing Pull Requests I", reuse=false) %}

Being able to work with PRs is an essential skill. To get started on that, let's learn how to review PRs properly. Besides, you'll be doing some PR reviews in the iP this week.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Automating the build process") }}
<!-- ---------------------------------------------------------------------------- -->
