{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}
{% from "common/macros.njk" import show_ai_impact with context %}


{% call topic_preamble("Design: Models", reuse=false) %}

In the tP, you'll be thrown into a codebase of about 6K <tooltip content="Lines of Code">LoC</tooltip>. It would be hard to understand the design simply by reading the code. That's why the codebase comes with a [Developer Guide](https://se-education.org/addressbook-level3/DeveloperGuide.html) containing some design models i.e., the diagrams. That means, you should be able to interpret those models by the time you start the tP in a few weeks. :fearful:

Let's start getting ready for that today. First, let's go through a high-level explanation of _models_.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Class/Object Diagrams: Basics", reuse=false) %}

Now that we have a high-level understanding of the role played by models, let's start learning some UML models, starting with UML _class diagrams_ (and _object diagrams_ which are like a close cousin of class diagrams).

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
* **Diagrams have become much easier to produce using AI, so you will encounter more of them.** An agent can produce a class diagram of a codebase you have never seen, in seconds. Doing that used to take a lot of effort, which meant it rarely happened.
* **A diagram shows the shape of a design faster than prose/code can.** When you are handed a large change you did not write, looking at the corresponding UML diagram can be a quicker way to get an initial grasp of the change before diving into the code.
* **A generated diagram can be wrong, and you are the only one who will notice.** It may quietly leave out something important, or show what the code happens rather than the intended design. If you cannot read the diagram, you cannot tell the difference.
{% endcall %}

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Java: JavaFX", reuse=false) %}

Switching to Java now, let's learn how to write Java GUIs. Fair warning: GUI programming is hard in any language, especially so in Java. Buckle down and get through it; there's no way around it.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Java: varargs", reuse=false) %}

While we are on the topic of Java, also take note of this is a lesser-known Java 'syntactic sugar' feature that was introduced not long ago, in case you come across it one day or find some use for it in your coding.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Code Quality: Naming", reuse=false) %}

Last week, we started learning about code quality. Let's continue on that, and learn a few other aspects of code quality.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Static Analysis", reuse=false) %}

Next up are two techniques that can be used to improve code quality. You need to learn them as you will be encountering both in your iP soon.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("RCS: Managing Pull Requests I", reuse=false) %}

Being able to work with PRs is an essential skill. To get started on that, let's learn how to review PRs properly. Besides, you'll be doing some PR reviews in the iP this week.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Automating the build process") }}
<!-- ---------------------------------------------------------------------------- -->
