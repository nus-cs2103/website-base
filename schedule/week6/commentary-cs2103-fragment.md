{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}
{% from "common/macros.njk" import show_ai_impact with context %}


<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Modeling: Sequence Diagrams", reuse=false) %}

The next UML model we'll be learning is _sequence diagrams_. As before, **focus on learning how to _interpret_ these diagrams** as you'll need to interpret some sequence diagrams in tP documentation pretty soon. _Drawing_ sequence diagrams will be covered in a future week.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Architecture Diagrams", reuse=false) %}

The tP developer guide also has something called an _architecture diagram_. Let's learn how to _interpret_ them too (_drawing_ them will be covered in a future week).

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("designApproaches-multilevelDesign-what", reuse=false) %}

As the tP is bigger than the iP, it's not possible to work with its entire design at the same time. The next topic explains a technique that can help when dealing with the design of a bigger system.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("IDEs: Intermediate Features", reuse=false) %}

{% call show_ai_impact("IDEs") %}
**AI changes what you use an IDE for, not whether you need one.**

* **The features that help you write code matter less now.** Auto-completion, code snippets, and memorized shortcuts save less time when the code arrives from an agent all at once. Typing code fast is no longer what makes a developer fast.
* **The features that help you read and check code matter more.** Jumping to a definition, finding every place a method is used, stepping through a debugger, reading a diff before you accept it: this is how you check work you did not write. An agent can tell you what its code is meant to do. Only running it will tell you what it actually does.
* **So an IDE is turning into a place where you inspect code, not just a place where you write it.** That makes the navigation and debugging features worth learning well, even if an agent does most of the typing.
{% endcall %}
{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Logging", reuse=false) %}

The tP uses logging as one of its error handing strategies. As you'll be reading tP code soon, let's make sure you can recognize logging code when you see them.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
