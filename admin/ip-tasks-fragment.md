{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/topics.njk" import panopto with context %}
{% from "common/macros.njk" import button, embed_topic, get_date, step, thumb, timing_badge with context %}
{% from "_module-" + module + "/weeklyIpTasks-fragment.md" import weekly_ip_tasks with context %}

{#====================================================================================================================
 # Common text segments
 #====================================================================================================================#}
<div id="ip-faq">
<box type="info" icon=":fas-question-circle:" light>

#####  **FAQ** about iP increments{.text-info}

<panel type="seamless" header="**Q.** How are the iP git tags used in grading?">

**A.** A git tag is a self-declaration that you _think_ you are done with the iP increment. We take your word for it. We don't check the code to see if you have actually done the said increment. Therefore, it is just a mechanism for you to self-declare progress and for us to monitor those progress declarations.
</panel>
<panel type="seamless" header="**Q.** What if I discovered a bug after I finished an increment?">

**A.** Go ahead and fix it in a subsequent commit. There is no need to update the previous commit or move the corresponding tag to the new commit. As we do not test your code at every tag, earlier bugs will not affect your grade as long as they are fixed later. Similarly, feel free to improve the code of previous increments later.
</panel>
<panel type="seamless" header="**Q.** I did multiple increments in the same commit. How to fix?">

**A.** You can add the corresponding tags to the same commit.<br>
Optionally, if you haven't pushed the commit to the fork yet, you can try to figure out how to split that commit into multiple commits.
</panel>
<panel type="seamless" header="**Q.** The requirements of an increment scheduled for this week is already satisfied by the work I did in an earlier week. What now?">

**A.** You can add the corresponding tag to the earlier commit (or the latest commit -- it doesn't matter) and push the tag.
</panel>
<panel type="seamless" header="**Q.** My iP increments are not detected by the dashboard because I forgot to push my tags earlier. What now?">

**A.** Not to worry. Just push the tags now. They will be detected by the dashboard at the next update. There is no penalty if mistakes are detected and fixed soon after.
</panel>
<panel type="seamless" header="**Q.** Oh no! I made a mistake in my tag/branch name.">

**A.** It's OK; correct it now.
</panel>
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
  * **`git tag` the commit with the exact increment** ID e.g., `Level-2`, `A-TextUiTesting`
    <box type="warning" seamless><md>[Git tags](../book/gitAndGithub/tag/) are not the same as [Git commit messages](../book/gitAndGithub/commit/).</md></box>
  * **`git push` the code to your fork**
    <box type="warning" seamless><md>Git doesn't push tags unless you [specifically ask it to](../book/gitAndGithub/push/).
    After pushing a tag to your fork, you should be able to see that tag by visiting `https://github.com/YOUR_USER_NAME/REPO_NAME/tags` e.g., https://github.com/se-edu/addressbook-level3/tags</md></box>
    <box type="tip" seamless><md>If you encounter issues connecting Sourcetree with your GitHub account, refer to these [Sourcetree Tips](https://se-education.org/guides/tutorials/sourcetree.html).</md></box>

* Remember to take note of our plagiarism policies, if you haven't done so already:

{{ embed_topic("policies-fragment.md#policy-reuse", "Admin " + icon_embedding + " Policies -> **Reuse**", "1", indent=2, type="danger") }}

<include src="ip-tasks-fragment.md#ip-faq" />

</div>
<div id="volatile-requirements">

<box type="info" dismissible>

The iP (and the tP) undergoes changes after each semester. As such, teething issues are a possibility. If you encounter any problem while doing the iP/tP, please post in the [forum]({{ url_forum }}) so that we can take necessary actions.
</box>
</div>
<div id="no-jumping-ahead">

<box dismissible>

{{ icon_important_big_red }} We discourage you from doing project tasks allocated to future weeks. Reasons: In order to help you gain <tooltip content="the ability to apply knowledge or do tasks effortlessly as if you have been doing them for a long time">_fluency_</tooltip> (and also to better simulate real projects), **we want the project work to be <tooltip content="done at multiple times with time gaps in between">_spaced_</tooltip> and span a longer period**, rather than to be done as a short burst.

Reminder: as per iP grading criteria, _some_ increments need to to be done in each week for you to get full marks.
</box>
</div>
<div id="follow-instructions">

<box dismissible>

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

<box dismissible>

**:fas-clock: Deadline:**

Note the typical deadline weekly project tasks:
{{ embed_topic("weeklySchedule.md#deadline-definition", "Admin " + icon_embedding + " Weekly schedule → **Deadline for weekly tasks**", "1") }}
<p/>

But ==as there are no tutorials this week, you have until the next lecture== to finish this week's iP tasks.
</box>
</div>
<div id="cs2103-week3-intro">

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

{#====================================================================================================================#}
{# Steps
{#====================================================================================================================#}
<span id="heading_learn_about_the_project">Learn about the project</span>
<div id="desc_learn_about_the_project">

* **Read the following two sections**, if you haven't done so already:

{{ embed_topic("ip-overview.md#main", "Admin " + icon_embedding + " **iP - Overview**", "3", indent="2") }}
{{ embed_topic("ip-grading.md#main", "Admin " + icon_embedding + " **iP - Grading**", "1", indent="2") }}
</div>
{#====================================================================================================================#}
<span id="heading_set_up_prerequisites">Set up prerequisites</span>
<div id="desc_set_up_prerequisites">

* **Ensure you have followed the <span class="ps-1 pe-1" style="color:purple; border: 0.5px solid lightgrey">:fas-hard-hat: Preparation</span> sections of the following module tools:**

{{ embed_topic("programmingLanguages.md#main", "Admin " + icon_embedding + " **Programming Language**", "2", indent="2") }}
{{ embed_topic("tools.md#rcs", "Admin " + icon_embedding + " **Tools → Git**", "2", indent="2") }}
{{ embed_topic("tools.md#github", "Admin " + icon_embedding + " Tools → **GitHub**", "2", indent="2") }}
{{ embed_topic("tools.md#ide", "Admin " + icon_embedding + " Tools → **Intellij IDEA**", "2", indent="2") }}
</div>
{#====================================================================================================================#}
<div tags="m--cs2113 m--tic4001" id="extra_Level-0">

<include src="ip-tasks-fragment.md#commit" />
</div>
<div id="extra_Level-1">

<include src="ip-tasks-fragment.md#order" />
{% if cs2103 %}<include src="ip-tasks-fragment.md#commit" />{% endif %}
<include src="ip-tasks-fragment.md#tag-push" />
</div>
{#====================================================================================================================#}
<span id="heading_set_up_project">Set up the project in your computer</span>
<div id="desc_set_up_project">

<box>

Read through this week's topics before starting the project.<br>
 **If you encounter technical problems** while doing the iP, follow the guidelines given below:

{{ embed_topic("appendixD-help.md", "Admin " + icon_embedding + " Appendix D: Getting Help", "2") }}
</box>

1. **Fork** [{{ url_module_org }}/{{ ip_repo_name }}]({{ url_module_org }}/{{ ip_repo_name }}), while noting the points below:<br>
   <box type="important" seamless><md>**==Keep the fork name== as `{{ ip_repo_name }}`** or else our grading scripts will not be able to detect it. You can change the fork name to something else after the semester (and the grading) is over e.g., after receiving your grade for the module.</md></box>
   <box type="tip" seamless><md>**Untick the `[ ] Copy the master branch only` option** so that you get a copy of the full repo.</md></box>
1. ==**Enable the issue tracker** of your fork== (Go to `Settings` of your fork, scroll to the `Features` section, and tick the `Issues` checkbox). %%Reason: at times we post feedback on your issue tracker.%%<br>
   <box type="tip" seamless><md> If the issue tracker is enabled, you should be able to visit the following URL `https://github.com/{your_user_name}/{{ ip_repo_name }}/issues`<br> e.g., `https://github.com/johnDoe/{{ ip_repo_name }}/issues`</md></box>
1. **Clone the fork** onto your computer.
1. **Set up the project in your IDE** as explained in [the README file]({{ url_module_org }}/{{ ip_repo_name }}/blob/master/README.md), unless you don't wish to use an IDE for the project.<br>

</div>
{#====================================================================================================================#}
<span id="heading_set_up_project_tic4002">Set up the project in your computer</span>
<div id="desc_set_up_project_tic4002">

* We assume you still have the iP project set up that you used for TIC4001. If not, please set it up as explained in [TIC4001 website](https://nus-tic4001-{{ previous_semester | lower }}.github.io/website/admin/ip-w2.html).
</div>
{#====================================================================================================================#}
<span id="heading_finish_leftover_tasks">Do any leftover iP tasks from the previous week</span>
<div id="desc_finish_leftover_tasks">

* Remember to do any leftover increments from the past weeks before starting on the current week's increments. This guideline applies to future weeks too.
</div>
{#====================================================================================================================#}
<span id="heading_create_pr_to_upstream">Create a PR to the upstream repo</span>
<div id="desc_create_pr_to_upstream">
{% if tic4002 %}

<box type="tip" seamless>

<span class="text-success">**If you encounter technical problems**</span>, follow the guidelines given below in seeking help:

{{ embed_topic("appendixD-help.md", "Admin " + icon_embedding + " Appendix D: Getting Help", "4", indent="2") }}
</box>

* Note that while you will be reusing the same <tooltip content="i.e., the cloned repo in your computer">_local repo_</tooltip> and the same <tooltip content="i.e., the one you forked to your GitHub account last semester">_forked remote repo_</tooltip>, you will be using a new <tooltip content="i.e., the repo you PR to">_upstream repo_</tooltip> we have set up for this semester. As a result, ==you need to create a new PR== from your fork to the new upstream repo, as given below.{% endif %}
* Create a <trigger trigger="click" for="modal:ipTasks-createPr">pull request (PR)</trigger> from your fork to the upstream repo. Note the following:
  * Create the PR from the `master` branch of your fork to the `master` branch of the upstream repo ({{ url_module_org }}/{{ ip_repo_name }}){% if tic4002 %}==Be careful to choose the new upstream repo to receive the PR.=={% endif %}
  * Set the PR name as `[{Your full/partial name or your Github username}] iP`<br>
    e.g., `[Richard Mathews Chee] iP` or `[Rich ... hee] iP` or `[TheRichMat] iP`<br>
    %%Note that the PR name will be publicly visible.%%<br>
    You may leave the description as empty.
  * If you created the PR correctly, it should appear in the list of PRs [here]({{ url_module_org }}/{{ ip_repo_name }}/pulls).
  * Steps for creating a PR is given in this textbook topic (==steps 5 onwards==):

{{ embed_topic("../book/gitAndGithub/createPRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Creating PRs**", "1", indent=2) }}

<div class="indented-level2">

<box tags="m--cs2103 m--cs2113 m--tic4001" type="info" seamless>

The PR will update automatically to reflect your latest code every time you push code to your fork. As a result, it provides a convenient way for us to access the current state of all your iP code from one location.

</box>

</div>

<modal large header="Pull Request (PR)" id="modal:ipTasks-createPr">

_Pull Requests_ is a mechanism for offering code to a repository e.g., a bug fix or a new feature. PRs allow developers to review, discuss, and refine proposed code changes before incorporating (i.e., _merging_) the new code to the repository.

Resources:
* [GitHub Help page on PRs](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests)
</modal>
</div>
{#====================================================================================================================#}
<div id="extra_Level-5">
<div tags="m--cs2113 m--tic4001">

* Do each increment as a Git branch. Here is an example:
  * Start a branch named `branch-{increment ID}` (e.g. `branch-Level-5`). You are recommended to have multiple commits in that branch. Follow the branch naming convention exactly or else our gradings scripts might miss your branch.
  * After the increment is ready, merge the `branch-Level-5` back on to `master`, ==without a _fast-forward_== so that git creates a separate commit for the merge. `git tag` that merge commit as `Level-5`.
  * Push the branch to your fork so that the grading script can detect it. As before, push the tag as well.
  * {{ icon_important_big_red }} Advanced git users: do not delete the branch after merging.
</div>
</div>
<div id="extra_A-Packages">
<div tags="m--cs2113 m--tic4001">

* Recommended: if you are new to git, do this as a separate branch too (for additional practice), similar to how you did `Level-5` (branch name `branch-A-Packages`).
</div>
</div>
<div id="extra_Level-6">
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
<div tags="m--tic4001">
<p/>

* Create a new branch `branch-Level-6`.
* Implement the increment in the new branch.
* Push the branch to your fork.
* Create a PR in your fork, from the new branch to the `master` branch.  Steps for creating a PR is given in this textbook topic (==steps 5 onwards==):

{{ embed_topic("../book/gitAndGithub/createPRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Creating PRs**", "1", indent=2) }}

* Merge the PR using GitHub. Note how to merge PRs:

{{ embed_topic("../book/gitAndGithub/managePRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Merging PRs**", "1", indent=2) }}

* Pull the `master` branch from the fork to your local repo.

</div>
</div>
<div id="extra_A-Jar">
<div tags="m--cs2113 m--tic4001">

* In case this increment does not require any code changes, you may tag the commit at which this was achieved as `A-Jar` (even if that commit has another tag already).
* Upload the jar file to your fork as explained in the panel below.
</div>
</div>
<div id="extra_Level-7">

<p/>

* Do Level 7 in a branch named `branch-Level-7`. Without merging that branch, go back to the `master` branch and implement the other increment in a separate branch named similar to the first (i.e., `branch-{increment ID}`). Now, go back to the `master` branch and merge the two branches one after the other. As before, tag the commit (in the `master` branch, after merging) that achieves the respective deliverable, and push to your fork.<br>
 {{ icon_important_big_red }} Remember to push the branches to your fork so that the grading script can detect them.<br>
 {{ icon_important_big_red }} Only _merged_ branches are detected by the script. After merging a branch `b1` to the `master` branch, you need to push both the `master` and the `b1` branches to the fork. Pushing the `master` branch does not automatically take the `b1` branch along with it just because it is already merged to the `master` branch.<br>
 {{ icon_important_big_red }} Advanced git users: do not delete the branch after merging.<br>
 {{ icon_tip }} Merge without a _fast-forward_ so that git creates a separate commit for the merge.

</div>
<span id="extra_Level-8">
<div tags="m--cs2113 m--tic4001" id="as-parallel-prs">

* **Note how to merge PRs**:

{{ embed_topic("../book/gitAndGithub/managePRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Merging PRs**", "1", indent=2) }}

* **Practice using parallel git branches _and_ PRs**, as explained below:
1. First, do each increment as a parallel branch (follow the branch naming convention you followed earlier `branch-Level-8` etc.), but do not merge any.
1. Then, push each branch to your fork, and create a PR !!within your fork!! (i.e., from the increment branch to the `master` branch). ==Be careful not to create a PR to [the upstream repo]({{ url_module_org }}/ip).== %%If you did create such a PR by mistake, no worries, just close it yourself.%%

{{ embed_topic("../book/gitAndGithub/createPRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Creating PRs**", "1", indent=2) }}

3. Now, merge one of the PRs and update the remaining PRs accordingly, as given below:
   1. Merge one of the PRs on GitHub e.g., Level-8. Remember to choose the `Create merge commit` option when merging.
   1. Pull the updated `master` branch from your fork to your Computer.
   1. Note how the remaining un-merged branches are no longer in sync with the latest `master`. To rectify, merge the `master` branch to each of them. Resolve merge conflicts, if any.
   1. Push the updated branches to your fork. The PRs will update automatically to reflect the updated branch.
   1. As before, tag the merge commit in the master branch and push the tag to your fork.
1. Merge the remaining PRs using a procedure similar to the above.
</div>
</span>
<div id="extra_A-Assertions">
<div tags="m--cs2103">

<include src="ip-tasks-fragment.md#as-parallel-prs" />
</div>
</div>
<div id="extra_A-MoreOOP">

<box tags="m--cs2103 m--cs2113" type="info" seamless>

****Why more OOP?****{.text-info}

One of the increments below asks you to push the design more towards the OOP approach. This is a good point to remind you the following points:

****Good OOP != OOP is good****: While the module pushes you to use _good OOP_, do not interpret it as a message of _OOP is good_; it's good for many situations but not so for some other situations. The best is usually a combination of approaches. Hence, you are encouraged to get better at other paradigms, the _functional_ paradigm in particular which has been rising in popularity in some areas such as big data, AI, parallel systems.<br>
That said, it is also preferable to use one paradigm as the primary approach and fallback on others only when the primary paradigm is clearly sub-optimal. Reason: mixing everything in equal measures might make the system even harder to understand.

**OOP is primary paradigm for this module and you are expected to try to push it to its limits.** That should give you a first-hand experience of OOP's strengths and weaknesses. Furthermore, OOP (or any other paradigm) will appear worse than it really is if not used correctly, and learning to use it correctly in increasingly larger systems is another objective you can aim for in this module. {% if cs2103 %}As you do the tP later, you'll also realize that while OOP is used for the internal design of its components, the higher-level design is not specifically an OOP one.{% endif %}<br>

**We do not prohibit the use of other paradigms**, however. For example, if you find a place where the _functional_ approach is better, go ahead and use it. As you know, Java supports functional programming to a certain extent. {% if cs2103 %}In fact, the tP code given to you uses small snippets of functional-style code in several places.{% endif %}
</box>

* As in the previous week, commit, tag, and push, as you do the following increments in the `master` branch (no need to use separate branches).{% if cs2103 or tic2002 %}
* {{ icon_important_big_red }} Do `A-Gradle` first, after which use the Gradle option (rather than the Intellij option) when doing `A-JUnit` and `A-JAR` as they are easier to do using Gradle.

<div class="indented-level2" id="pulling-branch-from-upstream">
<panel type="seamless" >
<span slot="header" class="card-title"><markdown>{{ icon_tip}} **If you fork doesn't have the `add-gradle-support` branch ...**{.text-success}</markdown></span>

If your fork doesn't have the `add-gradle-support` branch (i.e., you did not copy all the branched when you forked), here are the Git commands for (one of many ways of) fetching and merging the `add-gradle-support` branch from the upstream repo that you forked from:<br>

1. Add the upstream repo as a remote, and give it the name `upstream`:<br>
  `git remote add upstream {{ url_module_org }}/{{ ip_repo_name }}.git`
1. Switch to the `master` branch, if you are not on it already:<br>
   `git checkout master`
1. Fetch the `add-gradle-support` from the remote `upstream`:<br>
   `git fetch upstream add-gradle-support`
1. Merge the branch:<br>
   `git merge upstream/add-gradle-support`

Alternatively see the panel below on some general info on how to pull a branch from another remote repo, but note,

* the remote to pull _from_ is `{{ url_module_org }}/{{ ip_repo_name }}.git` (not `https://github.com/se-edu/samplerepo-things-2.git`)
* the repo to pull _to_ is your local repo used for the project (not `samplerepo-things`)
* the branch to pull is `add-gradle-support` (not `master`)

{{ embed_topic("../book/gitAndGithub/pull/text.md#section-working-with-multiple-remotes", "Textbook " + icon_embedding + " Git&Github → Pull → **Working with multiple remotes**", "2") }}
</panel>
<p/>
</div>

{% endif %}

</div>
<div id="extra_A-JavaDoc">

* As in the step 1 above, implement these three increments ==as three <tooltip content="i.e., start a branch, add some code to it, go back to the master branch (without merging the first branch), and start another branch, and so on">parallel</tooltip> branches== first (branch names: `branch-A-JavaDoc`, `branch-A-CodingStandard`, `branch-Level-9`), and then merge them one-by-one. Hopefully, you will encounter some merge conflicts so that you get to practice de-conflicting branches.
* The Java and Git standards to follow (for `A-CodingStandard`) are given in [this page](standardsAndConventions.html).
* After finishing, assuming you encountered merge conflicts (and some were rather painful to resolve), think of how such conflicts could have been reduced %%(e.g., by changing the order of merging, or minimizing parallel branches when certain type of changes are being done to the code)%%.
</div>
{#====================================================================================================================#}
<span id="heading_ensure_tic4001_increments">Ensure TIC4001 iP increments have been done</span>
<div id="desc_ensure_tic4001_increments">

* Ensure that following increments (that were due in TIC4001) have been done. Improve their implementation, if the current implementation is weak (in your own opinion). %%For example, you can add _more_ JavaDoc comments or JUnit tests even if the current code has them already.%%
<include src="dukeFragment.md" boilerplate var-header="**`Level1`: Greet, Echo, Exit**" var-fragment="text.md#Level-1" />
<include src="dukeFragment.md" boilerplate var-header="**`Level2`: Add, List**" var-fragment="text.md#Level-2" />
<include src="dukeFragment.md" boilerplate var-header="**`Level3`: Mark as Done**" var-fragment="text.md#Level-3" />
<include src="dukeFragment.md" boilerplate var-header="**`Level4`: ToDo, Event, Deadline**" var-fragment="text.md#Level-4" />
<include src="dukeFragment.md" boilerplate var-header="**`Level4`: ToDo, Event, Deadline**" var-fragment="text.md#Level-4" />
<include src="dukeFragment.md" boilerplate var-header="**`Level5`: Handle Errors**" var-fragment="text.md#Level-5" />
<include src="dukeFragment.md" boilerplate var-header="**`Level6`: Delete**" var-fragment="text.md#Level-6" />
<include src="dukeFragment.md" boilerplate var-header="**`Level7`: Save**" var-fragment="text.md#Level-7" />
<include src="dukeFragment.md" boilerplate var-header="**`Level9`: Find**" var-fragment="text.md#Level-9" />
<br>
<include src="dukeFragment.md" boilerplate var-header="**`A-AbstractClasses`: Use Abstract Classes**" var-fragment="extensions-fragment.md#A-AbstractClasses" />
<include src="dukeFragment.md" boilerplate var-header="**`A-MoreOOP`: Use more OOP**" var-fragment="extensions-fragment.md#A-MoreOOP" />
<include src="dukeFragment.md" boilerplate var-header="**`A-Packages`: Use Packages**" var-fragment="extensions-fragment.md#A-Packages" />
<include src="dukeFragment.md" boilerplate var-header="**`A-JavaDoc`: Add JavaDoc comments**" var-fragment="extensions-fragment.md#A-JavaDoc" />
<include src="dukeFragment.md" boilerplate var-header="**`A-JUnit`: Add JUnit Tests**" var-fragment="extensions-fragment.md#A-JUnit" />

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
* Requirements: Update <tooltip content="click on the the `...` icon on the top right corner of the previous description and choose `Edit`">(how?)</tooltip> the description of the iP PR you created earlier (<span class="text-danger">do not add a new comment</span>) so that it contains the following GFMD elements:
  1. a heading
  1. a bullet list
  1. a numbered list
  1. a fenced code block (with syntax highlighting)
  1. a task list
  1. an emoji
  1. a blockquote
  1. a hyper link
  1. inline code
  1. some text formatting: bold, italic, stikethrough etc.

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

If you Java programmer, you can use it to practice Java too. Here's the `main` method:
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

<div tags="m--cs2103 m--tic4001">

<box type="wrong" add-class="ml-4" icon=":fas-hand-paper:" icon-size="2x" seamless>

**Please wait till {{ date_w4_start | date(format_normal, 3) }}** to start this task, to give others a few extra days to create the PR if they haven't done so yet.
</box>
</div>

<box type="info" add-class="ml-4">

This task is worth `2x2=4` participation points.
</box>

* **Learn _how_ you should review PRs in this task**:

{{ '' if cs2113 else panopto('c001244c-01b5-4471-ab9d-ac1b0098110a') }}

{{ embed_topic("../book/gitAndGithub/reviewPRs/text.md#body", "Textbook " + icon_embedding + " Git & GitHub → **Reviewing PRs**", "1", indent=2) }}

* {{ step(1) }} **Note these additional guidelines**:
  * Read the [_Best practices for reviewing PRs_ @SE-EDU/guides](https://se-education.org/guides/guidelines/PRs-reviewing.html). You are ==expected to follow all of them==.
  * Make sure you ==add 'review comments' (not regular comments)== as only those are counted for participation. See step 4 in the panel above to find how to add 'review comments'.
  * If the PR has received some review comments already, feel free to confirm/complement/question those comments in your review. Also, look for things the previous reviewers may have missed.
  * At the end of the review, choose `Comment` (i.e., not `Approve` or `Request changes`)

* {{ step(2) }} **Do the first PR review** as follows.
  * Give comment on ==[coding standard]({{ url_java_coding_standard }}) related issues only==.<br>
    Review comments don't always have to be about problems in the code. Other things you can do:
    * complement the author on not making a common mistake
    * ask questions
    * suggest alternatives
  * The review allocation is given in the panel below.

<div class="indented-level4">

<include src="common-tutorials-fragment.md#show-ip-peer-review-allocation-1" />
</div>

* {{ step(3) }} **Do the second PR review** as follows.
  * Comment on ==other code quality guidelines== (see the <span tags="m--cs2103">section _Naming_</span><span tags="m--cs2113 m--tic4001">sections on _Naming_ and _Readability_</span> in [this textbook chapter](../se-book-adapted/chapters/codeQuality.html)) you have learned so far. It's optional to comment on coding standard violations in this PR review.
  * The review allocation is given in the panel below.

<div class="indented-level4">

<include src="common-tutorials-fragment.md#show-ip-peer-review-allocation-2" />
</div>

* {{ step(4) }} **[When you receive reviews for your own PR] Respond to comments received**. You are recommended to (but not obliged to) respond to comments received from peers, especially if the PR reviewer asked you for more info. As mentioned in [these guidelines](https://se-education.org/guides/guidelines/PRs-reviewing.html), do not get into arguments with PR reviewers/authors.

</div>
{#====================================================================================================================#}

<span id="heading_learn_from_others">Learn from others (optional)</span>
<div id="desc_learn_from_others">

* **You can use the [iP Code Dashboard]({{ url_ip_dashboard }}) to view others' iP code**, using the `Links → iP Code Dashboard` item in the top navigation menu of this module website. Click on the <span class="badge bg-light text-dark">%%**:fas-code:**%%</span>&nbsp;icon corresponding to a student name to see the code written by that person. We encourage you to read others’ code and learn from them. If you adopt solutions from others (also encouraged), please follow our reuse policy. 

{{ embed_topic("appendixB-policies.md#policy-reuse", "Admin " + icon_embedding + " **Module Policies → Policy on Reuse**", "1", indent=2) }}

</div>
{#====================================================================================================================#}

<span id="heading_evaluate_peer_ips">Evaluate two peer iPs</span>
<div id="desc_evaluate_peer_ips">

<div class="indented-level2">

<box type="info">

This activity is worth `2x2=4` participation points.
</box>

</div>

1. {% if cs2113 %}**The allocation will be sent via email**, by Monday 2359.{% else %}**Wait for the email notifying you which iPs are allocated for you to evaluate**. When the email is sent out, it will also be announced via module announcements.{% endif %}
1. **Download the _latest_ JAR file** of the first iP by following the link provided.
   <box type="info" icon=":fas-question:" seamless>

   **FAQ**: What if the student has not uploaded a JAR file, or the JAR file doesn't work at all?<br>
   **A**: When you submit the evaluation (step 7 below), there will be a way to indicate that the JAR was not available, or any other serious issues you faced.
   </box>
1. **Locate the User Guide** of the app by following the link provided.
1. **Open the Canvas survey** (the one named `iP Peer Evaluation 1`) that you will be using to submit your evaluation and take note of the things you need to evaluate.
1. **Do a light testing of the app** (not more than 10 minutes) to ensure the claimed features actually exist.<br>
   {{ icon_important_big_red }} Make sure you are using Java 11 to run the jar file (use `java -version` command to confirm).<br>
   {{ icon_tip }} If double-clicking the jar file doesn't work, use the `java -jar {file_name}` command to open it.
1. **Do a quick examination of the code** (~ 5 minutes) by following the provided link.
1. **Submit your evaluation** using the survey.
1. **Repeat the above steps for the 2nd iP** allocated to you (use the survey `iP Peer Evaluation 2`).
1. %%**Take note of the effort required for a _typical_ iP**: Now that you have seen two more iPs, you should now be in a better position to estimate how much you need to do for the tP (reason: the expected workload for the tP is that each team member puts in about one _typical_ iP worth of effort).%%
</div>
{#====================================================================================================================#}
<div id="extra_A-Gradle">

{% if tic4002 %}
* As before, after an increment has been completed, tag the commit using the increment ID (e.g., `A-Gradle` in this case) and push that tag to your fork.
* You are recommended to do each new increment in a separate branch.
* If you have done the increment in the previous semester already and the tag has been pushed to the repo, no further action needed.
{% else %}
* **Do each enhancement in a separate branch and merge to the `master` branch only when ready** (reason: if you push incomplete features into the `master` branch, it can confuse others reviewing your PR). There is no need to do the increments as _parallel_ branches though %%i.e., you can do one increment and merge that branch before starting on the next one%%.
<br>
{{ icon_tip }} If you have completed any of them in previous weeks, just add the corresponding tag (no need to create a branch).
{% endif %}
</div>
{#====================================================================================================================#}
<div id="post_Level-10">

<div class="indented-level2">

* Note that you no longer need to keep the text-based UI after adding a GUI. Similarly, there is no need to use the I/O redirection style automated testing anymore (that technique is suited for text UIs only).
</div>
</div>
{#====================================================================================================================#}
<span id="heading_generate_new_jar">{{ "Release" if tic4002 else "Generate" }} a new JAR file</span>
<div id="desc_generate_new_jar">

* Generate a new JAR file using Gradle %%(Gradle can bundle the JavaFX third-party library into the jar file. If you do not bundle JavaFX with the JAR file, the application will not work in computers that don't have JavaFX installed)%%. Refer to the [_Gradle tutorial_ @SE-EDU/guides](https://se-education.org/guides/tutorials/gradle.html#creating-a-jar-file) to find how.<br>
==If the `.jar`  file is smaller than 5MB==, most likely JavaFX libraries are not inside it.
* {% if tic4002 %}Make a new release on GitHub and upload the JAR file. You may use any appropriate version number for it.{% else %}There is no need to create a release in GitHub with this jar file (although you are welcome to).{% endif %}
</div>
{#====================================================================================================================#}
<span id="heading_write_full_commit_messages">Write some full commit messages</span>
<div id="desc_write_full_commit_messages">

* While we do not require you to write _full_ commit messages (i.e., including a message body) in the work done in this module, it is still good to learn how to write such commit message. The purpose of this task is to give you some practice in writing such full and well-written commit messages.
* Requirements:
  1. Write full commit messages for at least 2-3 commits that you push this week.
  1. Follow these [_Git conventions for the commit message body_ as specified by @SE-EDU/guides](https://se-education.org/guides/conventions/git.html#commit-message-body) when writing them.
  1. Git tag one of those commits as `A-FullCommitMessage`.
</div>
{#====================================================================================================================#}
<div id="extra_A-Assertion">

* Add the following increments, doing each in the following manner:
1. add the extension in a separate branch
1. push the branch to your fork
1. create PR within your fork (i.e., from the new branch, to the `master` branch)
1. merge the PR; you can try various merge options such as `Squash and Merge`, `Rebase and Merge`
1. sync your local clone with the fork
</div>
{#====================================================================================================================#}
<div id="extra_A-CI">

{% if not tic4002 %}* We recommend that ==at least one member== of the team attempt the following.{% endif %}
</div>
{#====================================================================================================================#}
<span id="heading_finalize_features">Finalize the features</span>
<div id="desc_finalize_features">

* You may give the product any name, but do not rename the repo.
* Reminder: you can give the chatbot any personality (there is no need to follow the exact command/response formats given)
* {{ icon_important_big_red }} Remember to give credit to any code you reused or solutions you adopted from others. Reuse without giving credit is plagiarism and **will be reported to the university for disciplinary action**.

{{ embed_topic("appendixB-policies.md#policy-reuse", "Admin " + icon_embedding + " **Module Policies → Policy on Reuse**", "1", indent="2") }}
</div>
{#====================================================================================================================#}
<span id="heading_set_up_website">Set up a product website</span>
<div id="desc_set_up_website">

<div  tags="m--cs2103 m--tic4002" id="ip-ui-png">

* **Add a representative screenshot** of the product to the `docs` folder.
  * ==The file should be in the `docs` folder and named `Ui.png` exactly== (even if the file format is not `png`, name it `png`)
  * Ideally, the product name is visible in the screenshot e.g., in the title bar of the Window

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

{% if not (tic4001 or tic4002) %}
* {{ icon_deadline }} **Soft deadline**: midnight before the tutorial
{% endif %}
* **Create a new jar file**
  * Create the JAR file {% if tic4002 or cs2103%}[using Gradle](https://se-education.org/guides/tutorials/gradle.html).{% else %}in one of these ways:
    * If you have added a GUI or using third-party libraries: [use Gradle](https://se-education.org/guides/tutorials/gradle.html).
    * Else: you can use Intellij.{% endif %}
  * The JAR file should be ==cross-platform and should work in a computer that has Java 11==.
* **Do the following [_smoke tests_](https://en.wikipedia.org/wiki/Smoke_testing_(software))** to ensure the jar file works %%(reason: a similar flow will be used when grading your iP)%%.<br>
  1. Copy the jar file to an empty folder and test it from there. This should surface issues with hard-coded file paths.
  1. Pass the jar file to team members and ask them to do a test drive. Assuming some of your team members' OS differ from yours, this should verify if the app is cross-platform.<br>
     {{ icon_tip }} If you don't have ready access to a specific OS, post a link to your JAR in the forum and ask
     others to help with the smoke testing -- some of them will even appreciate the opportunity to help a classmate.
* **Create a new release on GitHub** (e.g., `v0.2`) and upload the JAR file.
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

{{ icon_tip }} On a somewhat related note, you can also **create similar product websites for your other projects** (projects from other modules, pet projects).


</div>

</div>
{#====================================================================================================================#}
<span id="heading_add_an_extension">Add an extension</span>
<div id="desc_add_an_extension">

* Add at least one extension of your choice, selected from [category B, C, or D](../se-book-adapted/projectDuke/index.html#extensions-category-b) i.e., pick just one item from one category e.g., `B-DoWithinPeriodTasks` or `C-Sort` or `D-Places`{% if not tic4002 %}
* Recommended to add the extension via a branch (branch name is up to you). Optional to add it via a PR.{% endif %}
* Add a ==tag named `BCD-Extension`== to the corresponding commit.

<div class="indented-level2">

{{ icon_important_big_red }} Discuss with your team members to ensure that each member picks a different extension.


{{ icon_tip }} You may want to pick an extension that is potentially relevant to your tP so that the code can be reused in the tP later, if possible.
</div>
</div>
{#====================================================================================================================#}
<span id="heading_stricter_coding_standard">Apply a stricter coding standard</span>
<div id="desc_stricter_coding_standard">

<div class="indented">

In TIC4001, you applied only the _basic_ rules of the Java coding standard. TIC4002 raises the bar to ==cover _intermediate_ rules as well==. Update your code to comply with that new bar.

Tag to apply to the commit: `A-StricterCodingStandard`.

See the [Standards/conventions page](standardsAndConventions.md) for more info.

Implementing the following increment (optional) can be help with the above.
</div>

<include src="dukeFragment.md" boilerplate var-header="**`A-CheckStyle`: Use CheckStyle**" var-fragment="extensions-fragment.md#A-CheckStyle" />

</div>
{#====================================================================================================================#}
<span id="heading_more_code_quality">Increase code quality even further</span>
<div id="desc_more_code_quality">

* Increase the code quality by applying the [code quality guidelines covered in the textbook](../se-book-adapted/chapters/codeQuality.html). Even if you have done this previously in TIC4001, have another look to see if the code quality can be improved further.
* Remember to commit each refactoring separately and give a descriptive commit message (also pay attention to the [Git commit message conventions](standardsAndConventions.md) given).
* Tag to apply to the commit: `A-HigherCodingQuality`.

</div>
{#====================================================================================================================#}
<span id="heading_update_website">Update the website</span>
<div id="desc_update_website">

* Update the product website in the following ways:
  * Move the **User Guide** to a separate page (filename: `docs/UserGuide.md`) and update it to match the current version of the product.
  * Add a **Developer Guide**  (filename: `docs/DeveloperGuide.md`), similar to (but can be shorter) what you did for the tP in TIC4001.
    * Recommended length 1.5-2.5 pages
    * Include some class/object/sequence diagrams, user stories, and some non-functional requirements
    * Optional to include an architecture diagram
  * Update the **README** page to make it a landing page for your iP website (similar to the TIC4001 tP website).

<include src="ip-tasks-fragment.md#ip-ui-png"/>
<include src="ip-tasks-fragment.md#ip-ui-png-test"/>
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

<include src="{{ tasks_file }}#{{ module | lower }}-week{{ week_num }}-intro" optional/>
<p/>

{{ show_xp_steps(steps, tasks_file) }}

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
