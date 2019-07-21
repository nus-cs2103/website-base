{% from "common/macros.njk" import embed_topic with context %}

{% macro show_main_text() %}
<div id="main">

<img src="{{baseUrl}}/admin/images/toolsList.png" style="width: 700px"><br>

#### Tools Used: Learning Management System

This module website is the main source of information for the module. In addition, we use LumiNUS for some things %%(e.g., webcasts, announcements, file submissions, grade book, ...)%%.

<hr><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="github">

#### Tool Used: GitHub (for Code Hosting)

You are ==_required to_ use GitHub== as the hosting and collaboration platform of your project (i.e., to hold the Code repository, Issue Tracker, etc.). 

**Preparation**: Create a GitHub account (if you don't have one yet), as explained in the panel below.

{{ embed_topic("appendixE-gitHub.md#githubAccount", "Admin " + icon_embedding + " **Appendix E - GitHub: Creating an Account**", "-", "2") }}

**More info**: See [Appendix E - Using GitHub](appendixE-gitHub.html).

</div><hr><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="communication">

#### Tools Used: for Communication

* **The preferred channels for module-related communications are**:
  * ==[github/nus-{{ module | lower }}-{{ semester }}/forum]({{module_org}}/forum/issues)== (not LumiNUS forum) -- suitable for longer-running conversations
  * in our slack channel [{{slack_team}}]({{slack_team}}) -- suitable for quick chats 
* When communicating with instructors, prefer the two public channels given above. Use private channels (e.g., emails, private messages, face-to-face, private chat groups) only when the public channels are not suitable. %%Rationale: 1. More classmates can benefit from the discussions, 2. It is also safer because the prof can monitor information you receive for accuracy.%%.
* You are encouraged to help others in the forum (e.g., share tips, help with technical problems). ==We consider such sharing when giving out `A+` grades and when recruiting tutors.==

**Preparation:** We encourage you all to,
* ==join the slack channel== (you'll need to use an email address ending in `@nus.edu.sg`, `@comp.nus.edu.sg`, `@u.nus.edu.sg` or `@u.nus.edu` to join this channel).
* ==_watch_ [the forum]({{ forum_link }})== to get alerts when new issues/comments are posted ![image](https://user-images.githubusercontent.com/1673303/44647915-0c761a80-aa12-11e8-98ac-2deb50532643.png)

</div><hr><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="ide">

#### Tool Used: Intellij IDE

You are recommended to use [Intellij IDEA](https://www.jetbrains.com/idea/) for module-related programming work. While the use of Intellij is not compulsory, note that module materials are optimized for Intellij. Use other IDEs at your own risk. 

**Preparation:**
* Install the IDE in your Computer. You may use the Intellij community edition (free) or the ultimate edition (free for students). 

</div><hr><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="rcs">

#### Tool Used: Git (for Revision Control)

You are ==_required to_ use Git==. Other revision control software are not allowed. The recommended GUI client for Git is [SourceTree](https://www.sourcetreeapp.com/), but you may use any other, or none.

**Preparation:**
* Install Git and a Git GUI client on your Computer.<br>
  {{ icon_tip }} SourceTree comes with bundled with Git i.e., if you install SourceTree, you get both Git and a GUI client in one shot.

</div><hr><!-- ----------------------------------------------------------------------------------------------------- -->

#### Tool Used: RepoSense (for Analyzing Code Authorship)

We use a custom-built tool called [RepoSense](https://github.com/reposense/RepoSense) for extracting code written by each person.

<div class="indented-level2">
<panel type="seamless" header="##### Using RepoSense">
  <include src="reposenseCompatibility.md#main" />
</panel>
</div>

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("tools", show_main_text) }}