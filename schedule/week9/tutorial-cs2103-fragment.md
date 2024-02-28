{% from "common/macros.njk" import embed_topic, thumb, show_as_tab, timing_badge with context %}

#### {{ thumb(1) }} Demo measuring code _coverage_

<include src="../../admin/common-tutorials-fragment.md#demo-test-coverage" />

#### {{ thumb(2) }} Exercise: CCDs

1. {{ timing_badge("before the tutorial", "danger") }} Do the following question. As before, you should ==_freehand-draw_== the diagram.<br>
  %%{{ icon_tip }} You can use the <trigger trigger="click" for="modal:context-target">_association class_ notation</trigger> in the answer.%%

<modal large header="Relevant textbook topics" id="modal:context-target">

## Textbook → OOP → Associations →

<include src="../../book/oop/associations/associationClasses/container-inParent-asPanel.md" boilerplate />

----

## Textbook → UML → Class diagrams →
<include src="../../book/uml/classDiagrams/associationClasses/container-inParent-asPanel.md" boilerplate />
</modal>

<div class="indented-level1">

<include src="../../book/modeling/modelingStructures/objectOrientedDomainModels/q-courseDomainModel.md" />
<p/>
</div>

2. {{ timing_badge("during the tutorial", "info") }}
   * Paste a screenshot/scan/photo of your answer in the online document.
   * Discuss a sample answer, as guided by the tutor.
<box type="warning" seamless>

When discussing CCDs, remember to avoid terms such as _design_, _implementation_, _variable_, _method_ as these are terms used in the _solution domain_ whereas an CCD is about the _problem domain_.

* {{ bad }} "we can _design_ it this way"<br>
  {{ good }} "we can model it this way"
* {{ bad }} "coordinator _variable_ contains `Foo` objects"<br>
  {{ good }} "`Foo` objects are playing the role of coordinator"
* {{ bad }} "the _implementation_ will be like this"<br>
  {{ good }} "this model can support this object structure"
</box>

#### {{ thumb(3) }} Exercise: Activity Diagrams

1. {{ timing_badge("before the tutorial", "danger") }} Do the following question, similar to the previous question.

<div class="indented-level1">

<include src="../../book/modeling/modelingBehaviors/activityDiagrams/q-modelWorkflowOfBurgerShop.md" />
<p/>
</div>

2. {{ timing_badge("during the tutorial", "info") }} Post your answer and discuss, similar to the previous question.
