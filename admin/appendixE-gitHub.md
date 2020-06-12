{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("appendixE-gitHub") %}
<div id="main">

### <div class="text-white bg-dark p-1">Creating a GitHub Account</div>

<div id="githubAccount">

Create a personal GitHub account if you don't have one yet. 
1. You are advised to choose a sensible GitHub username as you are likely to use it for years to come in professional contexts. 
2. Strongly recommended: Complete your GitHub profile. In particular,  
   * Specify your full name. 
   * Upload a profile photo that matches <trigger trigger="click" for="modal:creatingGitHubAccount-photoCriteria">our requirements</trigger>.

   <panel type="seamless" header="%%Why am I being encouraged to complete my GitHub profile?%%" >

   The GitHub profile is useful for the tutors and classmates to identify you. If you are reluctant to share your info in your long-term GitHub account, you can remove those details after the module is over or create a separate GitHub account just for the module.

   </panel>
3. ==You are discouraged from changing your GitHub username during the semester/exam/grading period== as it can cause our auto-grading scripts to miss your GitHub activities. If you do change your GitHub username during that period, please let us know immediately.

<modal large header="Our requirements for the profile photo" id="modal:creatingGitHubAccount-photoCriteria">
  <include src="tp-deliverables-website.mbdf#profile-photo"/>
</modal>

</div>

### <div class="text-white bg-dark p-1">Guidelines for Reviewing PRs</div>

<div id="pr-review-guidelines">

<box type="success">

We expect the PR peer-review to be mutually beneficial to the reviewer and the author. i.e., you receive suggestions on how to improve your code, and get to learn alternative designs by reading others' code.
</box>

* If you are new to GitHub PRs, see [GitHub help on how to review PRs](https://help.github.com/en/articles/about-pull-request-reviews).
* Read the blog post [**10 tips for reviewing code you don’t like**](https://developers.redhat.com/blog/2019/07/08/10-tips-for-reviewing-code-you-dont-like/) - by David Lloyd (a Red Hat developer). In particular, follow the tip about phrasing objections as questions.
* Rather than give one overall comment for the entire PR, add specific comments at relevant places of the code.
* Feel free to ask for more info from the author, to help you understand the code/design. For example, you can ask why the author chose to write the code in a specific way.
* Feel free to compliment the author when appropriate %%e.g., _hey, I like how clean this bit of code is_ :+1:%%
* You can also suggest alternatives for the author to consider. Feel free to refer back to your own PR if you think a comparison would benefit the author. ==You are very welcome to offer to help the author with the project== (in your PR review, or outside of it) if you think the author needs such help i.e., as an informal mentor. Such mentoring will help both the author and you to become stronger programmers.
* You can use Markdown (specifically, [GitHub-Flavored Markdown](https://guides.github.com/features/mastering-markdown/)) in your comments.

**Guidelines for authors**:
* Don't get into arguments with reviewers. If you disagree with the reviewer, you can explain your own view in a non-confrontational way without trying to prove your way is better.
* Thank reviewers for their inputs.
</div>

<div id="organization-setup">

### <div class="text-white bg-dark p-1">Organization Setup</div>

{{ icon_important_big_red }} Please follow the organization/repo name format precisely because we use scripts to download your code or else our scripts will not be able to detect your work.

After receiving your team ID, one team member should do the following steps:
* Create a GitHub organization with the following details:
  * **Organization name** ==(all UPPER CASE) : `{{ semester }}-TEAM_ID`==. e.g.  `{{ semester }}-{{ module }}T-W12-1`, `{{ semester }}-{{ module }}-F09-3`
  * Plan:  Open Source ($0/month) 
  * This organization belongs to: My personal account
* Add members to the organization:
  * Create a team called `developers` to your organization.
  * Add your team members to the developers team.

</div>

<div id="repo-setup">

### <div class="text-white bg-dark p-1">Repo Setup</div>

Only one team member:

1. **Fork** [Address Book - Level 3 (AB3)]({{module_org}}/addressbook-level3) to your team org.
1. ==**Rename** the forked repo as `main`==. This repo (let's call it the _team repo_) is to be used as the repo for your project.
1. ==Ensure the issue tracker of your team repo is enabled.== %%Reason: our bots will be posting your weekly progress reports on the issue tracker of your team repo.%%
1. Ensure your team members have the desired level of access to your team repo.
1. [**Enable Travis CI for the team repo**]({{ ab3_website }}/UsingTravis.html#setting-up-travis-ci).
1. [**Set up _auto-publishing_ of docs**]({{ ab3_website }}/UsingTravis.html#enabling-auto-publishing-of-documentation). When set up correctly, your project website should be available via the URL  `https://{{ semester | lower }}-{team-id}.github.io/main` e.g., `https://{{ semester | lower }}-{{ module | lower }}-w13-1.github.io/main/`. This also requires you to [enable the _GitHub Pages_ feature of your team repo and configure it to serve the website from the `gh-pages` branch](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/#enabling-github-pages-to-publish-your-site-from-master-or-gh-pages).
1. **create a _team PR_** for us to track your project progress: i.e., create a PR from your ==team repo `master` branch== to [[nus-{{ module | lower }}-{{ semester }}/addressbook-level3]({{module_org}}/addressbook-level3)] `master` branch. PR name: `[Team ID] Product Name` e.g., `[CS2103T-T09-2] Contact List Pro`. %%As you merge code to your team repo's `master` branch, this PR will auto-update to reflect how much your team's product has progressed.%% In the PR description <tooltip content="use @githubUserName">@mention</tooltip> the other team members so that they get notified when the tutor adds comments to the PR.

All team members:

1. **Watch** the `main` repo (created above) i.e., go to the repo and click on the `watch` button to subscribe to activities of the repo
1. **Fork** the `main` repo to your personal GitHub account.
1. **Clone** the fork to your computer.
1. **Set up** the developer environment in your computer.<br>
   Recommended: Set it up as an Intellij project (follow the instructions in the Developer Guide carefully).

Note that some of our bot scripts depend on the following folder paths. Please do not alter those paths in your project.
* `/src/main`  
* `/src/test`  
* `/docs`

</div>

<div id="workflow">

### <div class="text-white bg-dark p-1">Workflow</div>

<div id="workflow-before-v11">

{{ icon_important_big_red }} **Read <trigger trigger="click" for="modal:appE-reusePolicy">our reuse policy %%(in Admin: Appendix B)%%</trigger>**, in particular, ==how to give credit when you reuse code from the Internet or classmates==:

<modal large header="Admin {{ icon_embedding }} Appendix E → Setting Git Username to Match GitHub Username" id="modal:appE-gitUsername">
  <include src="tools.md#git-username"/>
</modal>
<modal large header="Admin {{ icon_embedding }} Appendix B: Policies → Policy on Reuse" id="modal:appE-reusePolicy">
  <include src="appendixB-policies.md#policy-reuse"/>
</modal>


**Follow the <trigger trigger="click" for="modal:appErecommendedWorkflow-forkingworkflow">forking workflow</trigger> in your project up to v1.1.** In particular,

* **Create issues to represent project tasks** so that they can be tracked using the issue tracker features.
* **Create a PR when you implement a project task** that updates the code.<br>
  {{ icon_tip }} You can use GitHub's [_draft PRs_](https://github.blog/2019-02-14-introducing-draft-pull-requests/) feature to indicate that a PR is not yet ready for merging.<br>
  {{ icon_pro_tip }} `LGTM` is common abbreviation you can use in the review comments to mean `Looks Good To Merge`.
* **Get team members to review PRs.** A workflow without PR reviews is a risky workflow.
  * After [setting up Netlify]({{ ab3_website }}/UsingNetlify.html), you can use _Netlify PR Preview_ to preview changes to documentation files, if the PR contains updates to documentation. To see the preview, click on the `Details` link in front of the Netlify status reported (refer screenshot below).<br>
  <img src="{{ baseUrl }}/admin/images/gitHubPrStatus.png" width="700"/>
* **Do not merge PRs failing <tooltip content="Continuous Integration e.g., Travis">CI</tooltip>.** After [setting up Travis]({{ ab3_website }}/UsingTravis.html#setting-up-travis-ci), the CI status of a PR is reported at the bottom of the PR page. The screenshot below shows the status of a PR that is passing all CI checks.
  * **If there is a failure**, you can click on the `Details` link in corresponding line to find out more about the failure. Once you figure out the cause of the failure, push the a fix to the PR.<br>
  {{ icon_pro_tip }} You can use GitHub's [_protected branches_](https://help.github.com/en/articles/about-protected-branches) feature to prevent CI-failing PRs from being merged.
* After merging a PR, close the corresponding issue.<br>
  {{ icon_pro_tip }} You can use GitHub's [`Fixes #123` trick](https://help.github.com/en/articles/closing-issues-using-keywords) to get the issue to close automatically when the PR is merged.

<modal large header="TextBook {{ icon_embedding }}" id="modal:appErecommendedWorkflow-forkingworkflow">
  <include src="../book/revisionControl/forkingWorkflow/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

</div>
<div id="workflow-after-v11">

**After completing v1.1, you can reduce process rigor** to suit your team's pace. Here are some examples:

* **Reduce automated tests**: Automated tests have benefits, but they can be a pain to write/maintain; GUI tests are especially hard to maintain because their behavior can sometimes depend on things such as the OS, resolution etc.<br>
  It is OK to get rid of some of the troublesome tests and rely more on manual testing instead. The less automated tests you have, the higher the risk of regressions; but it may be an acceptable trade-off under the circumstances if tests are slowing you down too much.<br>
  There is no direct penalty for removing tests. Also note <trigger trigger="click" for="modal:appEworkflow-testingExpectations">our expectation on test code</trigger>.

* **Reduce automated checks**: You can also reduce the rigor of checkstyle checks to expedite PR processing.

* **Switch to a lighter workflow**: While _forking workflow_ is the safest, it is also rather heavy. You an switch to a simpler workflow if the forking workflow is slowing you down. Refer the textbook to find more about alternative workflows: _branching workflow_, _centralized workflow_. However, we still recommend that you use PR reviews, at least for PRs affecting others' features.

**You can also increase the rigor/safety of your workflow** in the following ways:

* Use GitHub's [_Protected Branches_](https://help.github.com/articles/about-protected-branches/) feature to protect your `master` branch against rogue PRs.

<modal header="Admin {{ icon_embedding }} Project Grading → Expectation on testing" id="modal:appEworkflow-testingExpectations">
  <include src="tp-expectations.md#testing-expectations"/>
</modal>
</div>


</div>

<div id="issue-tracker-setup">

### <div class="text-white bg-dark p-1">Issue Tracker Setup</div>

We recommend you configure the issue tracker of the `main` repo as follows:

* Delete existing labels and add the following labels.<br>
  {{ icon_tip }} **Issue type** labels are useful from the beginning of the project. The other labels are needed only when you start implementing the features.

<box>

**Issue type** labels:
* `type.Epic` : A big feature which can be broken down into smaller stories e.g. search
* `type.Story` : A user story
* `type.Enhancement`: An enhancement to an existing story
* `type.Task` (or `type.Chore`) : Something that needs to be done, but not a story, bug, or an epic. e.g. Move testing code into a new folder)
* `type.Bug` : A bug

</box>

<box>

**Status** labels:
* `status.Ongoing` : The issue is currently being worked on. note: remove this label before closing an issue.
</box>

<box>

**Priority** labels:
* `priority.High` : Must do
* `priority.Medium` : Nice to have
* `priority.Low` : Unlikely to do

</box>

<span id="bug-severity">

<box>

**Bug Severity** labels:
* `severity.VeryLow` : A flaw that is purely cosmetic and does not affect usage e.g., a typo/spacing/layout/color/font issues in the docs or the UI that doesn't affect usage.
* `severity.Low` : A flaw that is unlikely to affect normal operations of the product. Appears only in very rare situations and causes a minor inconvenience only.
* `severity.Medium` : A flaw that causes occasional inconvenience to some users but they can continue to use the product.
* `severity.High` : A flaw that affects most users and causes major problems for users. i.e., makes the product almost unusable for most users.

</box>

</span>

* Create following milestones : `v1.0`, `v1.1`, `v1.2`, `{{ penultimate_version }}`, `{{ final_version }}`,

* You may configure other project settings as you wish. e.g. more labels, more milestones

</div>

<div id="tp-schedule-tracking">

### <div class="text-white bg-dark p-1">Project Schedule Tracking</div>

In general, use the issue tracker (Milestones, Issues, PRs, Tags, Releases, and Labels) for assigning, scheduling, and tracking _all_ noteworthy project tasks, including user stories. Update the issue tracker regularly to reflect the current status of the project. You can also use GitHub's [Projects feature](https://www.youtube.com/watch?v=C6MGKHkNtxU) to manage the project, but keep it linked to the issue tracker as much as you can.

#### Using Issues:

<big>**During the initial stages**</big> (latest by the start of v1.2):

* **Record each of the user stories you plan to deliver as an issue in the issue tracker.** 
    %%e.g.%% `Title: As a user I can add a deadline`  
    `Description: ... so that I can keep track of my deadlines`

* **Assign the `type.*` and `priority.*` labels to those issues.**

* **Formalize the project plan** by assigning relevant issues to the corresponding milestone.

<big>**From milestone v1.2:**</big>

* **Define project tasks as issues**. When you start implementing a user story (or a feature), break it down to smaller tasks if necessary. Define reasonable sized, standalone tasks.  ==Create issues for each== of those tasks so that they can be tracked.%%e.g.%% 
  * A typical task should be able to done by one person, in a few hours.
    * %%{{ icon_dislike }} Bad (reasons: not a one-person task, not small enough): `Write the Developer Guide`%%
    * %%{{ icon_like }} Good: `Update class diagram in the Developer Guide for {{ final_version }}`%%

  * There is no need to break things into VERY small tasks. Keep them as big as possible, but they should be no bigger than what you are going to assign a single person to do within a week. %%eg.,%%
    * %%{{ icon_dislike }} Bad:`Implementing parser ` (reason: too big).%%
    * %%{{ icon_like }} Good:`Implementing parser support for adding of floating tasks`%%

  * Do not track things taken for granted. %%e.g., `push code to repo` should not be a task to track. In the example given under the previous point, it is taken for granted that the owner will also (a) test the code and (b) push to the repo when it is ready. Those two need not be tracked as separate tasks.%%

  * Write a descriptive title for the issue. %%e.g. `Add support for the 'undo' command to the parser`%%
    * Omit redundant details. In some cases, the issue title is enough to describe the task. In that case, no need to repeat it in the issue description. There is no need for well-crafted and detailed descriptions for tasks. A minimal description is enough. Similarly, labels such as `priority` can be omitted if you think they don't help you.<br><br>

* **Assign tasks (i.e., issues) to the corresponding team members using the `assignees` field.** ==Normally, there should be some ongoing tasks and some pending tasks against each team member at any point==.

* Optionally, you can use `status.ongoing` label to indicate issues currently ongoing.

<div id="using-milestones">

#### Using Milestones:

We recommend you do proper milestone management starting from v1.2. ==Given below are the conditions to satisfy for a milestone to be considered properly managed==:

**Planning a Milestone**:<br>

* **Issues assigned to the milestone, team members assigned to issues**: Used [GitHub milestones](https://help.github.com/articles/about-milestones/) to indicate which issues are to be handled for which milestone by assigning issues to suitable milestones. Also make sure those issues are assigned to team members. %%Note that you can change the milestone plan along the way as necessary.%%

* **Deadline set for the milestones** (in the GitHub milestone). %%Your internal milestones can be set earlier than the deadlines we have set, to give you a buffer.%%

**Wrapping up a Milestone**:<br>

  * **A working product tagged** with the correct tag (e.g. `v1.2`) and is pushed to the main repo<br>
    or a **product _release_ done on GitHub**. A product release is optional for v1.2 but required from from {{ penultimate_version }}. Click [here](https://github.com/se-edu/addressbook-level3/releases/) to see an example release.

  * **All tests passing** on Travis for the version tagged/released.

  * **Milestone updated to match the product** i.e. all issues completed and PRs merged for the milestone should be assigned to the milestone. Incomplete issues/PRs should be moved to a future milestone.<br>
    <img src="{{baseUrl}}/admin/images/assigningIssuesToMilestones.png" width="700"/>

  * **Milestone closed.**<br>
    <img src="{{baseUrl}}/admin/images/closingMilestones.png" width="700"/>

  * **If necessary, future milestones are revised** based on what you experienced in the current milestone %%e.g. if you could not finish all issues assigned to the current milestone, it is a sign that you overestimated how much you can do in a week, which means you might want to reduce the issues assigned to future milestones to match that observation%%.

</div>

</div>

</div>
{% endcall %}
