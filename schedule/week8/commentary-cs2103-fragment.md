{% from "common/topics.njk" import panopto, slugify, topic_followup, topic_preamble with context %}
{% from "common/macros.njk" import show_faq with context %}

<!-- ---------------------------------------------------------------------------- -->
{% call topic_preamble("[Revisiting] Drawing Class/Object Diagrams - Basics", reuse=false) %}

<span class="float-end ps-2 pe-2">

<pic eager src="../../admin/images/drawingDiagrams.png" width="212"></pic><br>
<sub>[[image source](https://www.cs.auckland.ac.nz/~john-g/papers/hcc2003_1.pdf)]</sub>
</span>

In an earlier week you learned how to _interpret_ class diagrams and object diagrams. Let's go back to that topic but this time let's learn how to _draw_ those diagrams to match code. You'll need to draw class/object diagrams when you document the design of your tP.

But note that while in the tP you'll be using diagramming tools to draw the diagram, here, we focus on hand drawing. The reason is, we also want you to be able ==to quickly hand-draw UML diagrams== to aid discussions (e.g., draw a diagram on a whiteboard while explaining a design decision to colleagues).

Heads up: A ==significant portion of the final exam will be based on hand-drawing UML diagrams!==

The relevant UML topics are repeated further down in this page, for reference. In addition, here are some **worked-examples/exercise of drawing class/object/sequence diagrams:**

<include src="../../admin/common-schedule-fragment.md#uml-worked-examples-cd" />
<include src="../../admin/common-schedule-fragment.md#uml-worked-examples-sd" />


**:thinking: So, UML diagrams should match the code _exactly_ ...?**{.text-info} Not exactly. If that was the case, we could have auto-generated the diagrams from the code.<br>
In the context of this course, we draw UML diagrams to document (or discuss) the design that was (or will be) implemented. Therefore, the **UML diagram should aim to represent the _intended_ design, rather than show a literal translation of the code**. %%For example, an instance level variable in the code can hold `null` or one object, which seems like a multiplicity of `0..1`. However, in the actual design, it could have been intended as a multiplicity of `1`, and if so, the UML diagram should show a multiplicity of `1`.%%

{{ show_faq("umlWhyNoCorrespondenceBetweenUmlAndCode") }}
{{ show_faq("umlHowToFindIntendedDesignFromCode") }}
{% endcall %}

<!-- ---------------------------------------------------------------------------- -->
{{ topic_preamble("Testing: Types") }}
{{ topic_preamble("Testing: Intermediate Concepts") }}
{{ topic_followup("testing-tdd-how") }}
<!-- ---------------------------------------------------------------------------- -->
