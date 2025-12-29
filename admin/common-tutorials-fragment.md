{% from "common/macros.njk" import embed_topic, show_faq, show_gm_lesson_link, step, thumb, timing_badge with context %}

<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="form-teams">

* Form teams, under the guidance of the tutor. See the panel below for _team forming constrains_ and other related info.<br>

{{ embed_topic(baseUrl+"/admin/tp-teams.md#main", "Admin " + icon_embedding + " **Teams → Team Forming Constraints**", "2", indent="1") }}
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="register-the-team">

* Get your team ID from the tutor. ==Each student must submit your team ID== via the Canvas `Class Groups` page -- for us to know which team you joined. Note the team ID follows a specific format.

{{ embed_topic("tp-teams.md#teamIdFormat", "Admin " + icon_embedding + " **Teams → Team ID Format**", "2", indent="2") }}
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="introduce-yourselves">

* Introduce yourself to the tutor and the members of your team and the _partner_ team (i.e., the other team under your tutor)
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="decide-meeting-time">

* If you haven't done so already, do the following tP task.

{{ embed_topic("tp-tasks-fragment.md#desc_set_up_meeting_time", "Admin " + icon_embedding + " **tP → Set up a meeting time**", "2", indent="1") }}
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="exercise-coding-standard-violations">

<box type="warning" seamless>

Learning goals of this exercise:

1. **Learn to carefully cross-refer the coding standard, and objectively identify rule violations.** This is not a memory test. No guesswork or speculations please.
1. **To learn not to mix up coding standard violations with other code quality issues.** The exercise asks you to identify coding standard violations only.

So, for each coding standard violation you identify, you should be able to trace it back to a rule in the [Java coding standard](https://se-education.org/guides/conventions/java/{{ 'intermediate' if cs2103 else 'basic'}}.html).

</box>

<div class="indented">

<include src="..\book\codeQuality\followStandard\basic\q-listViolations.md" />
</div>
<p/>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="help-troubleshoot-ip">

* If there is time, do the following tP task (if there isn't enough time, you can do this later during the week).

{{ embed_topic("tp-tasks-fragment.md#desc_check_collective_ip_status", "Admin " + icon_embedding + " **tP → Check collective iP status**", "2", indent="1") }}
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="share-project-direction">

* Show your collaborative project doc to others.
* Share the project direction, user profile, value proposition you have decided upon.
* Give feedback to the other team. Some examples:
  * Suppose you belong to the proposed target user group; do you find the value proposition attractive?
  * Do you foresee any potential violation of the project constraints?
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->

{% macro get_pr_link(username) -%}[{{ username }}]({{ url_course_org }}/{{ ip_repo_name }}/pulls/{{ username }}){%- endmacro %}
<div id="show-ip-peer-review-allocation-1">
<panel header="**Review allocation for the ==first== PR review** (click to expand)" minimized >
{% from "_course-" + course + "/studentData-fragment.md" import ip_pr_review_allocation with context %}
<d-table sortable searchable>
Tutorial | Reviewer | First PR to review | Backup PR to review
---------|----------|--------------------|---------------------
{% if not ip_pr_review_allocation | length %}Allocation ... | ... not ... | .... available yet. {% else %}{% for line in ip_pr_review_allocation %} {{ line[0] }} | {{ line[1] }} | {{ get_pr_link(line[2]) }} | <small>%%backup:%% {{ get_pr_link(line[3]) }}</small>
{% endfor %}{% endif %}
</d-table>
</panel>
<p/>

<div tags="m--cs2113 m--cs2103">

{{ icon_info }} If the student you have been allocated to review has not created a PR (or the PR has a trivial amount of code), you can review the _Backup PR to review_ provided in the allocation table. Failing both, review another PR allocated to another student in your own tutorial !!but not in your team!!.
<p/>

<box type="tip" light>

Tip for future reference: GitHub allows you to filter PRs/Issues using various criteria such as `author:AuthorUsername` ([example](https://github.com/reposense/RepoSense/pulls?utf8=%E2%9C%93&q=is%3Apr+author%3Afzdy1914+) -- see the `filters` text box in the target page).

Alternatively, you can use PR labels (if any) to filter PRs/Issues.<br>
<pic eager src="images/filterPrsUsingLabels.png"></pic>
</box>

:fas-question-circle: FAQ: How many comments should I add? Answer: Depends on the code being reviewed but we expect most PRs would warrant at least 4-5 comments. If the PR is huge, you can stop when you think you've put in a fair amount of time on the job (~15 minutes) and added enough comments for the PR author to receive some value.
</div>

</div>
<div id="show-ip-peer-review-allocation-2">
<panel header="**Review allocation for the ==second== PR review** (click to expand)" minimized >
{% from "_course-" + course + "/studentData-fragment.md" import ip_pr_review_allocation with context %}
<d-table sortable searchable>
Tutorial | Reviewer | Second PR to review | Backup PR to review
---------|----------|---------------------|---------------------
{% if not ip_pr_review_allocation | length %}Allocation ... | ... not ... | .... available yet. {% else %}{% for line in ip_pr_review_allocation %}{{ line[0] }} | {{ line[1] }} | {{ get_pr_link(line[4]) }} | <small>%%backup:%% {{ get_pr_link(line[5]) }}</small>
{% endfor %}{% endif %}
</d-table>
</panel>
<p/>

{{ icon_info }} If the allocated PR is not suitable, use the same strategy as before to find an alternative PR to review.
<p/>

</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="demo-debugging-using-personbook">

<box light type="success" add-class="ml-4" icon=":fas-lightbulb:">

**Suggested pre-tutorial preparations**:
* Clone the [{{ url_course_org }}/personbook]({{ url_course_org }}/personbook) repo to your Computer (no need to fork first).
* Set it up in your IDE.
* Use the IDE debugging to step through the code to understand how the code works. For example, you can try to find answers to these questions:
  * How to add a new `find` command to locate persons by name?
  * What's the purpose of the variable `PersonBook#lastShownList`? Is it really needed?

<panel type="seamless" header="FYI, here's a relevant video used in the textbook">

@[youtube](1bCgzjatcr4)

</panel>

</box>

<div class="indented">

During the tutorial, **demo your ability to do debugging using an IDE** by performing the following tasks:

1. Set a breakpoint in the following method of the `Main` class.
   ```java
   /** Reads the user command and executes it, until the user issues the exit command.  */
   private void runCommandLoopUntilExitCommand() {
       Command command;
       do {
           String userCommandText = ui.getUserCommand();
           command = new Parser().parseCommand(userCommandText);
           CommandResult result = executeCommand(command);
           personBook.setLastShownList(result.getRelevantPersons());
           ui.showResultToUser(result);

       } while (!ExitCommand.isExit(command));
   }
   ```
1. Use the debugger to step through the code while explaining how the code works. Start from the `main` method.
1. Suppose the code behaves incorrectly when using the `list` command after adding two persons. Show how to set a conditional breakpoint so that execution pauses when the user types in the command `list` but doesn't pause for other commands.<br>
   {{ icon_tip }} You need to set what is known as a _conditional breakpoint_.
</div>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="demo-ip-using-jar">

* Copy your iP jar file to an empty folder.{% if cs2113 %}
* Launch the jar file using the command prompt.
* Input the commands specified by your tutor.
* Take screenshots and paste them in the _tutorial workspace_ document as instructed.{% else %}
* Launch the jar file using the command prompt and type a command.
* Take a screenshot and paste in the _tutorial workspace_ document.
{% endif %}
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="setup-tp-org-repo">

* To be done as a team.
* Set up the team org, team fork, individual forks as described below:

{{ embed_topic("appendixE-gitHub.md#organization-setup", "Admin " + icon_embedding + " Appendix E (extract): **Organization Setup**", "1", indent="2") }}
{{ embed_topic("appendixE-gitHub.md#tp-team-repo-setup", "Admin " + icon_embedding + " Appendix E (extract): **tP Team Repo Setup**", "1", indent="2") }}
{{ embed_topic("appendixE-gitHub.md#tp-individual-fork-setup", "Admin " + icon_embedding + " Appendix E (extract): **tP Individual Fork Setup**", "1", indent="2") }}

* **[Each person] Verify that you know how to do the following** by performing each on your computer and posting a screenshot in the _tutorial workspace_ document:
  * run the code in your IDE
  * run I/O redirection tests
  * verify compliance with the coding standard automatically using Gradle
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="update-code-using-forking-workflow">
<div class="indented">

**In this activity you will be using the forking workflow to do some simple updates to the codebase** while working in parallel. The objective is to ensure you know how to follow the expected working in the tP. The steps are given below:

**First, ensure that you know how the _forking workflow_ works.** See {{ show_gm_lesson_link("forkingWorkflow", "T10L2. Forking Workflow (with Branching)") }} for more details.

**Next, add the `upstream` as a remote**: The forking workflow requires you to pull from the team repo and push to your own fork. To be able to do the former, you need to **add the team repo as a _remote_ of your clone** (if you don't remember how to add a remote to a repo, see {{ show_gm_lesson_link("setRemote", "T2L4. Linking a Local Repo With a Remote Repo") }}. Add a new remote with the _Remote name_ `upstream` (can be anything, but `upstream` is a common choice) and _URL / Path_ pointing to the team repo<br>
    e.g., `https://github.com/{{ semester }}-{{ example_team_id }}/{{ tp_repo_name }}.git` (==note the `.git` at the end==)

**Now, follow these steps to update the code using the forking workflow** e.g., each person can add their details to the `docs/AboutUs.md` page:
* {{ step(1) }} Decide which update each person will do.
* {{ step(2) }} Each person,
  *  {{ step('2.a') }} create a branch (e.g., `johnDoe-AboutUs`) in their local repo.
  *  {{ step('2.b') }} do the change in the branch.
  *  {{ step('2.c') }} push the branch to their own fork.
  *  {{ step('2.d') }} create a PR from their branch in the fork to the `master` branch of the team repo.
* {{ step(3) }} Work as a team to merge one PR at a time.
  * If a PR cannot be merged due to conflicts, resolve conflicts as you go (PR conflict resolution was covered in the week 6 lecture activity).
  * <span class="text-danger">Do not send PRs from team repo to individual repos</span> as that goes against the forking workflow. PRs should only go from forks to the team repo.
  * For reference, PR merging instructions are in {{ show_gm_lesson_link("prsMerge", "T9L3. Merging Pull Requests") }}:

* {{ step(4) }} Everyone sync their local repo and the fork with the team repo (see the last paragraph in the panel above)
</div>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="demo-junit-tests">

* Run JUnit test of your tP.
* Take a screenshot of the results and post in the _tutorial workspace_ document.
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="interpret-person-class-diagram">

* Do the following exercise as directed by the tutor.

<div class="indented-level2">

<include src="../book/modeling/modelingStructures/classDiagramsBasic/q-essay-explainClassDiagram.md" />
<p/>
</div>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="hand-drawing-diagrams">
<box type="info">

<pic eager src="images/drawingDiagrams.png" add-class="float-end me-2 ms-2">

<small>[Image source: [this article](https://medium.com/deekit-central/7-reasons-why-engineers-are-the-whiteboard-artists-c40acff8b0ed)]</small>
</pic>
**_Hand-drawing_ diagrams on a white-board and on paper is an important practical skill** %%(e.g., for technical interviews, project discussions)%%. It's possible that the diagrams first few UML hand drawing attempts to feel laborious/slow, and the result look amateurish/ messy/hard-to-read. With more practice, you will be able to draw such diagrams quicker %%(e.g., draw as you explain verbally your design)%%, with less need for corrections, and the diagrams will look more _professional_ too.

That is why we have structured these tutorials to get everyone to practice this skill so that **your first few (not-so-good) diagram drawing attempts to happen in the course, rather than in an interview or during your internship.**

Note the following:
* Draw ==on paper or on a whiteboard or use a free-hand drawing software== (e.g., Bamboo Paper). If latter, do not use UML software or predefined shapes.
* For the same reason, don't use rulers.
* When the tutor asks you to, take a screenshot or a photo of the drawing and post in the _tutorial workspace_ document.
* {{ icon_tip }} There are mobile apps ([example](https://apps.apple.com/sg/app/evernote-scannable/id883338188)) that can take a photo of a document and convert it to a high-quality scan.
</box>
{% if cs2103 %}<box type="tip">

**[Recommended] Do the following before attempting the tutorial tasks**

1. Do this week's Canvas quiz Part I, to self-test your memory of the required UML notation. You will be able to see the correct answer immediately after submitting answers.
1. Watch at least some of the [UML drawing step-by-step example videos](../schedule/week8/topics.html) provided.
</box>{% endif %}
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="draw-person-guardian-object-diagram">

<!--* Split into sub-teams of 2-3 persons and draw the following exercise on the white board. -->
<div class="indented-level2">

<include src="common-tutorials-fragment.md#hand-drawing-diagrams" />
</div>

* **Do the following exercise** while noting the info in the box above.

<div class="indented-level2">

<include src="../book/uml/classDiagrams/combine/basic/q-essay-objectDiagramsForClassDiagram.md" />
<p/>
</div>

* **Discuss answers** as guided by the tutor.
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="draw-box-etc-class-diagram">

* Do the following similar to the earlier exercise.
<div class="indented-level2">

<include src="../book/modeling/modelingStructures/classDiagramsBasic/q-essay-drawClassDiagramForBoxEtc.md" />
<p/>
</div>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="demo-assertion-failure">

* Temporarily edit the tP code to cause an assertion failure. Demo the assertion failure by running the app.<br>
  For example, you can add the following assertion at the start of the `main` method and then run `gradlew run`.
  ```java{.no-line-numbers highlight-lines="3" heading="your main class"}
  ...
  public static void main(String[] args){
      assert false : "dummy assertion set to fail";
      ...
  }
  ```
* Post a screenshot of the assertion failure in the _tutorial workspace_ document.
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="interpret-course-cd">

* {{ timing_badge("10 minutes", "info") }} With the tutor's guidance, interpret the following class diagram, focusing on the new CD notations that you learned this week.

<div class="indented-level2">

<include src="../book/modeling/modelingStructures/classDiagramsIntermediate/q-explainClassDiagramNotation.md" />
<p/>
</div>

* Some questions you can try to answer:
  1. What does this mean? <pic eager src="images/interpret-course-cd/extract-interface.png"></pic>
  1. What does this mean? <pic eager src="images/interpret-course-cd/extract-inheritance.png"></pic>
  1. Of the above two, why the lines in one are dashed?
  1. What does this mean? <pic eager src="images/interpret-course-cd/extract-dependence.png"></pic>
  1. What's the difference (w.r. t. what it means) between the above and a normal association?
  1. What does this mean? <pic eager src="images/interpret-course-cd/extract-composition.png"></pic>
  1. What's the difference if the diamond is empty?
  1. Can a `PR` object exist without any `Commit` objects attached to it?
  1. Can a `Commit` object exist without a corresponding `PR` object?
  1. A `Student` can belong to how many teams?<pic eager src="images/interpret-course-cd/extract-team.png"></pic>
  1. A `Team` can have how many `Student` objects?
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="draw-stock-cd">

<!--
* **Divide into two sub-teams** as you did in the previous week.
* {{ timing_badge("10 minutes", "info") }} **Each sub-team do the part (a)** of the following exercise, by drawing the answer on the whiteboard. Use the following layout:<br>
  <pic eager src="images/classLayout.png" width="600"></pic>

<div class="indented-level2">

<include src="../../book/modeling/modelingStructures/classDiagramsIntermediate/q-drawClassDiagramForItemEtc.md" />
</div>
<p/>

* {{ timing_badge("5 minutes", "info") }} **Compare answers with those from other sub-teams**. With the tutor's guidance, self-evaluate the answers.
* {{ timing_badge("5+5=10 minutes", "info") }} **Do part (b)** in the same manner.
-->

<div class="indented">

{{ icon_info }} Question adapted from past exam paper.
</div>

1. {{ timing_badge("before the tutorial", "danger") }} **Do the following exercise**, by ==hand-drawing== the answer.<br>
   Use the following layout:<br>
   <pic eager src="images/draw-stock-cd/classLayout.png" width="600"></pic>

<div class="indented-level2">

<include src="../book/modeling/modelingStructures/classDiagramsIntermediate/q-drawClassDiagramForItemEtc.md" />
<p/>
</div>

2. {{ timing_badge("first few minutes of the tutorial", "warning") }}
   * Paste the diagram (take a photo if you drew on paper) in the _tutorial workspace_ document.
   * **Discuss answers** as guided by the tutor.
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="draw-sd-personlist">

1. {{ timing_badge("before the tutorial", "danger") }}

<div class="indented-level2">

**(a) Do the following exercise** similar to the previous one.

<include src="../book/modeling/modelingBehaviors/sequenceDiagramsBasic/q-essay-drawSequenceDiagramForPerson.md" />
<p/>

**(b) How would you update the diagram** if the `PersonList` class was updated as follows?

```java
class PersonList{
    void addPerson(Person p){
        add(p);
    }

    void add(Person p){
        //...
    }
}
```
</div>


2. {{ timing_badge("first few minutes of the tutorial", "warning") }}:

<div class="indented">

* As before, paste the diagram in the _tutorial workspace_ document, and take part in the follow-up discussion, as guided by the tutor.


</div>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="demo-test-coverage">

* {{ timing_badge("before the tutorial, or in the first 10 minutes", "warning") }} Measure test coverage in your own iP using your IDE. Take a screenshot showing test coverage details such as lines covered, lines not covered, percentage of coverage for different files etc.

{{ embed_topic("../book/testing/testCoverage/text.md#body", "Textbook " + icon_embedding + " Testing → **Test Coverage**", "3", indent=1) }}

* When prompted by the tutor, post the screenshot in the _tutorial workspace_ document. An example is given below:<br>
 <pic eager src="images/demo-test-coverage/CoverageReportExample.png" ></pic>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="interpret-parserfactory-sd">

* Do the following exercise, as guided by the tutor.
<div class="indented-level2">

<include src="../book/modeling/modelingBehaviors/sequenceDiagramsIntermediate/q-essay-expainParserFactory.md" />
<p/>
</div>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="draw-quote-sd">

* Do following exercise. Remember to hand-draw the diagram and post a scan/photo in the _tutorial workspace_ after you ar done.

<div class="indented-level2">

<include src="../book/modeling/modelingBehaviors/sequenceDiagramsIntermediate/q-drawPrintQuoteSd.md" />
<p/>
</div>

* Discuss answers, as guided by the tutor.
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="review_others_dg">

<box type="info">
Do the following tP task.
</box>

<include src="tp-tasks-fragment.md#desc_review_others_dg" />
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="design-test-cases-isvalidday">

* ~~Divide into two subteams and do the following exercises on the white board.~~

<div class="indented-level2">
  <include src="../book/testCaseDesign/summary/exercises/q-essay-dayParameter.md" />
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="no-tutorial-take-a-break">

<box type="info">

No tutorial this week.

</box>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="tp-project-demo">

<box type="info">

This tutorial is used for tP project demos. Demo instructions are repeated below for your easy reference.
</box>

<include src="tp-tasks-fragment.md#demo-instructions" />
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="no-more-tutorials">

<box type="info" seamless>

**No tutorial this week.**

{% if cs2103 %}* **Recording of past tutorials** should now be available in the `Recordings.docx` of your tutorial's MS Teams. If not, remind your tutor to update that document with the recording links.{% endif %}
* **If you have questions related to past tutorials**, you can post them in your tutorial's MS Teams channel, and tag the tutor. If there is no reply within a reasonable time (e.g., 24 hours), remind the tutor via another means (e.g., via his/her email, given [here](instructors.md)).
* **Any queries regarding admin matters** should be sent to the course email (`cs2103@nus.edu.sg`) or posted in the [course forum]({{ url_forum }}) (do not send them to the tutor).
</box>

</div>
