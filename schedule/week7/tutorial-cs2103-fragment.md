{% from "common/macros.njk" import embed_topic, thumb, show_as_tab, timing_badge with context %}
{% from "_course-" + course + "/studentData-fragment.md" import team_review_allocation with context %}

#### {{ thumb(1) }} Exercise on Requirements: PR Tracker

* {{ timing_badge("10 minutes", "info") }} **Write the answers to the following questions**. You can write your answers in a local document file %%(e.g., a Word doc)%% first; when done, paste a screenshot in the workspace document. %%Writing the answer directly in the workspace document might result in too much lag.%% {text="1.1"}

   <box>

   %%{{ icon_info }} Question adapted from a past exam paper.%%

   <span class="text-monospace">Pull Request Tracker (PRT) is a desktop application meant to help tutors of a Software Engineering course deal with GitHub PRs more efficiently (compared to the GitHub Web interface). For example, it will help tutors find and review PRs from their _mentees_ easily. It will help the _managers_ of the course (e.g., professor, head TA) to easily keep track of how tutors are dealing with mentee PRs. PRT will communicate with GitHub using the GitHub API.</span>

   1. Write 1 must-have and 1 nice-to-have user stories, covering user types `tutor` and `manager`.
   1. Write at least 1 <tooltip content="Non-Functional Requirements">NFRs</tooltip>, related to performance/scalability and/or usability.
   1. Give at least 1 terms worth recording in the glossary.
   1. Complete the following use case. Give at least one extension. Note that the tutor should give comments in the order of PR size (i.e., give comments to smaller PRs first). Assume the following use cases exists already: `U1. Sort PRs by a criterion`, `U2. Add comments to a PR`

   <div class="indented-level2 text-monospace"><blockquote>


   System: PRT<br>
   Use Case: U3. Add comments to mentee PRs<br>
   Actor: ...<br>
   Precondition: ...<br>

   ...
   </blockquote>
   </div>

   </box>

* **Check a peer answer (provided by the tutor) for the bugs listed below** and discuss, as directed by the tutor. {text="1.2"}

{{ embed_topic("../../admin/tp-grading-bugs-fragment.md#userStoryBugs", "Admin " + icon_embedding + " tP Grading → DG Bugs → User Story → Possible Bugs", "3", indent="2", status="expanded", type="danger") }}
{{ embed_topic("../../admin/tp-grading-bugs-fragment.md#nfrBugs", "Admin " + icon_embedding + " tP Grading → DG Bugs → NFR → Possible Bugs", "3", indent="2", status="expanded", type="danger") }}
{{ embed_topic("../../admin/tp-grading-bugs-fragment.md#glossaryBugs", "Admin " + icon_embedding + " tP Grading → DG Bugs → Glossary → Possible Bugs", "3", indent="2", status="expanded", type="danger") }}
{{ embed_topic("../../admin/tp-grading-bugs-fragment.md#useCaseBugs", "Admin " + icon_embedding + " tP Grading → DG Bugs → Use Case → Possible Bugs", "3", indent="2", status="expanded", type="danger") }}


#### {{ thumb(2) }} Refine your DG {{ timing_badge("after the tutorial", "secondary") }}

* After the tutorial, if applicable, refine the relevant sections of your own DG based on what you learned from the tutorial activities.<br>
  Note: Ideally, you should have completed iteration `{{ version_practice }}` already. In that case, this DG refinement can be done as part of a subsequent iteration (e.g., `{{ version_first }}`)
