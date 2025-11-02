{% from "common/macros.njk" import embed_topic, get_date, show_faq with context %}

<div id="featureFlaws">

These are considered _feature flaws_:<br>
:fas-bug: The feature does not solve the stated problem of the intended user i.e., the feature is 'incomplete'<br>
:fas-bug: Hard-to-test features<br>
:fas-bug: Features that don't fit well with the product<br>
:fas-bug: Features that are not optimized enough for fast-typists or target users<br>
:fas-bug: Violations of given [project constraints](tp-constraints.md)
</div>

<div id="functionalityBugs">

These are considered _functionality bugs_:<br>
:fas-bug: Behavior differs from the User Guide<br>
:fas-bug: A legitimate user behavior is not handled %%e.g., incorrect commands, extra parameters%%<br>
:fas-bug: Behavior is not specified and differs from normal expectations %%e.g., error message does not match the error%%<br>
</div>

<div id="generalDocBugs">

<span id="visualsBugs">

:fas-bug: Use of visuals
* Not enough visuals e.g., screenshots/diagrams
* The visuals are not well integrated to the explanation
* The visuals are unnecessarily repetitive e.g., same visual repeated with minor changes
</span>
<span id="examplesBugs">

:fas-bug: Use of examples:
* Not enough or too many examples e.g., sample inputs/outputs
</span>
<span id="explanationBugs">

:fas-bug: Explanations:
* The target user for the product and/or the value proposition is not specified clearly.
* The explanation is too brief or unnecessarily long.
* The information is hard to understand for the target audience. e.g., using terms the reader might not know
</span>
<span id="neatnessBugs">

:fas-bug: Neatness/correctness:
* looks messy
* not well-formatted
* broken links, other inaccuracies, typos, etc.
* hard to read/understand
* unnecessary repetitions %%(i.e., hard to see what's similar and what's different)%%
</span>
</div>

<div id="ugBugs">

**These are considered UG bugs (if they hinder the reader):**<br>
<include src="tp-grading-bugs-fragment.md#generalDocBugs" />
</div>

<div id="dgBugs">

**These are considered DG bugs (if they hinder the reader):**

<panel type="seamless" header="Those given as possible UG bugs ...">
<include src="tp-grading-bugs-fragment.md#ugBugs" />
</panel>

<span tags="m--cs2103" id="architectureDiagramBugs">

:fas-bug: Architecture:
* Symbols used are not intuitive
* Indiscriminate use of double-headed arrows
* <tooltip content="e.g., the sequence diagram showing interactions between main components">_architecture-level_</tooltip> diagrams contain lower-level details
* Description given are not sufficiently high-level
</span>
<span id="umlDiagramBugs">

:fas-bug: UML diagrams:
* Notation incorrect or not compliant with the notation covered in the course.
* Some other type of diagram used when a UML diagram would have worked just as well.
* The diagram used is not suitable for the purpose it is used.
* The diagram is too complicated.
</span>
<span id="codeSnippetBugs">

:fas-bug: Code snippets:
* Excessive use of code e.g., a large chunk of code is cited when a smaller extract would have sufficed.
</span>
<span id="userStoryBugs">

:fas-bug: Problems in User Stories. Examples:
* Incorrect format
* All three parts are not present
* The three parts do not match with each other
* Important user stories missing
</span>
<span tags="m--cs2103" id="useCaseBugs">

:fas-bug: Problems in Use Cases. Examples:
* Important use cases missing
* Formatting/notational errors
* Incorrect step numbering
* Unnecessary UI details mentioned
* Missing/unnecessary steps
* Missing extensions
</span>
<span id="nfrBugs">

:fas-bug: Problems in NFRs. Examples:
* Not really a _Non-Functional_ Requirement
* Not scoped clearly (i.e., hard to decide when it has been met)
* Not reasonably achievable
* Highly relevant NFRs missing
</span>
<span id="glossaryBugs">

:fas-bug: Problems in Glossary. Examples:
* Unnecessary terms included
* Important terms missing
</span>
</div>

<div id="bugCalculationNotes">

##### Grading bugs found in the PE

* **Marks for finding bugs in the PE:** 3 marks. If you found 'enough' bugs (depends on how buggy the product was), you get full marks.<br>
  **Bugs found in your product:** determines 7 marks under the QA component, but in addition, also affect other components of the tP grade (e.g., documentation bugs affect the documentation component of the tP grade).
* **Bugs not accepted by the dev team**, if the non-acceptance is approved by the teaching team, will not affect marks of the tester or the developer.
* **The penalty/credit for a bug varies based on the severity** of the bug: `severity.High` > `severity.Medium` > `severity.Low` > `severity.VeryLow`
* **The three bug types (i.e., `type.FunctionalityBug`, `type.DocumentationBug`, `type.FeatureFlaw`) are counted for three different grade components.** The penalty/credit can vary slightly based on the bug type, but you may consider them as roughly equivalent. %%So, always choose the most suitable type for a bug rather than try to choose a type that benefits your grade.%%
* **The penalty for a bug is divided equally** among <popover content="In the PE, each team get to decide who are the assignees for each bug report they received">assignees</popover>.
* **Developers are not penalized for duplicate bug reports** they received but the testers earn credit for duplicate bug reports they submitted, provided the duplicates are not submitted by the same tester.<br>
  However, **<tooltip content="i.e., the same bug reported by many testers">_obvious_ bugs</tooltip> earn less credit** for the tester.
* **Excessive incorrect downgrading/rejecting/<tooltip content="marking as duplicates">duplicate-flagging</tooltip>**, if deemed an attempt to _game the system_, will be penalized.

{{ show_faq("tpMoreCodeMeansHigherPenalty") }}
{{ show_faq("tpTestingLessBuggyProducts", is_compact="1") }}
{{ show_faq("tpNoBugsInTestedProduct", is_compact="1") }}
{{ show_faq("tpNeedToFindAllBugs") }}
</div>
