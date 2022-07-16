{% from "common/macros.njk" import embed_topic, thumb, show_as_tab, timing_badge with context %}

#### {{ thumb(0, thumb_style="secondary") }} %%Demo v1.2%%

<div class="indented-level2">

%%The tutor to confirm the following has been done.%%

{{ embed_topic("../../admin/tp-tasks.mbdf#desc_do_an_informal_demo", "Admin " + icon_embedding + " tP v1.2: Demo", "3") }}
</div>
<p/>

#### {{ thumb(1) }} Demo measuring code _coverage_

<include src="../../admin/common-tutorials.mbdf#demo-test-coverage" />

#### {{ thumb(2) }} Exercise: OODMs

1. {{ timing_badge("before the tutorial", "danger") }} Do the following question. As before, you should ==_freehand-draw_== the diagram.<br>
  %%{{ icon_tip }} You can use the <trigger trigger="click" for="modal:context-target">_association class_ notation</trigger> in the answer.%%

<modal large header="Relevant textbook topics" id="modal:context-target">

## Textbook → OOP → Associations →

<include src="../../book/oop/associations/associationClasses/container-inParent-asPanel.md" boilerplate />

----

## Textbook → UML → Class diagrams →
<include src="../../book/uml/classDiagrams/associationClasses/container-inParent-asPanel.md" boilerplate />
</modal>

<div class="indented-level2">

<include src="../../book/modeling/modelingStructures/objectOrientedDomainModels/q-courseDomainModel.md" />
</div>

2. {{ timing_badge("during the tutorial", "info") }}
   * Paste a screenshot/scan/photo of your answer in the online document.
   * Discuss a sample answer, as guided by the tutor.

#### {{ thumb(3) }} Exercise: Activity Diagrams

1. {{ timing_badge("before the tutorial", "danger") }} Do the following question, similar to the previous question.

<div class="indented-level2">

<include src="../../book/modeling/modelingBehaviors/activityDiagrams/q-modelWorkflowOfBurgerShop.md" />
</div>

2. {{ timing_badge("during the tutorial", "info") }} Post your answer and discuss, similar to the previous question.
