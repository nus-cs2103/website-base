{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/topics.njk" import panopto, topic_preamble with context %}
{% from "common/macros.njk" import as_tag, button, embed_topic, get_date, show_faq, step, thumb, timing_badge with context %}
{% from "_course-" + course + "/weeklyIpTasks-fragment.md" import weekly_ip_tasks with context %}

{#====================================================================================================================
 # Common text segments
 #====================================================================================================================#}
<div id="ip-faq">
<box type="info" icon=":fas-question-circle:" light>

#####  **FAQ** about iP increments{.text-info}

{{ show_faq("ipHowTagsUsed") }}
{{ show_faq("ipBugAfterIncrementDone") }}
{{ show_faq("ipMultipleIncrementsInSameCommit") }}
{{ show_faq("ipIncrementAlreadyDone") }}
{{ show_faq("ipForgotToPushTag") }}
{{ show_faq("ipIncorrectTagOrBranch") }}
</box>
</div>
<div id="order">

**Implement the <tooltip content="in this context, an _increment_ is a Duke _level_ or a Duke _extension_">increments</tooltip> given below ==in the given order==.**
</div>
<div id="commit">

* From this point onward, commit code at important points. ==Minimally, commit after completing each increment==.<br>
  {{ icon_important_big_red }} Remember not to commit `.class` files and any other file that should not be revision controlled.
</div>
<div id="tag-push">

* From this point onward, after completing each increment,
  * **`git tag` the commit that _completed_ the increment with the exact increment ID** e.g., {{ as_tag('Level-2') }}, {{ as_tag('A-TextUiTesting') }}
    <box type="warning" seamless><md>[Git tags](../book/gitAndGithub/tag/) are not the same as [Git commit messages](../book/gitAndGithub/commit/).</md></box>
    <mermaid>
    {{ "%%{init: { 'theme': 'default', 'gitGraph': {'mainBranchName': 'master'}} }%%" }}
    gitGraph
      commit id: "..."
      commit id: "Rename main class"
      commit id: "Add greeting" tag: "Level-0"
      commit id: "Add support for echo"
      commit id: "Fix bug in echo" tag: "Level-1"
      commit id: "Add support for list"
      commit id: "Add support for bye"
    </mermaid>
  * **`git push` the code to your fork**
    <box type="warning" seamless><md>Git doesn't push tags unless you [specifically ask it to](../book/gitAndGithub/push/).
    After pushing a tag to your fork, you should be able to see that tag by visiting `https://github.com/YOUR_USER_NAME/REPO_NAME/tags` e.g., https://github.com/se-edu/addressbook-level3/tags</md></box>
    <box type="tip" seamless><md>If you encounter issues connecting Sourcetree with your GitHub account, refer to this [Sourcetree Tutorial](https://se-education.org/guides/tutorials/sourcetree.html).</md></box>
* The relevant textbook topics are:
   {{ embed_topic("../book/gitAndGithub/commit/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Committing**", "1", indent=1) }}
   {{ embed_topic("../book/gitAndGithub/tag/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Tagging**", "1", indent=1) }}
   {{ embed_topic("../book/gitAndGithub/push/text.md#simple-push", "Textbook " + icon_embedding + " Git & GitHub → **Pushing**", "1", indent=1) }}
</div>
<div id="take-note-of-plagiarism" >

* Remember to take note of our plagiarism policies, if you haven't done so already:

{{ embed_topic("policies-fragment.md#policy-reuse", "Admin " + icon_embedding + " Policies → **Reuse**", "1", indent=1, type="danger") }}

</div>
<div id="volatile-requirements">

<box type="info">

The individual project (iP) and the team project (tP) undergoes changes after each semester. As such, teething issues are a possibility. If you encounter any problem while doing the iP/tP, please post in the [forum]({{ url_forum }}) so that we can take necessary actions.
</box>
</div>
<div id="no-jumping-ahead">

<box>

{{ icon_important_big_red }} We discourage you from doing project tasks allocated to future weeks, although it is fine to stay ahead of the schedule a bit (but no more than a week ahead).<br>
Reasons: In order to help you gain <tooltip content="the ability to apply knowledge or do tasks effortlessly as if you have been doing them for a long time">_fluency_</tooltip> (and also to better simulate real projects), **we want the project work to be <tooltip content="done at multiple times with time gaps in between">_spaced_</tooltip> and spanned over a longer period**, rather than to be done as a short burst.

Reminder: As per iP grading criteria, _some_ increments need to be done in each week. Clumping all the iP work into a short burst of work will not earn you full marks.
</box>
</div>
<div id="follow-instructions">

<box>

{{ icon_important_big_red }} Please follow instructions carefully. Any deviations can cause our grading scripts to miss your work (and result in you not getting credit for the work).

</box>
</div>

{#====================================================================================================================
 # CS2103 Weekly Intros
 #====================================================================================================================#}
<div id="cs2103-week2-intro">

<include src="ip-tasks-fragment.md#volatile-requirements" />
<include src="ip-tasks-fragment.md#no-jumping-ahead" />
<include src="ip-tasks-fragment.md#follow-instructions" />

<box>

**:fas-clock: Deadline:**

Note the typical deadline weekly project tasks:
{{ embed_topic("weeklySchedule.md#deadline-definition", "Admin " + icon_embedding + " Weekly schedule → **Deadline for weekly tasks**", "1") }}
<p/>

As per the above, ==you have until the {{ lecture_name }}== at the end of this week (i.e., {{ get_date(date_w2_start, 4, time=time_lecture_start) }}) to finish this week's iP tasks, but if you fail to do so, we won't penalize you if you can catch up within one more week after that deadline.
</box>
</div>
<div id="cs2103-week3-intro">

**{{ icon_important_big_red }} You are required to follow the Git standard from this week**, as specified in [this page](standardsAndConventions.html).<br>
  ==Only _future_ commits need to follow the Git standard.== Editing past commit messages (to make them comply with the Git standard) is discouraged as it changes the commit timestamp, which can alter your iP progress timeline (as seen by progress tracking scripts).

**:fas-clock: Reminder about the deadline for the weekly project tasks:**
{{ embed_topic("weeklySchedule.md#deadline-definition", "Admin " + icon_embedding + " Weekly schedule → **Deadline for weekly tasks**", "1", indent=1) }}
<p/>

</div>
<div id="cs2103-week4-intro">

<box type="info" icon=":fab-apple:" seamless>

**++Mac users:++** Ensure you have followed the advisory given [here](programmingLanguages.md).
</box>

</div>

{#====================================================================================================================
 # CS2113 Weekly Intros
 #====================================================================================================================#}
<div id="cs2113-week2-intro">

<include src="ip-tasks-fragment.md#volatile-requirements" />
<include src="ip-tasks-fragment.md#no-jumping-ahead" />
<include src="ip-tasks-fragment.md#follow-instructions" />

<box dismissible>

**:fas-clock: Deadline:**

Note the typical deadline weekly project tasks:
{{ embed_topic("weeklySchedule.md#deadline-definition", "Admin " + icon_embedding + " Weekly schedule → **Deadline for weekly tasks**", "1") }}
<p/>

But ==as there are no tutorials this week, you have until the next lecture== to finish this week's iP tasks.
</box>
</div>
<div id="cs2113-week3-intro">

**:fas-clock: Reminder about the deadline for the weekly project tasks:**
{{ embed_topic("weeklySchedule.md#deadline-definition", "Admin " + icon_embedding + " Weekly schedule → **Deadline for weekly tasks**", "1", indent=1) }}
<p/>

</div>

{#====================================================================================================================
 # Pre/Post info
 #====================================================================================================================#}
<div id="pre_Level-0">
<div tags="m--cs2113">
<include src="ip-tasks-fragment.md#commit" />
</div>
<div tags="m--cs2103">

<include src="ip-tasks-fragment.md#order" />
<box type="important" light>

#####  Keep in mind ...{.text-danger}

<include src="ip-tasks-fragment.md#commit" />
<include src="ip-tasks-fragment.md#tag-push" />
<include src="ip-tasks-fragment.md#take-note-of-plagiarism" />
</box>
<box type="tip" light>

##### iP feels like 'same same' ...?{.text-success}

**As you do the iP, if you feel like you are not learning enough new stuff** as you've done similar work before (at least on the Java/OOP side), there is an alternative approach you can take to the iP. See the panel below if you are interested.

<panel type="seamless" header="****iP.AI****: an AI-assisted approach to the iP" minimized>

**Goal**: In the iP.AI approach, your goal is to minimize hand-coding the iP, by getting generative AI tools (such as Co-Pilot) to write the code for you instead. The learning goal is to explore how to increase your coding productivity using AI tools.

**Requirements:**

1. You should follow the normal iP requirements/deadlines, except that you will try to replace handcoding with AI-assisted code generation, where possible. It is still fine to do some of the coding work manually.
1. You may use any free or commercial AI tools, provided you declare which tool you used (how to declare? see next point).
1. Add a file named `AI.md` at the root of project folder (same location where `CONTRIBUTORS.md` lives). Commit the file. Keep it updated with a record of your use of AI tools (e.g., which tool you used for which increment), and interesting observations (e.g., what worked? what didn't? overall, how much time did it save?). You can update this file periodically (e.g., once a week). The content format can be plaintext or Markdown. It need not be very detailed (e.g., even a 0.5 page is enough).

**Caveat:** This alternative does not earn you extra credit, but it gives you an opportunity to learn more about AI tools related to SE, with the same (or even less) effort.<br>
This alternative is only suitable for those who are already good at hand-coding. Reason: At the current state of the art of AI tools, only those who are already good at hand-coding can use those tools to increase productivity. So, you must become good at hand-coding before you venture into using AI tools for coding.
</panel>
</box>
</div>
</div>

<div id="post_A-Enums">
<div tags="m--cs2103">
<p/>
<include src="ip-tasks-fragment.md#ip-faq" />
</div>
</div>
{#====================================================================================================================#}
<div id="pre_Level-5">
<div tags="m--cs2113">

* Do each increment as a Git branch. Here is an example:
  * Start a branch named `branch-{increment ID}` (e.g. `branch-Level-5`). You are recommended to have multiple commits in that branch. Follow the branch naming convention exactly or else our gradings scripts might miss your branch.
  * After the increment is ready, merge the `branch-Level-5` back on to `master`, ==without a _fast-forward_== so that git creates a separate commit for the merge. `git tag` that merge commit as `Level-5`.
  * Push the branch to your fork so that the grading script can detect it. As before, push the tag as well.
  * {{ icon_important_big_red }} Advanced git users: do not delete the branch after merging.
</div>
</div>
{#====================================================================================================================#}
<div id="pre_A-Packages">
<div tags="m--cs2113">

* Recommended: if you are new to git, do this as a separate branch too (for additional practice), similar to how you did `Level-5` (branch name `branch-A-Packages`).
</div>
</div>
{#====================================================================================================================#}
<div id="pre_Level-6">
<div tags="m--cs2113">

* Practice using parallel git branches, as explained below:
  1. First, do Level-6 in a branch named `branch-Level-6`, but do not merge it.
  1. Then, go back to the `master` branch and implement Level-7 in a separate branch named `branch-Level-7`.
  1. Now, go back to the `master` branch and merge the two branches one after the other.<br>
     If there are merge conflicts, you'll have to resolve them first.
  1. As before, tag the commit (in the `master` branch, after merging) that achieves the respective deliverable, and push to your fork.
* As before,
 {{ icon_tip }} Merge without a _fast-forward_ so that git creates a separate commit for the merge.<br>
 {{ icon_important_big_red }} Advanced git users: do not delete the branch after merging.
</div>

</div>
{#====================================================================================================================#}
<div id="pre_A-Jar">
<div tags="m--cs2103 m--cs2113">
<p/>
</div>
</div>
{#-------------------------------------------------------------------#}
<div id="post_A-Jar">
<div tags="m--cs2103 m--cs2113" class="indented-level2">

Note that if `A-Jar` increment does not require any code changes, you may tag the commit at which this was achieved as `A-Jar` (even if that commit has another tag already). Otherwise, tag the latest commit as usual. In both cases, push the tag to the fork.
</div>
</div>
{#====================================================================================================================#}
<div id="pre_Level-7">
<div tags="m--cs2103">

<mermaid>
{{ "%%{init: { 'theme': 'default', 'gitGraph': {'mainBranchName': 'master'}} }%%" }}
gitGraph
commit id: "m1"
commit id: "m2"
branch branch-Level-7
checkout branch-Level-7
commit id: "b1c1"
commit id: "b1c2"
checkout master
merge branch-Level-7 id: "Merge branch ..." tag: "Level-7"
branch branch-Level-8
checkout branch-Level-8
commit id: "b2c1"
checkout master
merge branch-Level-8 id: "Merge branch-Level-8 ..." tag: "Level-8"
commit id: "m4"
</mermaid>

<box type="warning" seamless>

If you are new to Git branching, before attempting this iP increment, first learn Git branching from [this week's textbook topics]({{ baseUrl }}/schedule/week3/topics.html). In particular, learn how to merge a branch without fast forwarding.
</box>

* **Do Level 7 in a branch named `branch-Level-7`**. Here are the steps:
  1. Start a branch `branch-Level-7`.
  1. Implement Level 7 while committing to that branch at appropriate points,
  1. Merge the branch back to the `master` branch (remember to create a merge commit i.e., ==no fast-forward==).
  1. Git tag the merge commit in the `master` branch as usual (i.e., add the tag `Level-7`).
  1. Push the following three things to your fork:<br>
     (a) the `master` branch,<br>
     (b) the `branch-Level-7` branch,<br>
     (c) the `Level-7` tag.<br>
     {{ icon_important_big_red }} Advanced git users: do not delete the branch after merging.<br>
     {{ icon_important_big_red }} Only _merged_ branches are detected by the script. After merging a branch `b1` to the `master` branch, you need to push both the `master` and the `b1` branches to the fork. Pushing the `master` branch does not automatically take the `b1` branch along with it just because it is already merged to the `master` branch.

</div>
</div>
{#====================================================================================================================#}
<div id="post_Level-7">
{{ show_faq("ipOtherDataFormats") }}
{{ show_faq("ipMessedUpBranching") }}
{{ show_faq("ipNotDoneInBranch") }}
</div>
{#====================================================================================================================#}
<div id="pre_Level-8">
<div tags="m--cs2103">

* **Do Level 8 similar to the above**, using a branch `branch-Level-8`.
</div>
</div>
<div tags="m--cs2113 m--cs2103" id="as-parallel-prs">

{% call topic_preamble(reuse=false) %}

As you know, one main goal of the iP is to prepare for you for the tP. The task below is heavy on the 'training for tP' aspect.

In previous iP increments, you learned:

* How to merge branches locally and push to your fork
* How to create PRs from the `master` branch to an upstream repo

In the following iP task you will learn how to do the following new things, which are relevant to the tP:

* How to merge branches remotely, and pull to your local repo
* How to create PRs from branches other than `master`
* How to manage PRs that your repo receive
* How to work with parallel PRs

Due to the above learning goals, this iP task is a bit complicated. Pay attention and try to achieve all learning goals along the way.
{% endcall %}
<br/>

* **Note how to merge PRs**:

{{ embed_topic("../book/gitAndGithub/managePRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Merging PRs**", "1", indent=1) }}

* **Practice using parallel git branches _and_ PRs**, as explained below:
1. First, do each increment as a parallel branch (follow the branch naming convention you followed earlier `branch-Level-8` etc.), but do not merge any.
   <mermaid>
   {{ "%%{init: { 'theme': 'default', 'gitGraph': {'mainBranchName': 'master'}} }%%" }}
   gitGraph
   commit id: "m1"
   commit id: "m2"
   branch branch-A-Assertions
   checkout branch-A-Assertions
   commit id: "b1c1"
   checkout master
   branch branch-A-CodeQuality
   checkout branch-A-CodeQuality
   commit id: "b2c1"
   checkout master
   branch branch-A-Streams
   checkout branch-A-Streams
   commit id: "b3c1"
   commit id: "b3c2"
   checkout master
   </mermaid>

1. Then, push each branch to your fork, and create a PR !!within your fork!! (i.e., from the increment branch to the `master` branch). ==Be careful not to create a PR to [the upstream repo]({{ url_course_org }}/ip).== %%If you did create such a PR by mistake, no worries, just close it yourself.%%

{{ embed_topic("../book/gitAndGithub/createPRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Creating PRs**", "1", indent=1) }}

<box type="tip" seamless>

When you are doing the next step, you can run into merge conflicts. In some cases, GitHub will give you a way to resolve those conflicts using the Web interface. While this approach may be good enough for simple merge conflicts, **de-conflicting locally in the standard way is safer** (e.g., you can run tests to confirm the updated code is correct) and more standard (it's a standard Git feature that you can use even when you are not using GitHub for your project).
</box>

3. Now, merge one of the PRs and update the remaining PRs accordingly, as given below:
   * Merge one of the PRs on GitHub. Remember to choose the `Create merge commit` option when merging.{ texts="['3.1)','3.2)','3.3)','3.4)','3.5)']" }
   * The above step will cause the `master` branch of your local repo to fall behind that of your fork (<popover content="because your remote `master` branch (i.e., `origin/master`) now has a merge commit that the local `master` does not have yet">why</popover>). Therefore, you need to sync the local `master` with the remote `master` branch. One way to do that is to switch to the local `master` branch and then pull the updated `master` branch from your fork e.g.,
      ```{.no-line-numbers}
      $ git checkout master
      $ git pull origin master
      ```
   Tag the merge commit as usual, and push to the fork.<br>
   The diagram below shows the current situation, assuming you merged the `A-Assertions` PR first.
   <mermaid>
   {{ "%%{init: { 'theme': 'default', 'gitGraph': {'mainBranchName': 'master'}} }%%" }}
   gitGraph
   commit id: "m1"
   commit id: "m2"
   branch branch-A-Assertions
   checkout branch-A-Assertions
   commit id: "b1c1"
   checkout master
   branch branch-A-CodeQuality
   checkout branch-A-CodeQuality
   commit id: "b2c1"
   checkout master
   branch branch-A-Streams
   checkout branch-A-Streams
   commit id: "b3c1"
   commit id: "b3c2"
   checkout master
   merge branch-A-Assertions tag: "A-Assertions"
   </mermaid>
   * Note how the remaining <tooltip content="i.e., branches not merged to the `master` branch yet">un-merged branches</tooltip> are no longer in sync with the latest `master`. To rectify, merge the `master` branch on to each of them. Resolve merge conflicts, if any. The outcome will be something like the below:{ texts="['3.3)']" }
   <mermaid>
   {{ "%%{init: { 'theme': 'default', 'gitGraph': {'mainBranchName': 'master'}} }%%" }}
   gitGraph
   commit id: "m1"
   commit id: "m2"
   branch branch-A-Assertions
   checkout branch-A-Assertions
   commit id: "b1c1"
   checkout master
   branch branch-A-CodeQuality
   checkout branch-A-CodeQuality
   commit id: "b2c1"
   checkout master
   branch branch-A-Streams
   checkout branch-A-Streams
   commit id: "b3c1"
   commit id: "b3c2"
   checkout master
   merge branch-A-Assertions tag: "A-Assertions"
   checkout branch-A-CodeQuality
   merge master id: "merge master to ..."
   checkout branch-A-Streams
   merge master
   </mermaid>
   * Push the updated branches to your fork. The PRs will update automatically to reflect the updated branch.{ texts="['3.4)','3.5)']" }
   * As before, tag the merge commit in the master branch and push the tag to your fork.
1. Merge the remaining PRs using a procedure similar to the above. The diagram below shows the situation after merging the `A-CodeQuality` PR and syncing the local `branch-A-Streams` with the updated `master` branch.
   <mermaid>
   {{ "%%{init: { 'theme': 'default', 'gitGraph': {'mainBranchName': 'master'}} }%%" }}
   gitGraph
   commit id: "m1"
   commit id: "m2"
   branch branch-A-Assertions
   checkout branch-A-Assertions
   commit id: "b1c1"
   checkout master
   branch branch-A-CodeQuality
   checkout branch-A-CodeQuality
   commit id: "b2c1"
   checkout master
   branch branch-A-Streams
   checkout branch-A-Streams
   commit id: "b3c1"
   commit id: "b3c2"
   checkout master
   merge branch-A-Assertions tag: "A-Assertions"
   checkout branch-A-CodeQuality
   merge master id: "merge master to ..."
   checkout branch-A-Streams
   merge master
   checkout master
   merge branch-A-CodeQuality tag: "A-CodeQuality"
   checkout  branch-A-Streams
   merge master
   </mermaid>

{{ show_faq("ipMessedUpBranching") }}
</div>
{#====================================================================================================================#}
<div id="pre_A-CheckStyle">
<div tags="m--cs2103">

* Do each increment as a separate branch, similar to [how you did Level 7]({{baseUrl}}/schedule/week3/project.html#3-add-increments-as-branches-level-7-level-8) before.
</div>
</div>
{#====================================================================================================================#}
<div id="post_A-CheckStyle">
<div tags="m--cs2103">

{{ show_faq("ipCheckstyleMismatchWithCodingStandard") }}
</div>
</div>
{#====================================================================================================================#}
<div id="pre_A-Assertions">
<div tags="m--cs2103">

<include src="ip-tasks-fragment.md#as-parallel-prs" />
</div>
</div>
{#====================================================================================================================#}
<div id="pre_A-MoreOOP">

{% if cs2103 %}
* While not required, you are encouraged to use separate branches for each increment.
  <br>Reason: that way, the `master` branch will always stay in a 'unbroken' state as the work-in-progress will be in a separate branch till such work is ready to be merged.{% endif %}
* As before, commit, tag, and push, after each increment.
</div>
{#-------------------------------------------------------------------#}
<div id="post_A-MoreOOP">
<div tags="m--cs2103 m--cs2113" class="indented-level2">

<panel type="seamless">
<span slot="header" class="card-title text-info"><markdown>{{ icon_info }} **Why more OOP?**</markdown></span>

One of the iP increments asks you to push the design more towards the OOP approach. This is a good point to remind you the following points:

****Good OOP != OOP is good****: While the course pushes you to use _good OOP_, do not interpret it as a message of _OOP is good_; it's good for many situations but not so for some other situations. The best is usually a combination of approaches. Hence, you are encouraged to get better at other paradigms, the _functional_ paradigm in particular which has been rising in popularity in some areas such as big data, AI, parallel systems.<br>
That said, it is also preferable to use one paradigm as the primary approach and fallback on others only when the primary paradigm is clearly sub-optimal. Reason: mixing everything in equal measures might make the system even harder to understand.

**OOP is primary paradigm for this course and you are expected to try to push it to its limits.** That should give you a first-hand experience of OOP's strengths and weaknesses. Furthermore, OOP (or any other paradigm) will appear worse than it really is if not used correctly, and learning to use it correctly in increasingly larger systems is another objective you can aim for in this course. {% if cs2103 %}As you do the tP later, you'll also realize that while OOP is used for the internal design of its components, the higher-level design is not specifically an OOP one.{% endif %}<br>

**We do not prohibit the use of other paradigms**, however. For example, if you find a place where the _functional_ approach is better, go ahead and use it. As you know, Java supports functional programming to a certain extent. {% if cs2103 %}In fact, the tP code given to you uses small snippets of functional-style code in several places.{% endif %}
</panel>
</div>
</div>
{#====================================================================================================================#}
<div id="pre_A-JavaDoc">
<div tags="m--cs2103">

* Implement these three increments ==as three <popover content="i.e., start a branch, add some code to it, go back to the master branch (without merging the first branch), and start another branch, and so on">parallel</popover> branches== first (branch names: `branch-A-JavaDoc`, `branch-A-CodingStandard`, `branch-Level-9`), and then merge them one-by-one. Hopefully, you will encounter some merge conflicts so that you get to practice de-conflicting branches.

<mermaid>
{{ "%%{init: { 'theme': 'default', 'gitGraph': {'mainBranchName': 'master'}} }%%" }}
gitGraph
commit id: "m1"
commit id: "m2"
branch branch-A-JavaDoc
checkout branch-A-JavaDoc
commit id: "b1c1"
commit id: "b1c2"
checkout master
branch branch-A-CodingStandard
checkout branch-A-CodingStandard
commit id: "b2c1"
checkout master
branch branch-Level-9
checkout branch-Level-9
commit id: "b3c1"
commit id: "b3c2"
checkout master
merge branch-A-JavaDoc tag: "A-JavaDoc"
merge branch-A-CodingStandard tag: "A-CodingStandard"
merge branch-Level-9 tag: "Level-9"
commit id: "m6"
</mermaid>

* The Java and Git standards to follow (for `A-CodingStandard`) are given in [this page](standardsAndConventions.html).
* After finishing, assuming you encountered merge conflicts (and some were rather painful to resolve), think of how such conflicts could have been reduced %%(e.g., by changing the order of merging, or minimizing parallel branches when certain type of changes are being done to the code)%%.
</div>
</div>
{#====================================================================================================================#}
<div id="pre_A-CodingStandard">

<box type="tip" seamless>

Relevant SE-EDU guide: [Intellij IDEA: Configuring the code style](https://se-education.org/guides/tutorials/intellijCodeStyle.html)
</box>
</div>
{#====================================================================================================================#}
<div id="post_A-CodingStandard">

{{ show_faq("ipAspectsNotCoveredByTheStandard") }}
</div>
{#====================================================================================================================#}
<div id="pre_A-Gradle">
<div tags="m--cs2103 m--tic2002">
<p/>

* Do the following increments in the given order because after doing `A-Gradle` you can use the Gradle option (rather than the IntelliJ option) when doing `A-JUnit` and `A-JAR` as they are easier to do using Gradle.{ icon="glyphicon-exclamation-sign" i-class="text-danger" i-size="25px"}

<div class="indented-level2" id="pulling-branch-from-upstream">
<panel type="seamless" >
<span slot="header" class="card-title"><markdown>{{ icon_tip}} **How do I fetch the `add-gradle-support` branch from my fork?**{.text-success}</markdown></span>

General instructions for fetching a new branch from a remote can be found in the panel below:

   {{ embed_topic("../book/gitAndGithub/remoteBranches/text.md#pulling-a-new-branch", "Textbook " + icon_embedding + " Git&Github → **Remote branches** (extract)", "2", status="expanded") }}

</panel>

<panel type="seamless" >
<span slot="header" class="card-title"><markdown>{{ icon_tip}} **If your fork doesn't have the `add-gradle-support` branch ...**{.text-success}</markdown></span>

If your fork doesn't have the `add-gradle-support` branch (i.e., you did not copy all the branches when you forked), here are the steps for fetching the `add-gradle-support` branch from the upstream repo:<br>

1. Add the upstream repo `{{ url_course_org }}/{{ ip_repo_name }}.git` as a remote, and give it the name `upstream`.<br>
   General instructions for adding a remote to your repo can be found in the panel below:

   {{ embed_topic("../book/gitAndGithub/pull/text.md#section-working-with-multiple-remotes", "Textbook " + icon_embedding + " Git&Github → Pull → **Working with multiple remotes**", "2", indent="1") }}

2. fetch the `add-gradle-support` from the remote `upstream`.<br>
   General instructions for fetching a new branch from a remote can be found in the panel below:

   {{ embed_topic("../book/gitAndGithub/remoteBranches/text.md#pulling-a-new-branch", "Textbook " + icon_embedding + " Git&Github → **Remote branches** (extract)", "2", indent="1") }}
</panel>
<p/>
</div>

</div>
</div>
{#====================================================================================================================#}
<div id="pre_Level-10">

<div class="indented-level1">
<br>

<span class="text-danger">**:fab-apple: Attention Mac users**</span>! If you are not using the ==exact **Azul** JDK distribution== (not any other JDK 17 distributions) specified by our advisory for Mac users in [this page](programmingLanguages.md), you are likely to run into problems while doing `Level-10`.
</div>
</div>
{#====================================================================================================================#}
<div id="post_Level-10">

<div class="indented-level1">

*  **You no longer need to keep the text-based UI** after adding a GUI (although you are welcome to). Similarly, there is no need to keep the I/O redirection style automated testing added via `A-TextUiTesting`) anymore -- that technique is suited for text UIs only.{{ bullet_info }}
* **Is the `bye` command still needed**, now that the GUI can be closed in other ways?<br>
  Yes, we recommend keeping it. Reason: Being able to close the app by typing a command is consistent with the app's CLI-style <tooltip content="i.e., User Experience">UX</tooltip>.{{ bullet_Q }}
</div>
</div>
{#====================================================================================================================#}
<div id="pre_A-CI">

* We recommend that ==at least one member== of the team attempt the following.
</div>
{#====================================================================================================================#}
<div id="pre_A-BetterGui">
<div tags="m--cs2103">

* As before, we recommend (but not require) that each increment is done as a separate branch and merged to the `master` branch when ready fully done.
</div>
</div>
{#====================================================================================================================#}
<div id="pre_A-AiAssisted">
{% set ip_ai_link = "[iP.AI route](../schedule/week2/project.html#:~:text=iP.AI%3A%20an%20AI%2Dassisted%20approach%20to%20the%20iP)" %}
* If you are already following the {{ ip_ai_link }}, you may add the `A-AiAssisted` tag to the latest commit of your repo without needing any further work.
* Otherwise (i.e., if you haven't been using AI tools in the iP until now), the increment below is an opportunity for you to use the iP to explore how AI tools can help with programming tasks. If you take it up, in places where you use AI-assisted code, give some details (e.g., which tool you used how it helped) as a code comment. Alternatively, you can add an `AI.md` file, similar to the {{ ip_ai_link }}.
</div>

{#====================================================================================================================#}
{# Steps
{#====================================================================================================================#}
<span id="heading_learn_about_the_project">Learn about the project</span>
<div id="desc_learn_about_the_project">

* **Read the following two sections**, if you haven't done so already:

{{ embed_topic(baseUrl+"/admin/ip-overview.md#main", "Admin " + icon_embedding + " **iP - Overview**", "3", indent="1") }}
{{ embed_topic(baseUrl+"/admin/ip-grading.md#main", "Admin " + icon_embedding + " **iP - Grading**", "1", indent="1") }}
</div>
{#====================================================================================================================#}
<span id="heading_set_up_prerequisites">Set up prerequisites</span>
<div id="desc_set_up_prerequisites">

* **Ensure you have followed the <span class="ps-1 pe-1" style="color:purple; border: 0.5px solid lightgrey">:fas-hard-hat: Preparation</span> sections of the following course tools:**

{{ embed_topic(baseUrl+"/admin/programmingLanguages.md#main", "Admin " + icon_embedding + " **Programming Language**", "2", indent="1") }}
{{ embed_topic("tools.md#rcs", "Admin " + icon_embedding + " **Tools → Git**", "2", indent="1") }}
{{ embed_topic("tools.md#github", "Admin " + icon_embedding + " Tools → **GitHub**", "2", indent="1") }}
{{ embed_topic("tools.md#ide", "Admin " + icon_embedding + " Tools → **IntelliJ IDEA**", "2", indent="1") }}
</div>
{#====================================================================================================================#}
<span id="heading_set_up_project">Set up the project in your computer</span>
<div id="desc_set_up_project">

<div class="indented">
<box>

Read through this week's topics before starting the project.<br>
 **If you encounter technical problems** while doing the iP, follow the guidelines given below:

{{ embed_topic(baseUrl+"/admin/appendixD-help.md#main", "Admin " + icon_embedding + " Appendix D: Getting Help", "2") }}
</box>
</div>

1. **Fork** [{{ url_course_org }}/{{ ip_repo_name }}]({{ url_course_org }}/{{ ip_repo_name }}), while noting the points below:<br>
   <box type="important" seamless><md>==**Keep the fork name as `{{ ip_repo_name }}`**== or else our grading scripts will not be able to detect it. You can change the fork name to something else after the semester (and the grading) is over e.g., after receiving your grade for the course.</md></box>
   <box type="tip" seamless><md>**Untick the `[ ] Copy the master branch only` option** so that you get a copy of the full repo.</md></box>
1. ==**Enable the issue tracker** of your fork== (Go to `Settings` of your fork, scroll to the `Features` section, and tick the `Issues` checkbox). %%Reason: at times we post feedback on your issue tracker.%%<br>
   <box type="tip" seamless><md> If the issue tracker is enabled, you should be able to visit the following URL `https://github.com/{your_user_name}/{{ ip_repo_name }}/issues/new`<br> e.g., `https://github.com/johnDoe/{{ ip_repo_name }}/issues/new`</md></box>
1. **Clone the fork** onto your computer.
   <box type="warning" seamless><md>**Avoid putting Git-controlled files inside cloud-synced (e.g., OneDrive, Dropbox) folders.** Reason: Multiple tools trying to detect/sync changes in the same folder can cause conflicts and unexpected behaviors.<br> If you want to access project files from multiple computers, use Git to do that (rather than cloud syncing tools).</md></box>
1. **Set up the project in your IDE** as explained in [the README file]({{ url_course_org }}/{{ ip_repo_name }}/blob/master/README.md), if you plan to use an IDE for the project.
   <box type="tip" seamless><md>**Not willing to lose Vim power?** Vim users worried about losing access to powerful Vim features if you use an IDE for the project: Most IDEs have a Vim plugin (e.g., [IdeaVim plugin](https://github.com/JetBrains/ideavim)) for using Vim features within the IDE i.e, it is possible to access both IDE features and Vim features at the same time!</md></box>

</div>
{#====================================================================================================================#}
<span id="heading_finish_leftover_tasks">Do any leftover iP tasks from the previous week</span>
<div id="desc_finish_leftover_tasks">

* Remember to do any leftover increments from the past weeks before starting on the current week's increments. This guideline applies to future weeks too.
</div>
{#====================================================================================================================#}
<span id="heading_create_pr_to_upstream">Create a PR to the upstream repo</span>
<div id="desc_create_pr_to_upstream">

* Create a <trigger trigger="click" for="modal:ipTasks-createPr">pull request (PR)</trigger> from your fork to the upstream repo. Note the following:
  * Create the PR from the `master` branch of your fork to the `master` branch of the upstream repo ({{ url_course_org }}/{{ ip_repo_name }})
  * Set the PR name as `[{Your full/partial name or your GitHub username}] iP`<br>
    e.g., `[Richard Mathews Chee] iP` or `[Rich ... hee] iP` or `[TheRichMat] iP`<br>
    %%Note that the PR name will be publicly visible.%%<br>
    You may leave the description empty.
  * If you created the PR correctly, it should appear in the list of PRs [here]({{ url_course_org }}/{{ ip_repo_name }}/pulls).
  * Steps for creating a PR is given in this textbook topic (==steps 5 onwards==):

{{ embed_topic("../book/gitAndGithub/createPRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Creating PRs**", "1", indent=2) }}

<div class="indented-level2">

<box tags="m--cs2103 m--cs2113" type="info" seamless>

There is no need to create new PRs every time you update the code in your fork. The PR will update automatically to reflect the latest code of the branch it was sent from (i.e., when you push changes to the `master` branch of your fork).
</box>

</div>

<modal large header="Pull Request (PR)" id="modal:ipTasks-createPr">

_Pull Requests_ is a mechanism for offering code to a repository e.g., a bug fix or a new feature. PRs allow developers to review, discuss, and refine proposed code changes before incorporating (i.e., _merging_) the new code to the repository.

Resources:
* [GitHub Help page on PRs](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests)
</modal>
</div>
{#====================================================================================================================#}
<span id="heading_start_learning_javafx">[Optional] Get a head start on JavaFX</span>
<div id="desc_start_learning_javafx">

If you can spare some time, start learning JavaFX by following the [_JavaFX tutorial_ @SE-EDU/guides](https://se-education.org/guides/tutorials/javaFx.html). Doing so will make your life easier in the following week.
</div>
{#====================================================================================================================#}
<span id="heading_prepare_for_pr_reviews">Get ready to review PRs</span>
<div id="desc_prepare_for_pr_reviews">

* **Do the following to prepare for the PR review exercise** you will be doing in the coming tutorial.
  * Learn how to review PRs:

{{ embed_topic("../book/gitAndGithub/reviewPRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Reviewing PRs**", "1", indent=2) }}

  * Read the [_Best practices for reviewing PRs_ @SE-EDU/guides](https://se-education.org/guides/guidelines/PRs-reviewing.html). You are ==expected to follow all of them==.
</div>
{#====================================================================================================================#}
<span id="heading_use_gfmd_in_pr_description">Use GFMD in the PR description</span>
<div id="desc_use_gfmd_in_pr_description">

* [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/) (and Markdown in general) is useful in many places when using GitHub %%e.g., issue tracker, PR reviews, writing documentation%%. The aim of this task is to ensure that you are sufficiently familiar with the GFMD syntax.
* Requirements: **Update  the description of the [iP ==PR==]({{ url_course_org }}/ip/pulls)** <tooltip content="go to the PR, click on the the `...` icon on the top right corner of the previous description and choose `Edit`">(how?)</tooltip> you created earlier (<span class="text-danger">do not add a new comment</span>) so that it contains the following GFMD elements:
  1. a heading
  1. a bullet list
  1. a numbered list
  1. a fenced code block (with syntax highlighting)
  1. a task list
  1. an emoji
  1. a blockquote
  1. a hyperlink
  1. inline code
  1. some text formatting: bold, italic, strikethrough etc.

<div class="indented-level2">

<panel header="Here is an example:" expanded no-close no-switch>

##### DukePro

> “Your mind is for having ideas, not holding them.” – David Allen ([source](https://dansilvestre.com/productivity-quotes))

DukePro frees your mind of having to remember things you need to do. It's,
* text-based
* easy to learn
* ~~FAST~~ _SUPER_ FAST to use

All you need to do is,
1. download it from [here]().
1. double-click it.
1. add your tasks.
1. let it manage your tasks for you :wink:

And it is **FREE**!

Features:
- [x] Managing tasks
- [ ] Managing deadlines (coming soon)
- [ ] Reminders (coming soon)

---

If you are a Java programmer, you can use it to practice Java too. Here's the `main` method:
```java{.no-line-numbers}
public class Main {
    public static void main(String[] args) {
        Application.launch(MainApp.class, args);
    }
}
```

</panel>
</div>

<box type="info" seamless>

If you wish, **you _may_ write the PR description to be very similar to the example** given above -- as the goal here is to demonstrate your mastery of the GFMD syntax (not ad writing skills).
</box>
</div>
{#====================================================================================================================#}
<span id="heading_review_two_prs">Review some peer PRs</span>
<div id="desc_review_two_prs">

<div tags="m--cs2103">

<box type="wrong" add-class="ml-4" icon=":fas-hand-paper:" icon-size="2x" seamless>

**Please wait till {{ date_w4_start | date(format_normal, 0) }}** to start this task, to give others a few extra days to create the PR if they haven't done so yet.
</box>
</div>

<box type="info" add-class="ml-4">

This task is worth `2x2=4` participation points.
</box>

* **Learn _how_ you should review PRs in this task**:

{{ '' if cs2113 else panopto('c001244c-01b5-4471-ab9d-ac1b0098110a') }}

{{ embed_topic("../book/gitAndGithub/reviewPRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Reviewing PRs**", "1", indent=1) }}

* {{ step(1) }} **Note these additional guidelines**:
  * Read the [_Best practices for reviewing PRs_ @SE-EDU/guides](https://se-education.org/guides/guidelines/PRs-reviewing.html). You are ==expected to follow all of them==.
  * Make sure you ==add 'review comments' (not regular comments)== as only those are counted for participation. See step 4 in the panel above to find how to add 'review comments'.
  * If the PR has received some review comments already, feel free to confirm/complement/question those comments in your review. Also, look for things the previous reviewers may have missed.
  * At the end of the review, choose `Comment` (i.e., not `Approve` or `Request changes`)

* {{ step(2) }} **Do the first PR review** as follows.
  * Give comment on ==[coding standard]({{ url_java_coding_standard }}) related issues only==.<br>
    Review comments don't always have to be about problems in the code. Other things you can do:
    * compliment the author on not making a common mistake
    * ask questions
    * suggest alternatives
  * The review allocation is given in the panel below.

<div class="indented-level2">

<include src="common-tutorials-fragment.md#show-ip-peer-review-allocation-1" />
</div>

* {{ step(3) }} **Do the second PR review** as follows.
  * Comment on ==other code quality guidelines== <span tags="m--cs2103">(see the section [_Code Quality: Naming_]({{ baseUrl }}/schedule/week4/topics.html#w4-6-code-quality-naming))</span><span tags="m--cs2113">(see the sections on _Naming_ and _Readability_ in [this textbook chapter](../se-book-adapted/chapters/codeQuality.html))</span> you have learned so far. It's optional to comment on coding standard violations in this PR review.
  * The review allocation is given in the panel below.

<div class="indented-level2">

<include src="common-tutorials-fragment.md#show-ip-peer-review-allocation-2" />
</div>

* {{ step(4) }} **[When you receive reviews for your own PR] Respond to comments received**. You are recommended to (but not obliged to) respond to comments received from peers, especially if the PR reviewer asked you for more info. As mentioned in [these guidelines](https://se-education.org/guides/guidelines/PRs-reviewing.html), do not get into arguments with PR reviewers/authors.

</div>
{#====================================================================================================================#}
<span id="heading_learn_from_others">Learn from others (optional)</span>
<div id="desc_learn_from_others">

* **You can use the [iP Code Dashboard]({{ url_ip_dashboard }}) to view others' iP code**, using the `Links → iP Code Dashboard` item in the top navigation menu of this course website.We encourage you to read others’ code and learn from them. If you adopt solutions from others (also encouraged), please follow our reuse policy. <br>


<box type="tip" seamless>

Click on the <span class="badge bg-light text-dark">%%**:fas-code:**%%</span>&nbsp;icon corresponding to a student name to see the code written by that person.

You can enable the `[ ] show tags` option at the top of the dashboard to see tags in each repo. Similarly, you can click on the <span class="badge bg-light text-dark">%%**:fas-list:**%%</span>&nbsp;icon to see a list of commits in a specific repo.
</box>

{{ embed_topic("appendixB-policies.md#policy-reuse", "Admin " + icon_embedding + " **Course Policies → Policy on Reuse**", "1", indent=1) }}

</div>
{#====================================================================================================================#}
<span id="heading_evaluate_peer_ips">Evaluate two peer iPs</span>
<div id="desc_evaluate_peer_ips">

<div class="indented-level2">

<box type="info">

This activity is worth `2x2=4` participation points.
</box>

</div>

1. {% if cs2113 %}**The allocation will be sent via email**, by Monday 2359.{% else %}**Wait for the email notifying you which iPs are allocated for you to evaluate**. When the email is sent out, it will also be announced via course announcements.{% endif %}
1. **Download the _latest_ JAR file** of the first iP by following the link provided.
   {{ show_faq("ipEvaluationNoJar") }}
3. **Locate the User Guide** of the app by following the link provided in that email.
1. **Open the Canvas survey** (the one named `iP Peer Evaluation 1`) that you will be using to submit your evaluation and take note of the things you need to evaluate.
1. **Run the jar file** in the following manner:
   * Put the jar file in an ==empty folder==<br>
     %%Reason: prevent data files created by other jar files you tested earlier from interfering with the current jar file.%%{ texts="['5.1','5.2','5.3','5.4']" }
   * Open a terminal, and ==navigate to the folder== you put the JAR file in (e.g., `cd smoke-test/ip1`)<br>
     %%Reason: data files will be created relative to the folder the terminal is currently in.%%
   * {{ icon_important_big_red }} Run the ==`java -version` command== to confirm you are using Java 17.{% if cs2103 %}<br>
      :fab-apple: Mac user, confirm you are using the exact Java distribution we have prescribed [here](programmingLanguages.md).{% endif %}
   * Run the jar file using the ==`java -jar "{file_name}"` command== (rather than double-clicking) in the same terminal.
1. **Do a light testing of the app** (not more than 10 minutes) to ensure the claimed features actually exist and there are no obvious bugs.<br>
1. **Do a quick examination of the code** (~ 5 minutes) by following the provided link.
1. **Submit your evaluation** using the survey.
1. **Repeat the above steps for the 2nd iP** allocated to you (use the survey `iP Peer Evaluation 2`).<br>
   If _both_ iPs crash or fail severely in a similar fashion, the problem may be on your side. Please contact the teaching team to ask how to proceed.
1. %%**Take note of the effort required for a _typical_ iP**: After seeing two more iPs, you should now be in a better position to estimate how much you need to do for the tP (reason: the expected implementation effort for the tP is estimated with reference to the implementation effort required for a _typical_ iP).%%
</div>
{#====================================================================================================================#}
<span id="heading_generate_new_jar">Generate a new JAR file</span>
<div id="desc_generate_new_jar">

* Generate a new JAR file using Gradle %%(Gradle can bundle the JavaFX third-party library into the jar file. If you do not bundle JavaFX with the JAR file, the application will not work in computers that don't have JavaFX installed)%%. Refer to the [_Gradle tutorial_ @SE-EDU/guides](https://se-education.org/guides/tutorials/gradle.html#creating-jar-files) to find how.<br>
==If the `.jar`  file is smaller than 5MB==, most likely JavaFX libraries are not inside it.
* There is no need to create a release in GitHub with this jar file (although you are welcome to).
</div>
{#====================================================================================================================#}
<span id="heading_write_full_commit_messages">Write some full commit messages</span>
<div id="desc_write_full_commit_messages">

* While we do not require you to write _full_ commit messages (i.e., including a message body) in the work done in this course, it is still good to learn how to write such commit message. The purpose of this task is to give you some practice in writing such full and well-written commit messages.
* Requirements:
  1. Write full commit messages for at least 2-3 commits that you push this week.
  1. Follow these [_Git conventions for the commit message body_ as specified by @SE-EDU/guides](https://se-education.org/guides/conventions/git.html#commit-message-body) when writing them.
  1. Git tag one of those commits as `A-FullCommitMessage`.
</div>
{#====================================================================================================================#}
<span id="heading_finalize_features">Finalize the features</span>
<div id="desc_finalize_features">

* **Ensure the product can handle common errors <tooltip content="should not crash the app or render it unusable; user should be notified of the problem">gracefully</tooltip>**, such as the user making an unintentional error in the command, or the data file not being found in the expected location.
* {{ icon_important_big_red }} **Ensure that the name of the product name is not `Duke`** (as required by [Level-0](../se-book-adapted/projectDuke/index.html#level-0-rename-greet-exit)){% if cs2103 %}<br>
   and the name is shown correctly everywhere it appears in the UI e.g., title bar of the GUI{% endif %}.
  * Reminder: You may give the product any name, but do not rename the repo.
  * Reminder: You can give the chatbot any personality (there is no need to follow the exact command/response formats given)
* {{ icon_important_big_red }} **Remember to give credit for any code you reused** or solutions you adopted from others. Reuse without giving credit is plagiarism and **will be reported to the university for disciplinary action**.

{{ embed_topic("appendixB-policies.md#policy-reuse", "Admin " + icon_embedding + " **Course Policies → Policy on Reuse**", "1", indent="1") }}

{{ show_faq("ipMoreCodeQualityFeedback") }}
</div>
{#====================================================================================================================#}
<span id="heading_set_up_website">Set up a product website</span>
<div id="desc_set_up_website">

<div  tags="m--cs2103" id="ip-ui-png">

* **Add a representative screenshot** of the product to the `docs` folder.
  * ==The file should be in the `docs` folder and named `Ui.png` exactly== (even if the file format is not `png`, name it `png`)
  * `Ui.png` should show the _full_ GUI window (i.e., not just the part containing the chat messages).
  * `Ui.png` should be a _single_ GUI window (i.e., do not stitch multiple screenshots together).
  * Ideally, the product name should visible in the screenshot e.g., in the title bar of the Window
  * Also note the tips given in the panel below:

{{ embed_topic("tp-deliverables-website-fragment.md#tips-for-product-screenshot", "Admin " + icon_embedding + " Team Project (tP) → Tips for Product Screenshots", "3", indent="2") }}
</div>

* **Add a brief User Guide (UG)**

<div class="indented">

<include src="dukeFragment.md" boilerplate var-header="**`A-UserGuide`: User Guide**" var-fragment="extensions-fragment.md#A-UserGuide" />
</div>
<p/>

<div  tags="m--cs2103" id="ip-ui-png-test">

* {{ icon_tip }} If you added the `Ui.png` correctly and set up the product website correctly, ==you should be able to **see your screenshot in the [iP Showcase](ip-showcase.html) page**== %%(a link to the iP Showcase page is also available in the top navigation menu → Links)%% and you should be able to access the image using the link `https://{your user name}.github.io/{repo name}/Ui.png` (e.g., `https://johndoe.github.io/ip/Ui.png`).
</div>
</div>
{#====================================================================================================================#}
<span id="heading_submit_the_final_version">Submit the final version</span>
<div id="desc_submit_the_final_version">

1. **Double-check to confirm your iP meets the criteria for full marks**:
  {{ embed_topic(baseUrl+"/admin/ip-grading.md#main", "Admin " + icon_embedding + " **iP - Grading**", "1", indent="1") }}
2. **Create a new jar file**
   * Create the JAR file {% if cs2103%}[using Gradle](https://se-education.org/guides/tutorials/gradle.html) -- this needs to be a [fat JAR file](https://se-education.org/guides/tutorials/jar.html#fat-jar-files:~:text=given%20here.-,Fat%20JAR%20files,-A%20normal%20JAR) (hence, it's best created [using Gradle's shadow plugin](https://se-education.org/guides/tutorials/jar.html#:~:text=Creating-,JAR%20files,With%20Gradle,-With%20IntelliJ%20IDEA)).{% else %}in one of these ways:
     * If you have added a GUI or using third-party libraries: [use Gradle](https://se-education.org/guides/tutorials/gradle.html).
     * Else: you can use IntelliJ.{% endif %}
   * The JAR file should be ==cross-platform and should work in a computer that has Java 17== (but no other Java version). To avoid version compatibility issues, we strongly recommend the following approach:
      1. Open a terminal window, and navigate to the root of your project folder.
      1. Run the `java -version` command to confirm the terminal is using Java 17.
      1. Run the `./gradlew clean shadowJar` command to create the JAR file.
3. **Do the following [_smoke tests_](https://en.wikipedia.org/wiki/Smoke_testing_(software))** to ensure the jar file works %%(reason: a similar flow will be used when grading your iP)%%.<br>
   1. Copy the jar file to an empty folder and test it from there. This should surface issues with hard-coded file paths.<br>
      When running the jar file for smoke testing, instead of double-clicking the jar file, do the following: open a terminal -> navigate to the jar location -> run the `java -jar "JAR_FILE_NAME"` command.
   1. Pass the jar file to team members and ask them to do a test drive. Assuming some of your team members' OS differ from yours, this should verify if the app is cross-platform.<br>
      {{ icon_tip }} If you don't have ready access to a specific OS, post a link to your JAR in the forum and ask
     others to help with the smoke testing -- some of them will even appreciate the opportunity to help a classmate.<br>
     {{ icon_info }} Note that concepts you encounter while doing course project tasks (e.g., _smoke testing_) are in the [scope of the final exam](exams.html#:~:text=you%20are%20expected%20to%20be%20aware%20of%20SE%2Drelated%20things%20(i.e.%2C%20tools%2C%20techniques%2C%20concepts)%20encountered%20while%20dong%20the%20iP%20and%20the%20tP).
4. **Create a new release on GitHub** (e.g., `v0.2`) and upload the JAR file.
   * Recommended to refrain from uploading multiple JAR files as this can cause extra work for the evaluators.

<div class="indented">

<include src="dukeFragment.md" boilerplate var-header="**`A-Release`: Release**" var-fragment="extensions-fragment.md#A-Release" />
</div>
<p/>
</div>
{#====================================================================================================================#}
<span id="heading_get_more_out_of_the_ip">[Optional] Get more out of the iP</span>
<div id="desc_get_more_out_of_the_ip">
<div class="indented">

**If you wish to cite the iP in your resume**, you can do more to make it look more impressive to a potential employer. These improvements are not considered for grading and can be done after the semester is over. Some ideas:
* **Improve the GUI**: Make the UI look nicer, unique, and memorable. You can get inspiration from [what others have done](ip-showcase.html) (but remember to give credit if you reuse any code from them).
* **Add a demo** video or an animated gif to your user guide to show how the app works.
* **Improve code quality**: iP is the right size to cite as an example of your code quality. You can use the RepoSense link (<span class="badge rounded-pill bg-light text-dark text-monospace">**&lt;/>**</span>) in the [iP showcase page](ip-showcase.html) to point to your iP code.
* **Add more features.**

{{ icon_tip }} On a somewhat related note, you can also **create similar product websites for your other projects** (projects from other courses, pet projects).


</div>

</div>
{#====================================================================================================================#}
<span id="heading_add_an_extension">Add an extension</span>
<div id="desc_add_an_extension">

* Add at least one extension of your choice, selected from [category B, C, or D](../se-book-adapted/projectDuke/index.html#extensions-category-b) i.e., pick just one item from one category (i.e., one extension in total, not one from _each_ category) e.g., `B-DoWithinPeriodTasks` or `C-Sort` or `D-Places`
* Recommended to add the extension via a branch (branch name is up to you). Optional to add it via a PR.
* Add a ==tag named `BCD-Extension`== to the corresponding commit.<br>
Irrespective of the exact extension you did, the tag name should be `BCD-Extension`.

<div class="indented-level2">

{{ icon_important_big_red }} Discuss with your team members to ensure that each member picks a different extension.


{{ icon_tip }} You may want to pick an extension that is potentially relevant to your tP so that the code can be reused in the tP later, if possible.
</div>
</div>
{#====================================================================================================================#}
<span id="heading_start_next_week_tasks">Start next week's tasks</span>
<div id="desc_start_next_week_tasks">

* If you are done with this week's iP tasks, you may also start on next week's iP tasks if you wish.

</div>
{#====================================================================================================================#}

{% macro get_id_list(increments) -%}
{% set id_list = [] %}
{% for i in increments %} {% set id_list = (id_list.push('`' + i.id + '`'), id_list) %} {% endfor %}
{{ id_list | join(", ") }}
{%- endmacro %}
{#====================================================================================================================#}

{% macro get_xp_step_heading(step, tasks_file, is_summary=false) -%}
{% set deadline_type = step.deadline_type if step.deadline_type else 'danger' %}
{% set deadline_badge = timing_badge(step.deadline, deadline_type if is_summary else 'secondary') if step.deadline else ''  %}
{% set grading_badge = (' ' + icon_graded) if step.graded else ''  %}
{% if step.id == 'add_increments' %}
{% set prefix = "Add Increment" + ("" if (step.increments | length) == 1 else "s") %}
{{ prefix }}{{ step.suffix }}: {{ (get_id_list(step.increments) | trim)}} {{ deadline_badge }}
{% else %}
<include src="{{ tasks_file }}#heading_{{ step.id }}" trim inline /> {{ deadline_badge }}{{ grading_badge }}
{% endif %}
{%- endmacro %}
{#====================================================================================================================#}

{% macro show_xp_step(number, step, tasks_file) %}

#### {{ thumb(number) }} {{ get_xp_step_heading(step, tasks_file) | trim }}

{% if step.id == 'add_increments' %}
  {% if step.pre != '' %}
<include src="{{ tasks_file }}#extra_{{ step.increments[0].id }}" optional />
  {% endif %}
  {% for i in step.increments %}
    {% set file = 'text.md' if i.id[0] == 'L' else 'extensions-fragment.md' %}
    {% set tag = ('var-tag=' + i.tag) if i.tag else '' %}
<include src="{{ tasks_file }}#pre_{{ i.id }}" optional />
<include src="dukeFragment.md" boilerplate var-header="**`{{ i.id }}`: {{ i.title }}**" {{ tag }} var-fragment="{{ file }}#{{ i.id }}" />
<include src="{{ tasks_file }}#post_{{ i.id }}" optional />
  {% endfor %}
{% else %}
<include src="{{ tasks_file }}#desc_{{ step.id }}" />
{% endif %}
<p/>
{% endmacro %}

{#====================================================================================================================#}

{% macro show_xp_steps(steps, tasks_file) %}
{% for step in steps %}
{{ show_xp_step(loop.index, step, tasks_file) }}
{% endfor %}
{% endmacro %}
{#====================================================================================================================#}

{% macro show_xp_steps_summary(steps, tasks_file) %}
{% call show_project_summary_lead()%}
{% for step in steps %}1. {{ get_xp_step_heading(step, tasks_file, is_summary=true) | trim }}
{% endfor %}
{% if (steps | length) == 0 %}&nbsp;%%None assigned for this week%%{% endif %}
{% endcall %}
{% endmacro %}
{#====================================================================================================================#}

{% macro show_xp_page(week_num, steps, tasks_file) %}
<div id="main">

{{ show_xp_steps_summary(steps, tasks_file) }}

<div id="body">

<include src="{{ tasks_file }}#{{ course | lower }}-week{{ week_num }}-intro" optional/>
<p/>

{{ show_xp_steps(steps, tasks_file) }}

<include src="{{ tasks_file }}#{{ course | lower }}-week{{ week_num }}-outro" optional/>
</div>
</div>
{% endmacro %}
{#====================================================================================================================#}

{% macro show_ip_page(week_num) %}
{{ show_xp_page(week_num, weekly_ip_tasks['week' + week_num], 'ip-tasks-fragment.md') }}
{% endmacro %}
{#====================================================================================================================#}

{% macro show_admin_ip_page(week_num) %}
{% call show_admin_page("ip-w" + week_num) %}
{{ show_ip_page(week_num) }}
{% endcall %}
{% endmacro %}
