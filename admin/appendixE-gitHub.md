{% macro show_main_text() %}
<div id="main">

## Creating a GitHub account

<div id="githubAccount">

Create a personal GitHub account if you don't have one yet. 
1. You are advised to choose a sensible GitHub username as you are likely to use it for years to come in professional contexts. 
2. Strongly recommended: Complete your GitHub profile. In particular,  
   * Specify your full name. 
   * Upload a suitable profile photo (i.e. a recent photo of your face). 

   <panel type="seamless" header="%%Why am I being pushed to complete my GitHub profile?%%" >
   
   The GitHub profile is useful for the tutors and classmates to identify you. If you are reluctant to share your info in your long-term GitHub account, you can remove those details after the module is over or create a separate GitHub account just for the module.
   
   </panel>
   <panel src="project-deliverables.md#profile-photo" header="Admin {{ icon_embedding }} Choosing a profile photo" minimized />
   
   </div>

<div id="git-username">

## Setting Git Username to Match GitHub Username

We use various tools to analyze your code. ==For us to be able to identify your commits, you should use the GitHub username as your Git username as well. If there is a mismatch, or if you use multiple user names for Git,== our tools might miss some of your work and as a result you might not get credit for some of your work.

In each Computer you use for coding, after installing Git, you should set the Git username as follows.

1. Open a command window that can run Git commands (e.g., Git bash window)
2. Run the command `git config --global user.name YOUR_GITHUB_USERNAME`<br>
   e.g., `git config --global user.name JohnDoe`
   
More info about setting Git username is [here](https://help.github.com/articles/setting-your-username-in-git/).

</div>
<div id="tutorial-pr-instructions">

## Submitting Pull Requests as evidence of an LO

1. Fork the repo to your personal GitHub account, if you haven't done so already.

2. Create a branch named after the LO ID e.g. `W2.2b`
    ==Remember to switch to master branch before creating the new branch.==
    
3. Commit your changes to that branch. Push to your fork.

4. Create a Pull Request against the `master` branch of the repo
   `{{module_org}}/{repo_name}`  
   e.g. `{{module_org}}/addressbook-level2`
   ==(do not create PRs against the upstream repo at `se-edu` org)== <br/> 
   <img src="{{baseUrl}}/admin/images/PrDetails.png" width="700" /><br/>
   PR name should be: `[LO_ID][TEAM_ID]Your Name`  
   e.g. If you are in tutorial W09 (i.e. Wednesday 9am) and team 1, `[W2.2b][W09-1]James Yong`.
   Your Team ID can be found in [this page]({{ team_IDs_page }}).
   Note that our tutorial IDs are different from those shown in CORS/IVLE. Our tutorial IDs are given in the panel below.

<div class="indented-level2">
{{ embed_topic("../admin/tutorials.md#tutorialTimetable", "Admin " + icon_embedding + " Tutorials → Tutorial Timetable", "apdxE-tutrialIds", "4") }}
</div>

5. Check the 'Files Changed' tab on GitHub to confirm the PR contains intended changes only.<br/> 
    ![](images/FilesChangedTab.png)
    
6. If the content of the PR is not as you expected, you can fix those problems in your local repo, commit, and push those new commits to the fork. The PR content will update automatically to match new commits. Alternatively, you can close that PR and create a new one with the correct content.
    
7. ==If your PR adapted/referred code from elsewhere== (e.g. a stackoverflow post or a classmate's PR -- which is allowed, even encouraged), acknowledge the source in your PR description text. e.g. `Some code adapted from #2431 (I followed the same technique for parsing user command)`

8. If the PR is not ready for review yet, add a comment `Work in progress`. When the PR is ready for review later, add a comment `Ready for review`  If there is no comment, we assume the PR is ready for review.

</div>

<div id="organization-setup">

## Organization setup

The instructions below are for setting up a GitHub organization for your team.

You can create your GitHub organization (for your team) after receiving your team ID. Here are the instructions (==please follow the organization/repo name format precisely because we use scripts to download your code. If the names are not as expected, our scripts will not work==):

* One team member (e.g. team leader) should create an organization with the following details:
* ==Organization name : `{{ module }}-{{ semester }}-TEAM_ID`==. e.g.  `{{ module }}-{{ semester }}-W12-1`
* Plan:  Open Source ($0/month) 
* After that, the same person can add members to the organization:
* Create a team called `developers` to your organization.
* Add your team members to the developers team.

</div>

<div id="repo-setup">

## Repo setup

Only one team member:

1. Fork [Address Book Level 4]({{module_org}}/addressbook-level4) to your team org.
1. ==Rename the forked repo as `main`==. This repo is to be used as the repo for your project.
1. Ensure your team members have the desired level of access to your team repo.

All team members:

1. Go to the `main` repo (created above) and click on the `watch` button to subscribe to activities of the repo
1. Fork the `main` repo to your personal GitHub account.
1. Clone the fork to your Computer.
1. Recommended: Set it up as an Intellij project (follow the instructions in the Developer Guide carefully).

Note that some of our download scripts depend on the following folder paths. Please do not alter those paths in your project. 
* `/src/main`  
* `/src/test`  
* `/docs`

</div>

<div id="issue-tracker-setup">

## Issue tracker setup

We recommend you configure the issue tracker of the `main` repo as follows:

* Delete existing labels and add the following labels.<br>
  :bulb: **Issue type** labels are useful from the beginning of the project. The other labels are needed only when you start implementing the features.

<tip-box>

**Issue type** labels:
* `type.Epic` : A big feature which can be broken down into smaller stories e.g. search
* `type.Story` : A user story
* `type.Enhancement`: An enhancement to an existing story
* `type.Task` : Something that needs to be done, but not a story, bug, or an epic. e.g. Move testing code into a new folder)
* `type.Bug` : A bug

</tip-box>

<tip-box>

**Status** labels:
* `status.Ongoing` : The issue is currently being worked on. note: remove this label before closing an issue.
</tip-box>

<tip-box>

**Priority** labels:
* `priority.High` : Must do
* `priority.Medium` : Nice to have
* `priority.Low` : Unlikely to do

</tip-box>

<span id="bug-severity">

<tip-box>

**Bug Severity** labels:
* `severity.Low` : A flaw that is unlikely to affect normal operations of the product. Appears only in very rare situations and causes a minor inconvenience only.
* `severity.Medium` : A flaw that causes occasional inconvenience to some users but they can continue to use the product.
* `severity.High` : A flaw that affects most users and causes major problems for users. i.e., makes the product almost unusable for most users.

</tip-box>

</span>

* Create following milestones : `v1.0`, `v1.1`, `v1.2`, `v1.3`, `v1.4`,

* You may configure other project settings as you wish. e.g. more labels, more milestones

</div>

<div id="project-schedule-tracking">

## Project Schedule Tracking

In general, use the issue tracker (Milestones, Issues, PRs, Tags, Releases, and Labels) for assigning, scheduling, and tracking _all_ noteworthy project tasks, including user stories. Update the issue tracker regularly to reflect the current status of the project. You can also use GitHub's new [Projects feature](https://www.youtube.com/watch?v=C6MGKHkNtxU) to manage the project, but keep it linked to the issue tracker as much as you can.

### Using Issues:

<big>**During the initial stages:**</big>

* **Record each of the user stories you plan to deliver as an issue in the issue tracker.** 
    %%e.g.%% `Title: As a user I can add a deadline`  
    `Description: ... so that I can keep track of my deadlines`

* **Assign the `type.*` and `priority.*` labels to those issues.**

<big>**From milestone v1.1:**</big>

* **When you start implementing a story, break it down to tasks.** Define reasonable sized, standalone tasks. A task should be able to done by one person, in a few hours. %%e.g.%%   
  * %%{{ icon_like }} Good: `Update class diagram in the project manual for v1.4`%%
  * %%{{ icon_dislike }} Bad (reasons: not a one-person task, not small enough): `Write the project manual`%%

* **Write a descriptive title for the issue.** %%e.g. Add support for the 'undo' command to the parser.%%

* **There is no need to break things into VERY small tasks.** Keep them as big as possible, but they should be no bigger than what you are going to assign a single person to do within a week. %%eg.,%%

  * `Implementing parser `  %%: too big because it cannot be done by a single person in a week.%% 
  * `Implementing parser support for adding of floating tasks` %%: appropriate size.%%
 
* **Do not track things taken for granted.** %%e.g., `push code to repo` should not be a task to track. In the example given under the previous point, it is taken for granted that the owner will also (a) test the code and (b) push to the repo when it is ready. Those two need not be tracked as separate tasks.%%

* **Omit redundant details.** In some cases, the summary/title is enough to describe the task. In that case, no need to repeat it in the description. There is no need for well-crafted and detailed descriptions for tasks. A minimal description is enough. Similarly, labels such as `priority` can be omitted if you think they don't help you.

* **Assign tasks to team members using the `assignees` field.** At any point, there should be some ongoing tasks and some pending tasks against each team member.

* **Optionally, you can use `status.ongoing` label to indicate issues currently ongoing.** 

<div id="using-milestones">

### Using Milestones:

We recommend you do the following from milestone v1.1:

* Use [GitHub milestones](https://help.github.com/articles/about-milestones/) to indicate which issues are to be handled for which milestone by assigning issues to suitable milestones.

* Set the deadlines for milestones (in GitHub). Your internal milestones can be set earlier than the deadlines we have set, to give you a buffer.

* Note that you can change the milestone plan along the way as necessary.

**Wrapping up a Milestone**:<br>
==Here are the conditions to satisfy for a milestone to be considered properly wrapped up==:
  * A working product tagged with the correct tag (e.g. v1.2) is pushed to the main repo.
  * All tests passing on Travis for the version tagged above.
  * Milestone updated to match the product i.e. all issues completed and PRs merged for the milestone should be assigned to the milestone.<br>
    <img src="{{baseUrl}}/admin/images/assigningIssuesToMilestones.png" width="700"/>
  * Milestone closed. If there are incomplete issues or unmerged PRs in the milestone, move them to a future milestone.<br>
    <img src="{{baseUrl}}/admin/images/closingMilestones.png" width="700"/>
  * Optionally, issues for the next milestone are assigned to team members (this is not compulsory to do _before_ the tutorial, but we recommend you to do it soon after the tutorial). 
    
  * Optionally, future milestones are revised based on what you experienced in the current milestone %%&nbsp;e.g. if you could not finish all issues assigned to the current milestone, it is a sign that you overestimated how much you can do in a week, which means you might want to reduce the issues assigned to future milestones to match that observation%%.
   
  * Doing a 'release' on GitHub is optional for v1.1 and v1.2 but compulsory from v1.3.  

</div>

</div>

<div id="workflow">

## Workflow

We recommend using the _Forking Workflow_.

<panel src="../book/gitAndGithub/forkingWorkflow/unit-inElsewhere-asFlat.md" boilerplate header="%%Textbook {{ icon_embedding }}%% Git and GitHub: Forking Workflow" />

</div>

</div>{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("appendixE-gitHub", show_main_text) }}
