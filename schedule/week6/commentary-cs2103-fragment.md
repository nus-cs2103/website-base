{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}


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

It's time to push our IDEs to do more for us. The features given below can often make the IDEs worth the trouble.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("Logging", reuse=false) %}

The tP uses logging as one of its error handing strategies. As you'll be reading tP code soon, let's make sure you can recognize logging code when you see them.

{% endcall %}
<!-- ---------------------------------------------------------------------------- -->
