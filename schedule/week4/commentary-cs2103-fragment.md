{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}


{% call topic_preamble("Design: Models", reuse=false) %}

In the tP, you'll be thrown into a codebase of about 6K <tooltip content="Lines of Code">LoC</tooltip>. It would be hard to understand the design simply by reading the code. That's why the code base comes with a [Developer Guide](https://se-education.org/addressbook-level3/DeveloperGuide.html) containing some design models i.e., the diagrams. That means, you should be able to interpret those models by the time you start the tP in a few weeks. :fearful:

Let's start getting ready for that today. First, let's go through a high-level explanation of _models_.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Class/Object Diagrams: Basics", reuse=false) %}

Now that we have a high-level understanding of the role played by models, let's start learning some UML models, starting with UML _class diagrams_ (and _object diagrams_ which are like a distant cousin of class diagrams).

==Note that we are learning to _interpret_ these models only==, not _draw_ them (that would come later), or _design_ them. Hence, we will be going through these topics fairly rapidly.

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
{% call topic_preamble("Code reviews", reuse=false) %}

Next up are two techniques that can be used to improve code quality. You need to learn them as you will be encountering both in your iP soon.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("RCS: Managing Pull Requests", reuse=false) %}

Being able to work with PRs is an essential skill. To get started on that, let's learn how to review PRs properly. Besides, you'll be doing some PR reviews in the iP this week.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Automating the build process") }}
<!-- ---------------------------------------------------------------------------- -->
