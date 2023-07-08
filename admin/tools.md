{% from "common/macros.njk" import embed_topic with context %}

{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tools") %}
<div id="main">

<pic src="{{baseUrl}}/admin/images/toolsList.png" style="width: 700px"></pic><br>

## Tool: Learning Management System

This course website is the main source of information for the course. In addition, we use Canvas for some things %%(e.g., announcements, file submissions, grade book, ...)%%.

<!-- ----------------------------------------------------------------------------------------------------- -->
{% if not cs2113 %}
## Tool: Zoom (for Lectures)

Install Zoom in your computer. Installation and login instructions are [here](https://wiki.nus.edu.sg/pages/viewpage.action?spaceKey=THES&title=Proctoring+with+Zoom). Remember to login using your NUSNET account.
{% endif %}
<!-- ----------------------------------------------------------------------------------------------------- -->
<div id="github">

## Tool: GitHub (for code hosting)

**You are _required to_ use GitHub** as the hosting and collaboration platform of your project (i.e., to hold the Code repository, Issue Tracker, etc.).

<box>

<span style="color:purple">**:fas-hard-hat: Preparation**:</span>

Create a GitHub account (if you don't have one yet), as explained in the panel below.

{{ embed_topic("appendixE-gitHub.md#githubAccount", "Admin " + icon_embedding + " **Appendix E - GitHub: Creating an Account**", "2") }}
</box>

**More info**: See [Appendix E - Using GitHub](appendixE-gitHub.html).

</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="rcs">

## Tool: Git (for revision control)

**You are _required to_ use Git.** The recommended GUI client for Git is [SourceTree](https://www.sourcetreeapp.com/), but you may use any other, or none.

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

**Install Git and a Git GUI client** on your computer.<br>
  {{ icon_tip }} SourceTree comes bundled with Git i.e., if you install SourceTree, you get both Git and a GUI client in one shot. If you are already comfortable using Git command line, you need not install/use a GUI client.

<div id="git-username">

**Set Git `user.name`**: We use various tools to analyze your code. For us to be able to identify your commits, we encourage you to ==set your Git `user.name` in all computers you use== to a sensible string that uniquely identifies you. For example, ==you can set it to your GitHub username or your full name==. If this user name is not set properly or if you use multiple usernames for Git, our grading scripts might miss some of your work.

After installing Git in a computer, you can set the Git username as follows:
1. Open a terminal that can run Git commands (e.g., a [Git Bash](https://www.atlassian.com/git/tutorials/git-bash) window, which comes with SourceTree)
2. Run the command `git config --global user.name YOUR_GITHUB_USERNAME`<br>
   e.g., `git config --global user.name JohnDoe`

More info about setting Git username is [here](https://help.github.com/articles/setting-your-username-in-git/).

<box type="warning" seamless>

**Caveat against using other Git GUIs**: While we do not _insist_ that you use SourceTree, note that we are unable  to provide any support if you run into any problems while using a different Git GUI.
</box>
</div>
</box>

</div><!-- ----------------------------------------------------------------------------------------------------- -->

<div tags="m--cs2113 m--tic2002" id="coursemology">

## Tool: Coursemology (for coding exercises)

* We'll be using Coursemology for coding exercises (compulsory).

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

* You'll receive the invitation to Coursemology sometime close to the first lecture.
* More information about Coursemology will be given in the first lecture.
</box>

</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="communication">

## Tools: for communication

##### :fas-comment: Forum %%(for longer-running discussions)%%
* **The preferred channels for course-related communication is the `forum` on GitHub** ==[{{url_forum}}]({{url_forum}})== (not the Canvas forum)
* When communicating with instructors, use the forum. Use private channels (e.g., emails, private messages, face-to-face, private chat groups) only when the forum is not suitable. %%Rationale: 1. More classmates can benefit from the discussions, 2. It is also safer because the prof{{ "s" if tic4001 }} can monitor information you receive for accuracy%%.
<div tags="m--cs2103 m--cs2113 m--tic4002">

* You are encouraged to help others in the forum (e.g., share tips, help with technical problems). ==We consider such sharing when giving out `A+` grades and when recruiting tutors.==
</div>

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

We encourage all to ==_watch_ [the forum]({{ url_forum }})== to get alerts when new issues/comments are posted ![image](https://user-images.githubusercontent.com/1673303/44647915-0c761a80-aa12-11e8-98ac-2deb50532643.png)
</box>

<div tags="m--cs2103 m--cs2113 m--tic4001 m--tic4002">

##### :fas-users-cog: MS Teams %%(for quick chats, in-lecture consultations)%%

* **Use MS Teams for short chats**.
* Install MST in your computer. Installation and login instructions are [here](https://wiki.nus.edu.sg/pages/viewpage.action?spaceKey=THES&title=Before+exams+-+Install+and+log+in+to+Microsoft+Teams). Remember to login using your NUSNET account.


<div tags="m--cs2103 m--cs2113">

* **MS Team for this class**: [{{ course_pair }}-{{ semester }}]({{ url_ms_teams_class }})
</div>
<div tags="m--tic4001 m--tic4002">

* for in-lecture consultations: [{{ course }}-{{ period }}]({{ url_ms_teams_class }})
</div>
</div>

</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="ide">

## Tool: Intellij IDE

You are recommended to use [Intellij IDEA](https://www.jetbrains.com/idea/) for course-related programming work. While the use of Intellij is not compulsory, note that course materials are optimized for Intellij.

<box type="warning" seamless>

Use other IDEs at your own risk. If you run into problems while using them, we won't be able to help you.
</box>

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>
* Install the IDE in your computer. You may use the Intellij community edition (free) or the ultimate edition (free for students).
* If you have an older version of the IDE, we recommend updating to the latest version.
</box>

</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="reposense">

## Tool: RepoSense (for authorship tracking)

<include src="tools-reposense-fragment.md" />
</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="teammates">

## Tool: TEAMMATES (for Peer Evaluations)

We use the [TEAMMATES](http://teammatesv4.appspot.com/) online peer evaluation system. %%TEAMMATES is a project run by NUS SoC students and used by over 0.6 million users from over 1000 universities.%%

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>
When the first feedback session is open on TEAMMATES, you will receive an eamil from TEAMMATES. There is nothing for you to do until then.

When you do receive that email, it will contain a unique link that you can use to access TEAMMATES without logging in first. Logging in to TEAMMATES using a Google account is optional (but doing so will allow you to see all your TEAMMATES sessions in one page).
</box>
</div>

</div>

{% endcall %}
