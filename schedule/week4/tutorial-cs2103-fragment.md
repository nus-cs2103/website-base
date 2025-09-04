{% from "common/macros.njk" import show_faq, thumb with context %}

{% if semester != "AY2425S2" %}
#### {{ thumb(1) }} **[First 5 minutes] Share iP progress**

1. Launch the current version of your iP.
1. Give some inputs to it.
1. Take a screenshot of the current state of the UI.
1. Paste the screenshot in the `T4-Workspace.pptx` file (your tutor will tell you where to find that file).

{{ show_faq("warmUpTaskRushed") }}

#### {{ thumb(2) }} **Interpret class/object diagrams**
{% else %}
#### {{ thumb(1) }} **Interpret class/object diagrams**
{% endif %}

* Do the two exercise given below, as directed by the tutor.

<box type="tip" seamless>

**Use the ==[UML Reference Sheet]({{ baseUrl }}/admin/uml-reference-sheet.md)==** to quickly look up UML notation.
</box>

<div class="indented-level2">

<include src="../../book/combined/exercises/interpretClassAndObjectDiagramAllNotations.md" />
<include src="../../book/modeling/modelingStructures/classDiagramsIntermediate/q-explainClassDiagramNotation.md" />
<p/>
</div>

{{ show_faq("umlIsItUsedInIndustry") }}
{{ show_faq("umlAreWeOverdoing") }}
<!--
#### {{ thumb(4) }} **Share Git tips** {{ icon_extra }}

* Find out how to do these git tasks and share with others
  * modify the most recent commit
  * undo the most recent commit
  * delete the most recent commit
  * stash changes
  * squash commits
  * cherrypick commits
-->
