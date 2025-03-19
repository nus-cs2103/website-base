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

{{ panopto("88a6d3bc-7bbb-4566-a035-ac4100ce1085", desc="Drawing class/object diagrams (basic) - `Box`, `Item`, `Lid`", questions="yes") }}
{{ panopto("052aa055-c89f-4dbf-af24-ac4000f175e0", desc="Drawing class/object diagrams (intermediate) - `Action`, `Task`, `History`") }}
{{ panopto("f4f7e1f2-60a4-4d18-b70a-ac4000f17608", desc="Drawing class/object diagrams (intermediate) - `Person`, `Inbox`, `Message`") }}
{{ panopto("e05845ed-8c70-47d9-a4d0-ac6800d58224", desc="Drawing class/object diagrams (intermediate) - `Person`, `Project`, `Task`") }}
{{ panopto("fe9d362e-4e3d-4c30-81ec-ac5a00cf8d95", desc="Drawing sequence diagrams (basic) - `Item` creation") }}
{{ panopto("3e47c3c3-60db-4e2f-a15f-ac4100ce10c4", desc="Drawing sequence diagrams (intermediate) - `TaskList#generateTask()`") }}
{{ panopto("c4856a68-4c30-4f9c-8efa-ac6800d581f2", desc="Drawing sequence diagrams (intermediate) - create `Quote`") }}


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
