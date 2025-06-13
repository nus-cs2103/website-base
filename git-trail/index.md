<frontmatter>
title: "Git Learning Trail"
pageNav: 4
</frontmatter>

{% from "common/topics.njk" import  panopto with context %}
{% from "common/macros.njk" import embed_topic with context %}
{% from "git-trail/common-fragement.md" import show_trail_unit, divider with context %}

<div class="website-content" id="main">

# :fas-route: ++Git Learning Trail++{.text-success}

<p class="lead"><md>This learning trail is for those who are new to Git and would like to learn it in advance to prepare for the course.<br>
These topics are covered during the [regular course schedule](../schedule/timeline.html) and in the [course textbook](../se-book-adapted/index.html) as well. So, <mark>doing this in advance is optional</mark>, but doing so can reduce your workload during the regular semester.</md></p>

<box>

**Note before you start:**

* **Watching the given videos is optional but recommended**. They cover almost the same ground as the text content, but provide a more visual view of the explanations. Watch if you can spare the time.
* **Doing the given activities is strongly recommended**. It is not enough to just go through the content -- you need to get some hands-on practice.
* **If you encounter any problems** while following this learning trial, you can post in the [course forum]({{ url_forum }}) (requires a Github account).
</box>

<span class="non-printable">

**Take a peek at the full picture(?)**. Optionally, if you are the sort who prefers to have some sense of the full picture before you get into the nitty-gritty details, watch the video in the panel below:
</span>

<panel header="%%{{ icon_resource }} Git Overview%%" class="non-printable">

@[youtube](v40b3ExbM0c)

</panel><p/>

<box>

**Tours:**

1. [Tour 1: Recording the History of a Folder](tour-recording-folder-history.md)
</box>

{{ show_trail_unit("gitAndGithub/ignore", "Git: `.ignore`", "47b7180e-9acb-4fc7-8ad7-ac0900a53544") }}

{{ divider("Phase 2: Using Revision History") }}

<p class="lead">In this phase, you'll learn how to make use of the revision history contained inside a Git repository.</p>

{{ show_trail_unit("revisionControl/usingHistory", "RCS: Using History") }}
{{ show_trail_unit("gitAndGithub/tag", "Git: `tag`", "9f40b219-58d7-4192-8ec8-ac0900a64410") }}
{{ show_trail_unit("gitAndGithub/diff", "Git: `diff`", "cccc7475-1bfa-4d88-8e2f-ac0900a8dbd2") }}
{{ show_trail_unit("gitAndGithub/checkout", "Git: `checkout`", "f16e2d7f-5f78-455c-830e-ac0900b7a747") }}
{{ show_trail_unit("gitAndGithub/stash", "Git: `stash`", "683017df-21c8-4890-8c42-ac0900c15bf4") }}

{{ divider("Phase 3: Working With Remote Repos") }}

<p class="lead">In this phase, you'll start interacting with git repositories hosted on remote servers.</p>

{{ show_trail_unit("revisionControl/remoteRepositories", "RCS: Remote Repositories", "d5c79357-9778-4cf7-8e5d-ac0900c337ae") }}
{{ show_trail_unit("gitAndGithub/clone", "Git: `clone`", "3bcdcf56-7456-46e3-a163-ac0900d28d6e") }}
{{ show_trail_unit("gitAndGithub/pull", "Git: `pull`", "3dbac71a-f450-47b6-8f4e-ac0900d765fe") }}
{{ show_trail_unit("gitAndGithub/fork", "Github: `fork`", "76879d62-2bb4-4951-a3d3-ac0900c68689") }}
{{ show_trail_unit("gitAndGithub/push", "Git: `push`", "897e2c87-2add-454c-8e2b-ac0900d8006f") }}

{{ divider("Phase 4: Working With Branches") }}

<p class="lead">In this phase, you'll learn how to use Git branches to track code changes done in parallel.</p>

{{ show_trail_unit("revisionControl/branching", "RCS: Branching", "c1688fb0-ff95-462c-a736-ac0e00c93e04") }}
{{ show_trail_unit("gitAndGithub/branch", "Git: `branch`, `merge`", "2580eb90-e6c1-42ab-9b5b-ac0e00c93de0") }}
{{ show_trail_unit("gitAndGithub/mergeConflicts", "Git: Merge Conflicts", "6de3f8b2-af7b-403a-a34f-ac0e00c97328") }}
{{ show_trail_unit("gitAndGithub/remoteBranches", "Git: Remote Branches") }}

</div>
