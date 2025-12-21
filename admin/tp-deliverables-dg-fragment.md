{% from "common/macros.njk" import show_faq with context %}

{{ show_faq("dgDetailsLevel") }}

* The main content you add should be in the `docs/DeveloperGuide.md` file (for ease of tracking by grading scripts).<br>
  If you use PlantUML diagrams, commit the diagrams as `.puml` files in the `docs/diagrams` folder.
* **Should match the latest release of the product**.

<div tags="m--cs2113">

* **Follow the [AddressBook-Level3 (AB3) DG]({{ url_ab3_upstream_website }}/DeveloperGuide.html) structure**. Sections to include in your DG:
  * Design: similar to AB3 DG except,
    * you may omit the _Architecture_ section (no penalty)
    * if you have not organized the code into clearly divided components (no penalty if you didn't), you can use a single class diagram (if it is not too complicated) or use several class diagrams each describing a different area of the system.
  * Implementation: similar to AB3 DG
  * Appendix A: Product Scope
  * Appendix B: User Stories
  * Appendix C: Non-Functional Requirements
  * Appendix D: Glossary
  * Appendix E: Instructions for Manual Testing (more details below)
</div>

* **Ensure the 'Acknowledgements' section is accurate**: It should cite all ideas/code/documentation you reused. If you reused/adapted or even drew inspiration from other projects (including projects by past/current students), mention the extent of reuse and give hyperlinks to the original projects' GitHub page, UG, DG, etc. Examples:
  * %%The feature Foo was inspired by a similar feature of the past project [TaskPro]() ([UG](), [DG]()), although our implementation is entirely new.%%
  * %%The feature Bar (including the code) was reused with minimal changes from the same [TaskPro]() project.%%
* **{{ optional }} You can include proposed implementations of future features.**
* **{{ icon_important_big_red }} Include an appendix named _Instructions for Manual Testing_**, to give some guidance to the tester to chart a path through the features, and provide some important test inputs the tester can copy-paste into the app.
  * **Cover all user-testable features**<span tags="m--cs2103"> but no need to cover existing AB3 features if you did not touch them</span>.
  * **No need to give a long list of test cases** including all possible variations. It is upto the tester to come up with those variations.
  * Information in this appendix should _complement_ the UG. ==Minimize repeating information that are already mentioned in the UG.==
  * **Inaccurate instructions will be considered bugs**.
<div tags="m--cs2103">

* {{ icon_important_big_red }} **We highly recommend adding an appendix named _Appendix: Effort_** that evaluators can use to estimate the total project effort.
  * Keep it brief (~1 page)
  * Explain the difficulty level, challenges faced, effort required, and achievements of the project.
  * If a significant part (e.g., more than 5%) of the effort was saved through reuse, mention what you reused and how it affected the effort %%e.g., the feature X is implemented using library Foo -- our work on adapting Foo to our product is contained in class `FooAdapter.java`%%.
  * Use AB3 as a reference point %%e.g., you can explain that while AB3 deals with only one entity type, your project was harder because it deals with multiple entity types%%.
</div>
<div tags="m--cs2103" id="planned-enhancements-info">

* {{ icon_important_big_red }} **We highly recommend adding an appendix named _Planned Enhancements_**, listing fixes you propose to add in the near future, to counter known feature flaws that you are not allowed to fix in {{ version_final }}.<br>
  **Enhancements listed in this section will be immune from the PE bug reporting** i.e., they will not be penalized if reported as bugs during the PE.
  * This can be added _after_ the PE-D is over (and PE-D bug reports have been received).
  * This section may contain up to `team_size x 2` enhancements %%e.g., a 5-person team can have up to 10 enhancements%%.
  * At the start of the section, clearly state the team size. While this information is not useful for a real DG, it will help PE testers easily see if you have exceeded the allowed planned enhancements count.<br>
    For a similar reason, structure this section as a numbered list, each item in the list describing exactly one planned enhancement.<br>
    Each enhancement should be specific, describing the feature flaw it addresses and how exactly the feature will be changed, providing sample UIs/inputs/outputs if applicable. e.g.,
    > ****Planned Enhancements****
    >
    > Team size: 5
    >
    > 1. **Make 'failed contact deletion' message more specific**: The current error message for a failed contact deletion `Operation failed!` is too general. We plan to make the error message also mention which action failed and the reason for the failure: `The contact Amy Lee could not be deleted as it is referenced by another contact Ben Chua`.
    > 2. ...
  * Each enhancement should be a tweak to an existing feature, and should not be a new feature altogether.
  * `type.FeatureFlaw` bug reports matching an item in this section ==will not be penalized== for the team, and testers will not earn credit for reporting them either. However, testers can report `type.FeatureFlaw` bugs on the enhancements listed in this section, if they think the planned feature tweak itself is flawed/inadequate.

{{ show_faq("tpCountingSimilarPlannedEnhancements") }}

* <span class="text-danger">If the team has exceeded the allowed count in the planned enhancements</span>, only the first N items (where N is `team size x 2`) in that list will have immunity. The rest can be reported as bugs. In addition, exceeding the count can be reported as a separate DG bug.
</div>
<div tags="m--cs2103">

* **What to do with other dev docs** linked from the DG e.g., [_Setting up and getting started_ guide](https://se-education.org/addressbook-level3/SettingUp.html)?
  * They are not part of the tP deliverables, and are not graded.
  * You are welcome to (but not required to) update them. If you do, the work can be counted as a tP contribution.
  * The normal course of action is to just leave them be. It's fine if they are outdated and doesn't match with your current product anymore.
  * But best not to delete them altogether, as that can result in broken links in your DG page.

{{ show_faq("tpDgKeepingProposedFeatures") }}

 * **The _Appendix: Requirements_ section** should be updated as follows:
   * Requirements implemented in the current version: make sure requirements match the way they are actually been implemented (e.g., use case steps).
   * Requirements yet to be implemented: keep these as well, as this is an ongoing project and these are meant to be implemented in future iterations.
</div>

##### DG Tips

<div id="dgTips">

* **Aim to showcase your documentation skills.** The primary objective of the DG is to explain the design/implementation to a future developer, but a secondary objective is to serve as evidence of your ability to document deeply-technical content using prose, examples, diagrams, code snippets, etc., appropriately. To that end, you may also describe features that you plan to implement in the future, even beyond {{ version_final }} (hypothetically).<br>
  For an example, see [the description of the undo/redo feature implementation in the AddressBook-Level3 developer guide]({{ url_ab3_upstream_website }}/DeveloperGuide.html#proposed-undoredo-feature).
* **Use multiple UML diagram types.** Following from the point above, try to include UML diagrams of multiple types to showcase your ability to use different UML diagrams.

{{ show_faq("dgAddNewUml") if cs2103 }}
{{ show_faq("noEffectOnUml") if cs2103 }}
{{ show_faq("umlWhenNotationNotEnough") }}


* **Diagramming tools**:
  * AB3 uses PlantUML (see the guide [_Using PlantUML_ @SE-EDU/guides](https://se-education.org/guides/tutorials/plantUml.html) for more info).

{{ show_faq("tpOtherDiagrammingTool") }}
{{ show_faq("tpIdeGeneratedDiagrams") }}


* **Keep diagrams simple.** The aim is to make diagrams ==_comprehensible_, not necessarily _comprehensive_==.<br>
  Ways to simplify diagrams:
  * **Omit less important details**. Examples:
    * a class diagram can omit minor utility classes, private/unimportant members; some less-important associations can be shown as attributes instead.
    * a sequence diagram can omit less important interactions, self-calls, method parameters, etc.<br>
      {{ icon_tip }} You can use `...` (e.g., `foo(...)`) to indicate parameters have been omitted.<br>
      {{ icon_tip }} You can use pseudocode instead of exact method calls e.g., `save data in file` instead of `saveData(content, filename)`.<br>
      {{ icon_tip }} Omit intricate details that complicated the diagram unnecessarily they add to the diagram e.g., exception handling (`throw`/`catch`), lambdas, calls to anonymous methods, etc.<br>
      If you feel they are important to the purpose of the diagram (i.e., omitting them can mislead the reader), you can use a UML note to mention that information (as plain text) in the diagram.
  * **Omit repetitive details** e.g., a class diagram can show only a few representative ones in place of many similar classes (note how the <trigger trigger="click" for="modal:ipWeek10-logicClassDiagram">AB3 Logic class diagram</trigger> shows concrete `*Command` classes using a placeholder `XYZCommand`).
  * **Limit the scope of a diagram.** Decide the purpose of the diagram (i.e., what does it help to explain?) and omit details not related to it.<span tags="m--cs2103"> In particular, avoid showing lower-level details of multiple components in the same diagram unless strictly necessary e.g., note how  <trigger trigger="click" for="modal:ipWeek10-deleteSd">this sequence diagram</trigger> shows only the detailed interactions within the Logic component i.e., does not show detailed interactions within the model component.</span>
  * **Break diagrams into smaller fragments** when possible.
    * If a component has a lot of classes, consider further dividing into subcomponents (e.g., a Parser subcomponent inside the Logic component). After that, subcomponents can be shown as black-boxes in the main diagram and their details can be shown as separate diagrams.
    * You can use `ref` frames to break sequence diagrams to multiple diagrams.{% if cs2103 %} Similarly, `rake`s can be used to divide activity diagrams.
  * **Stay at higher levels of abstraction** e.g., note how <trigger trigger="click" for="modal:ipWeek10-archiSd">this sequence diagram</trigger> shows only the interactions between architectural components, abstracting away the interactions that happen inside each component.{% endif %}
  * **Use visual representations** as much as possible. E.g., show associations and navigabilities using lines and arrows connecting classes, rather than adding a variable in one of the classes.
  * For some more examples of what NOT to do, see <trigger trigger="click" for="modal:ipWeek10-umlExamples">here</trigger>.
* **Integrate diagrams into the description.** Place the diagram close to where it is being described.
* **Use code snippets sparingly.** The more you use code snippets in the DG, and longer the code snippet, the higher the risk of it getting outdated quickly. Instead, use code snippets only when necessary and cite only the strictly relevant parts only. You can also use pseudocode instead of actual programming code.
* **Resize diagrams** so that the text size in the diagram matches the text size of the main text of the diagram. See <trigger trigger="click" for="modal:ipWeek10-diagramSizeNegative">example</trigger>.


<modal large header="UML Diagrams: Negative Examples " id="modal:ipWeek10-umlExamples">

  These class diagrams seem to have lots of member details, which can get outdated pretty quickly:<br>
  <pic eager src="https://cs2103-ay1819s1-w10-3.github.io/main/images/PollClassDiagram.png" width="750"></pic><br>
  <pic eager src="https://cs2103-ay1819s1-w10-4.github.io/main/images/healthPlanClassDiagram.png" width="750"></pic>

  <hr>
  This class diagram seems to have too many classes:<br>
  <pic eager src="https://cs2103-ay1819s1-f10-1.github.io/main/images/ModelClassDiagram.png" width="750"></pic>

  <hr>
  These sequence diagrams are bordering on 'too complicated':<br>
  <pic eager src="https://cs2103-ay1819s1-w13-1.github.io/main/images/TagCommandSequenceDiagram.png" width="750"></pic>
  <p/>
  <pic eager src="https://cs2103-ay1819s1-f10-1.github.io/main/images/modifyPermissionSequenceDiagram.png" width="750"></pic>

</modal>

<modal large header="Diagram resizing: a negative example" id="modal:ipWeek10-diagramSizeNegative">

In this negative example, the text size in the diagram is much bigger than the text size used by the document:<br>
<pic eager src="images/diagramSizeNegativeExample.png" width="200"></pic><br>
It will look more 'polished' if the two text sizes match.
</modal>

<modal large header="AB3 - Class Diagram of the Logic Component" id="modal:ipWeek10-logicClassDiagram">
  <pic eager src="{{ url_ab3_upstream_website }}/images/LogicClassDiagram.png" width="900"></pic>
</modal>

<modal large header="AB3 - Sequence Diagram for the `delete` command" id="modal:ipWeek10-deleteSd">
  <pic eager src="{{ url_ab3_upstream_website }}/images/DeleteSequenceDiagram.png" width="900"></pic>
</modal>

<modal large header="AB3 - Architecture-Level Sequence Diagram" id="modal:ipWeek10-archiSd">
  <pic eager src="{{ url_ab3_upstream_website }}/images/ArchitectureSequenceDiagram.png"></pic>
</modal>
</div>