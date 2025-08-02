{% from "common/macros.njk" import button, embed_topic, show_as_tab, show_as_rounded_tab, show_faq, step, thumb, thumb_small, timing_badge with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("appendixE-gitHub") %}
<div id="main">

## Creating a GitHub Account

<div id="githubAccount">

Create a personal GitHub account if you don't have one yet.
1. Choose a sensible GitHub username as you are likely to use it for years to come in professional contexts e.g., in job applications.
2. Recommended (but not required): Complete your GitHub profile. In particular,
   * Specify your name.
   * Upload a profile photo that matches <trigger trigger="click" for="modal:creatingGitHubAccount-photoCriteria">our requirements</trigger>.

   <panel type="seamless" header="%%Why am I being encouraged to complete my GitHub profile?%%" >

   The GitHub profile is useful for the tutors and classmates to identify you. If you are reluctant to share your info in your long-term GitHub account, you can remove those details after the course is over or create a separate GitHub account just for the course.

   </panel>
3. ==Please do not change your GitHub username during the semester/exam/grading period== as it can cause our auto-grading scripts to miss your GitHub activities. If you change your GitHub username during that period due to an unavoidable reason, please let us know immediately.

<modal large header="Our requirements for the profile photo" id="modal:creatingGitHubAccount-photoCriteria">
<include src="tp-deliverables-website-fragment.md#profile-photo"/>
</modal>

</div>

<!-- ==================================================================================================== -->

## Guidelines for Reviewing PRs

<div id="pr-review-guidelines">

Follow the [_Best practices for reviewing PRs_ @SE-EDU/guides](https://se-education.org/guides/guidelines/PRs-reviewing.html). You are ==expected to follow all of them==.

</div>

<!-- ==================================================================================================== -->

<div id="organization-setup">

## tP Team Organization Setup


<box type="important" seamless>

Please follow the organization/repo name format precisely or else our grading scripts will not be able to detect your work.

</box>

****({{ icon_individual }}/%%{{ icon_team }}%%) Only one team member:****

After receiving your team ID, one team member should do the following steps:
* Create a GitHub organization with the following details:
  * **Organization name** ==(all UPPER CASE) :`{{ semester }}-TEAM_ID`==. e.g., {% if has_t %}`{{ semester }}-{{ course }}T-W12-1`,{% endif %} `{{ semester }}-{{ example_team_id }}`
  * Plan: Open Source ($0/month)
  * This organization belongs to: My personal account
* Add members to the organization:
  * Create a team called`developers`to your organization.
  * Add your team members to the developers team.

</div>

<!-- ==================================================================================================== -->

<div id="tp-team-repo-setup">

## tP Team Repo Setup

****({{ icon_individual }}/%%{{ icon_team }}%%) Only one team member:****

<box tags="m--cs2113" seamless type="important">

The tP project template given to you is a variation of the iP repo you used for the iP, but ==with some important differences==. Please follow instructions carefully, rather than follow what you remember from the iP.

</box>

1. **Fork** the [{{url_course_org}}/{{ tp_repo_name }}]({{url_course_org}}/{{ tp_repo_name }}) repo to your team org.
   * This repo (let's call it the _team repo_) is to be used as the repo for your project.
   * <span id="do-not-rename">{{ icon_important_big_red }} Please do not rename the fork %%Reason: our grading scripts rely on the repo name.%%</span>
1. **Enable the issue tracker**.
1. **Enable GitHub Actions**: Go to the {{ show_as_rounded_tab(':fas-play-circle: Actions') }} tab and enable workflows by clicking the {{ button('Enable actions', button_style="success") }} button (or the {{ button('I understand ... enable them', button_style="success") }} button). That will enable the GitHub Actions that are already included in the repo you forked.{% if cs2103 %}<br>
   **Set up codecov**, as explained in the [DevOps guide]({{ url_ab3_fork_website }}/DevOps.html).{% endif %}
{% if cs2103 %}
1. **Set up the project website**<br>
   There are two options for the project website: [Jekyll](https://jekyllrb.com/), [MarkBind](https://markbind.org). You can choose either one. More info are given in the panels below:

<div class="indented-level2">

<panel header="##### Jekyll" expanded>

**Pros:**
* Widely used (one of the most popular static site generator tools)
* Built-in support by GitHub

**Cons:**
* More optimized for blogs (but can be used for normal websites as well)
* Local installation is more troublesome (requires Ruby)

Example AB3 website using Jekyll: [here](https://se-education.org/addressbook-level3/)

**How to set up:** Follow instructions in the [_Documentation guide_ page]({{ url_ab3_fork_website }}/Documentation.html) of AB3 developer guide.
</panel>

<panel header="##### MarkBind" expanded>

**Pros:**
* Optimized for creating course/project websites -- also used by CS2103/T website<br>
  e.g., Built-in support for PlantUML, and many other features useful for project documentation
* Easier to set up locally (and JavaScript based, rather than Ruby)

**Cons:**
* Home-grown, small user base

Example AB3 website using MarkBind: [here](https://damithc.github.io/ab3-markbind/)

**How to set up:**
1. Merge the given `switch-docs-to-markbind` branch to the `master` branch.
1. After that, follow instructions in the [this se-edu/guide](https://se-education.org/guides/tutorials/markbind-forked-sites.html).
</panel>
<p/>

{{ icon_tip }} When set up correctly, your project website should be available via the URL  `https://{{ semester | lower }}-{team-id}.github.io/{{ tp_repo_name }}`<br>
 e.g., `https://{{ semester | lower }}-{{ course | lower }}-w13-1.github.io/{{ tp_repo_name }}`.
</div>
{% elseif course == "CS2113"%}
1. **Enable GitHub Pages**: Go to the {{ show_as_rounded_tab(':octicon-gear: Settings') }} tab and enable `GitHub Pages` for the `master branch /docs folder` (similar to how you did it in the iP).<br>
   Update the `README.md` file to change the title from "Duke project template" to your product name. Commit and push to the master branch. <br>
   After a few minutes, confirm your tP website is available in the corresponding `github.io` URL.
{% endif %}
5. **Add members**. Ensure your team members have the desired level of access to your team repo.<br>
   Recommended: Give _admin access_ to 1-2 members and _write access_ to others.
1. **Create a _team PR_** for us to track your project progress: i.e., create a PR from your ==team repo `master` branch== to [[nus-{{ course | lower }}-{{ semester }}/{{ tp_repo_name }}]({{url_course_org}}/{{ tp_repo_name }})] `master` branch. PR name: `[Team ID] Product Name` e.g., `[{{ example_team_id }}] InsureList`. %%As you merge code to your team repo's `master` branch, this PR will auto-update to reflect how much your team's product has progressed.%%<br>
   Please fill in these details as specified because they are used by our grading scripts.
   * **PR subject: the name of your product** e.g., `[{{ example_team_id }}] InsureList`
   * **Description: a 1-2 sentence overview** (plain text only, no formatting or links) of your project indicating the target user and the value proposition e.g., `InsureList helps insurance agents manage detail of their clients. It is optimized for CLI users so that frequent tasks can be done faster by typing in commands.`
1. [Optional, recommended] **Protect the `master` branch**: Use GitHub's [_Protected Branches_](https://help.github.com/articles/about-protected-branches/) feature to protect your `master` branch against rogue PRs. We suggest the following:
   * Go to the {{ show_as_rounded_tab(':octicon-gear: settings') }} of your team repo.{ texts="['i.', 'ii.', 'iii.']" }
   * Click on the `Branches` option on the navigation menu on the left.
   * Click the {{ button('**Add rule**') }} button. In the _Branch protection rule_ page,
     * Specify the _Branch name pattern_ to be `master`
     * Tick the option `Require status checks to pass before merging` to ensure that a branch has to pass CI before it can be merged into the `master` branch
     * If you think all PRs should be reviewed by someone other than the PR author before they are merged, also tick the `Require pull request reviews before merging` option.

</div>
<!-- ==================================================================================================== -->

<div id="issue-tracker-setup">

## tP Issue Tracker Setup

We recommend you configure the issue tracker of the tP team repo as follows:

1. **Delete existing labels**
1. **Add the following labels.**<br>
  {{ icon_tip }} **Issue type** labels are useful from the beginning of the project. The other labels are needed only when you start implementing the features.

<div class="indented-level1">
<box>

**Issue type** labels:
* `type.Epic`: A big feature which can be broken down into smaller stories e.g., search
* `type.Story`: A user story
* `type.Enhancement`: An enhancement to an existing story
* `type.Task` (or `type.Chore`): Something that needs to be done, but not a story, bug, or an epic. %%e.g., Move testing code into a new folder%%
* `type.Bug`: A bug

</box>
<box>

**Priority** labels:
* `priority.High`: Must do
* `priority.Medium`: Nice to have
* `priority.Low`:Unlikely to do

</box>
<div id="bug-severity">
<box>

**Bug Severity** labels:
* `severity.VeryLow` : A flaw that is purely cosmetic and does not affect usage e.g., a typo/spacing/layout/color/font issues in the docs or the UI that doesn't affect usage.
  ==Only cosmetic problems should have this label==.
* `severity.Low` : A flaw that is unlikely to affect normal operations of the product. Appears only in very rare situations and causes a minor inconvenience only.
* `severity.Medium` : A flaw that causes occasional inconvenience to some users, but they can continue to use the product.
* `severity.High` : A flaw that affects most users and causes major problems for users. i.e., only problems that make the product ==almost unusable for most users== should have this label.

{{ icon_info }} When applying for documentation bugs, replace _user_ with _reader_.

</box>
</div>
</div>

3. **Create following milestones** : {% if cs2103 %}`{{ version_practice }}`{% endif %} {% if cs2103 %}`{{ version_first }}`{% endif %} `{{ version_mvp }}` {% if cs2103 %}`{{ version_alpha }}`{% endif %} `{{ version_penultimate }}` `{{ version_final }}`

4. You may configure other project settings as you wish. e.g., more labels, more milestones

</div>

<!-- ==================================================================================================== -->
<div id="tp-individual-fork-setup">

## tP Individual Fork Setup

****({{ icon_individual }}, {{ icon_individual }}, {{ icon_individual }}, ...) Every team member:****

1. **Watch** the `{{ tp_repo_name }}` team repo (created earlier) i.e., go to the repo and click on the {{ button(':octicon-eye: Watch :octicon-triangle-down:') }} button to subscribe to activities of the repo.
1. **Fork** the `{{ tp_repo_name }}` team repo to your personal GitHub account.<br>
   <include src="appendixE-gitHub.md#do-not-rename" inline />
1. **Clone** the fork to your computer.
1. **Set up** the developer environment on your computer by following the
   <span tags="m--cs2103">[_Setting up and getting started_ page]({{ url_ab3_fork_website }}/SettingUp.html) of AB3 developer guide.</span><span tags="m--cs2113">the [README]({{url_course_org}}/{{ tp_repo_name }}) carefully as the ==steps are different from the iP==.</span>

<box type="wrong" seamless>

**Do not alter these paths** in your project as our grading scripts depend on them.
* `src/main/java`
* `src/test/java`
* `docs`
</box>

</div>

<!-- ==================================================================================================== -->

<div id="tp-schedule-tracking">
<div id="tp-schedule-tracking-overview">

## tP Project Schedule Tracking

**For tP schedule tracking, our strategy is to leverage tools already available in the GitHub platform**, rather than bring in an entirely separate tool for it. Given below is a summary of the most basic needs related to this aspect, and which GitHub tool is used for each.

Tracking need | GitHub tool used
-----|------------
{{ thumb_small("a", thumb_style="primary") }} **WHAT** needs to be done? i.e., project tasks | Tasks are posted as **issues** in the GitHub issue tracker.
{{ thumb_small("b", thumb_style="primary") }} **WHO** should do which task? i.e., tasks assignment | Issues are given **assignees**.
{{ thumb_small("c", thumb_style="primary") }} **WHEN** is a task to be done? i.e., task scheduling | Issues are assigned to a GitHub **milestones**, which in turn has a **deadline**.
{{ thumb_small("d", thumb_style="primary") }} **HOW** is a task progressing? | **PRs** are created to match tasks in progress.<br>**Merging** the PR (and closing of the matching issue) indicates task completion.
{{ thumb_small("e", thumb_style="primary") }} **HOW** is an iteration progressing? | A GitHub **milestone** is used to track an iteration.<br>A GitHub **release** represents the iteration deliverables.<br>Closing the milestone indicates the completion of the iteration.

<box type="tip" seamless>

[Optional] **You can also use GitHub's [Projects feature](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects)** (which works like a layer on top of GitHub issues/PRs) to manage the project. If you do, keep it linked to the issue tracker as much as you can.
</box>
</div>
The sections below describe a-e in more details.
<!-- ------------------------------------------------------------------------------------------------------ -->

<div id="tp-schedule-tracking-issues">

#### {{ thumb("a", thumb_style="primary") }} Using issues to track project tasks

* **Define project tasks as issues**. When you start implementing a feature/fix/enhancement etc., break it down to smaller tasks if necessary. Define reasonably sized, standalone tasks.  ==Create issues for each== of those tasks so that they can be tracked.
  * A typical task should be small enough for one person to do in a few hours. %%eg.,%%
    * %%{{ bad }}: `Write the Developer Guide` (reasons: not a one-person task, not small enough)%%
    * %%{{ good }}: `Implement parser support for adding events`%%
* **Ensure the issue details are 'good enough'**:
  * **Write a descriptive title** for the issue.
    * %%{{ bad }}: `Update parser`(reason: not specific enough)%%
    * %%{{ good }}: `Add support for the 'undo' command to the parser`%%
  * **Assign the `type.*` and `priority.*` labels**, if applicable.
  * **Omit redundant details.**
    * There is no need for well-crafted and detailed descriptions for tasks. A minimal description is enough.
    * If the issue title is enough to describe the task, no need to repeat it in the issue description.
    * Similarly, labels such as `priority` can be omitted if you think they don't help you.
* **No need to track things taken for granted.** %%e.g., `push code to repo` (reason: it is taken for granted that the code author will push the code to the repo).%%
* **Ensure issues are compliant with the breadth-first iterative approach.** That is, ==a code merge to the `master` branch should take the product from one working version to another (slightly better) working version==.
  * %%{{ bad }}: `Add all data classes` (reason: this is the depth-first approach)%%
  * %%{{ good }}: `Support adding simple todo tasks`%%

<box type="info" icon=":fas-circle-info:" light>

****Using issues to track user stories****{.text-info}

In our project, we use _user stories_ to track user requirements. Instead of using a separate tool for tracking requirements, we can use the GitHub issue tracker for this as well. To do that, record each user story as an issue in the issue tracker. More details (taken from the textbook) are given below. {% if cs2103 %}**It is optional to use the GitHub issue tracker for recording user stories.**{% endif %}

----

<include src="..\book\specifyingRequirements\userStories\usage\tools.md#user-stories-in-issue-tracker" />

</box>

{{ show_faq("githubWhoCreatesIssues") }}
{{ show_faq("githubIssuesForNonCodingTasks") }}
{{ show_faq("githubIssuesSubTasks") }}

</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="tp-schedule-tracking-assignees">

#### {{ thumb("b", thumb_style="primary") }} Using issue assignees to track task allocation

* **Assign the issue to a team member** after you've decided who should do the corresponding task.

{{ show_faq("githubMultipleIssueAssignees") }}
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="tp-schedule-tracking-milestones-when">

#### {{ thumb("c", thumb_style="primary") }} Using milestones for task scheduling

* **Create [GitHub milestones](https://docs.github.com/en/issues/using-labels-and-milestones-to-track-work/about-milestones)**, to represent upcoming iterations of your project.

* **Allocate the issues (and corresponding PRs) to a milestone**, to indicate which tasks will be done in that milestone. As milestones have deadlines, this also indicates _when_ those tasks will be done.

</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="tp-schedule-tracking-prs">

#### {{ thumb("d", thumb_style="primary") }} Using PRs to track task progress

<div id="tp-schedule-tracking-prs-creating">

****Creating PRs****:

* **Create a PR when you implement a project task** that updates the code.
  * Use the <trigger trigger="click" for="modal:appErecommendedWorkflow-forkingworkflow">forking workflow</trigger> when creating PRs in early iterations %%(you can switch to the <trigger trigger="click" for="modal:appErecommendedWorkflow-featurebranchworkflow">feature branch workflow</trigger> after completing {{ version_mvp }} if you wish)%%.<br>
  =={{ icon_alert }} This means each PR should come from a _separate branch_ (i.e., not the `master` branch) of your _own fork_ (not the team repo), as that is an essential part of the forking workflow.==
  * Suggestion: Make the PR title same as the title of the corresponding issue (for easier matching between PRs and issues).
  * {{ icon_tip }} You can use GitHub's [_draft PRs_](https://github.blog/2019-02-14-introducing-draft-pull-requests/) feature to indicate that a PR is not yet ready for merging.
  * {{ icon_tip }} You can use GitHub's [`Fixes #123` trick](https://help.github.com/en/articles/closing-issues-using-keywords) to get the issue to close automatically when the PR is merged.
* **Assign the PR to a milestone.** This allows the PR to become visible under the milestone progress.<br>
  There is no need to assign the PR to a person. The PR author is considered as the owner of the PR.
* **While waiting for one PR to be merged, you can send more PRs.** If you do, remember to use a separate branch for each PR, and try to reduce overlaps between parallel PRs %%(so that each can be reviewed/merged independently of the others)%%.

{{ show_faq("githubIssueForEachPr") }}

<modal large header="TextBook {{ icon_embedding }}" id="modal:appErecommendedWorkflow-forkingworkflow">
  <include src="../book/gitAndGithub/forkingWorkflow/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

<modal large header="TextBook {{ icon_embedding }}" id="modal:appErecommendedWorkflow-featurebranchworkflow">
  <include src="../book/gitAndGithub/featureBranchFlow/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

</div>
<div id="tp-schedule-tracking-prs-reviewing">

****Reviewing PRs****:

* **Get team members to review PRs**, to reduce the risk of problematic code, but also, to practice the important skill of reviewing code.
  * **You can [request review](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review)** from specific team members, to expedite the PR progress.
* **When reviewing others' PRs**:
  * **Follow the** [_**Best practices** for reviewing PRs_ @SE-EDU/guides](https://se-education.org/guides/guidelines/PRs-reviewing.html).
  * **Give comments at specific locations** of the code changes, in addition to adding an overall comment for the entire PR. Reason: location-specific comments are valued more in grading.
  * {{ icon_tip }} `LGTM` is common abbreviation you can use in the review comments to mean `Looks Good To Me`.

</div>
<div id="tp-schedule-tracking-prs-merging">

****Merging PRs****:

* **Do not merge PRs failing <tooltip content="Continuous Integration e.g., GitHub Actions">CI</tooltip>.** The CI status of a PR is reported at the bottom of the {{ show_as_rounded_tab(":octicon-comment-discussion: conversation")}} tab of the PR page. Here's an example:<br>
  ![](images/gitHubPrStatus.png)
  * **If there is a failure**, you can click on the `Details` link in corresponding line to find out more about the failure. Once you figure out the cause of the failure, push a fix to the PR.
  * An exception to this guideline is when the failure is confirmed to be due to something you can afford to ignore %%e.g., when CI fails due to a drop in code coverage but the code section that is causing the coverage drop is not practical to be covered by automated tests, or you plan to write the relevant tests at a later time%%.
* **Avoid rebasing/squashing** when merging PRs. While both are good alternatives to the default behavior of creating a merge commit, rebasing/squashing can affect the timestamp of the commits, which can interfere with the progress tracking that we do for grading purposes %%i.e., the commits can get detected under a week different from the week they were actually done%%.
* **After merging a PR**,
  * **close the corresponding issue** (which should happen automatically, if you followed [this trick](https://help.github.com/en/articles/closing-issues-using-keywords)).
  * **sync your individual repos/forks with the team repo** as follows:
    * Pull the latest `master` from the team repo, and push it to your own fork.
    * If there are any unmerged branches in your local repo, for each of them,<br>
      merge `master` branch to it, and push the updated branch to your fork.<br>
      %%{{ icon_info }} Another way to sync a branch with the `master` branch is to rebase it. But we discourage that approach as it will change the timestamp of your branch commits, affecting how our grading scripts track your work.%%
  * <span class="text-danger">**don't delete the branch used by the PR**.</span> While it is common practice to delete a branch after merging it, we require you to keep those branches in the team repo so that our scripts can confirm that you used branches when adding changes.
{% if course == "CS2113" %}
* **As you add functionality, update the `input.txt` and `EXPECTED.txt` as well** so that the functionality you add gets regression tested automatically every time the code is updated from that point onwards.
{% endif %}

{{ show_faq("githubWhoMergesPrs") }}
</div>
</div>
<!-- ------------------------------------------------------------------------------------------------------ -->
<div id="tp-schedule-tracking-milestones-progress">

#### {{ thumb("e", thumb_style="primary") }} Using milestones to track iteration progress

****At the start of the iteration:****

* **Create milestones to represent the iteration.** For example, if your next iteration will produce the version `{{ version_first }}` of the product, we can create a milestone named `v1.1` %%(for convenience, we use the product version as the milestone name as well)%%.
* **Set a deadline** for the milestone. %%This can be earlier than the deadlines set by the course, to give you a buffer.%%
* **Create issues** for tasks to be done in that iteration.<br>
  **Assign them to team members.**<br>
  **Assign them to the milestone.**


****During the iteration****:

<pic eager src="{{baseUrl}}/admin/images/assigningIssuesToMilestones.png" width="700"/>

* **Ensure incoming PRs are assigned to the milestone** as well.<br>
  **Review and merge PRs**, and ensure the corresponding issue is closed when the PR is merged.
* **Adjust iteration targets as necessary**, by assigning new issues/PR to the milestone, or removing them from the milestone.


****At the end of the iteration****:

<pic eager src="{{baseUrl}}/admin/images/closingMilestones.png" width="700"/>

* **Update the milestone to match the product** i.e., all issues completed and PRs merged for the milestone should be assigned to the milestone. Incomplete issues/PRs should be moved to a future milestone.
* **Do a release** ([example](https://github.com/se-edu/addressbook-level3/releases/)), if required by the milestone.
* **Close the milestone.**

</div>
</div>

<!-- ------------------------------------------------------------------------------------------------------ -->

</div>
{% endcall %}
