{% from "common/macros.njk" import embed_topic with context %}

{% macro show_main_text() %}
<div id="main">

<img src="{{baseUrl}}/admin/images/toolsList.png" style="width: 700px"><br>

#### <div class="text-white bg-dark p-1">Tools Used: Learning Management System</div>

This module website is the main source of information for the module. In addition, we use LumiNUS for some things %%(e.g., webcasts, announcements, file submissions, grade book, ...)%%.

<!-- ----------------------------------------------------------------------------------------------------- -->
<div id="github">

#### <div class="text-white bg-dark p-1">Tool Used: GitHub (for Code Hosting)</div>

You are ==_required to_ use GitHub== as the hosting and collaboration platform of your project (i.e., to hold the Code repository, Issue Tracker, etc.). 

<box>

<span style="color:purple">**:fas-hard-hat: Preparation**:</span>

Create a GitHub account (if you don't have one yet), as explained in the panel below.

{{ embed_topic("appendixE-gitHub.md#githubAccount", "Admin " + icon_embedding + " **Appendix E - GitHub: Creating an Account**", "-", "2") }}
</box>

**More info**: See [Appendix E - Using GitHub](appendixE-gitHub.html).

</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="rcs">

#### <div class="text-white bg-dark p-1">Tool Used: Git (for Revision Control)</div>

You are ==_required to_ use Git==. Other revision control software are not allowed. The recommended GUI client for Git is [SourceTree](https://www.sourcetreeapp.com/), but you may use any other, or none.

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

**Install Git and a Git GUI client** on your computer.<br>
  {{ icon_tip }} SourceTree comes with bundled with Git i.e., if you install SourceTree, you get both Git and a GUI client in one shot.

<div id="git-username">

**Set Git `user.name`**: We use various tools to analyze your code. For us to be able to identify your commits, we encourage you to ==set your Git `user.name` in all computers you use== to a sensible string that uniquely identify you. For example, ==you can to GitHub username or your full name as your Git username==. If this user name is not set properly or if you use multiple user names for Git, our tools might miss some of your work and as a result you might not get credit for some of your work.

After installing Git in a computer, you can set the Git username as follows:
1. Open a command window that can run Git commands (e.g., Git bash window)
2. Run the command `git config --global user.name YOUR_GITHUB_USERNAME`<br>
   e.g., `git config --global user.name JohnDoe`

More info about setting Git username is [here](https://help.github.com/articles/setting-your-username-in-git/).
</div>
</box>

</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="communication">

#### <div class="text-white bg-dark p-1">Tools Used: for Communication</div>

* **The preferred channels for module-related communications are**:
  * ==[github/nus-{{ module | lower }}-{{ semester }}/forum]({{module_org}}/forum/issues)== (not LumiNUS forum) -- suitable for longer-running conversations
  * our slack channel [{{slack_team}}]({{slack_team}}) -- suitable for quick chats 
* When communicating with instructors, prefer the two public channels given above. Use private channels (e.g., emails, private messages, face-to-face, private chat groups) only when the public channels are not suitable. %%Rationale: 1. More classmates can benefit from the discussions, 2. It is also safer because the prof can monitor information you receive for accuracy%%.
* You are encouraged to help others in the forum (e.g., share tips, help with technical problems). ==We consider such sharing when giving out `A+` grades and when recruiting tutors.==

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

We encourage you all to,
* ==join the slack channel== (you'll need to use an email address ending in `@nus.edu.sg`, `@comp.nus.edu.sg`, `@u.nus.edu.sg` or `@u.nus.edu` to join this channel).
* ==_watch_ [the forum]({{ forum_link }})== to get alerts when new issues/comments are posted ![image](https://user-images.githubusercontent.com/1673303/44647915-0c761a80-aa12-11e8-98ac-2deb50532643.png)
</box>

</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="ide">

#### <div class="text-white bg-dark p-1">Tool Used: Intellij IDE</div>

You are recommended to use [Intellij IDEA](https://www.jetbrains.com/idea/) for module-related programming work. While the use of Intellij is not compulsory, note that module materials are optimized for Intellij. Use other IDEs at your own risk. 

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>
* Install the IDE in your computer. You may use the Intellij community edition (free) or the ultimate edition (free for students).
</box>

</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="reposense">

#### <div class="text-white bg-dark p-1">Tool Used: RepoSense (for Analyzing Code Authorship)</div>

<include src="reposenseCompatibility.md" />
</div>

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("tools", show_main_text) }}