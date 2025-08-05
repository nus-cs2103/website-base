{% from "common/macros.njk" import embed_topic with context %}

{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tools") %}
<div id="main">

<pic eager src="{{baseUrl}}/admin/images/toolsList.png" style="width: 700px"></pic><br>

## Tool: Learning Management System

This course website is the main source of information for the course. In addition, we use Canvas for some things %%(e.g., announcements, file submissions, grade book, ...)%%.

<!-- ----------------------------------------------------------------------------------------------------- -->
{% if not cs2113 %}
## Tool: Zoom (for {{ lecture_name }}s)

Install Zoom on your computer. Installation and login instructions are [here](https://wiki.nus.edu.sg/pages/viewpage.action?spaceKey=THES&title=Proctoring+with+Zoom). Remember to login using your NUSNET account.
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

**You are _required to_ use Git.** Installing and configuring Git is covered in [this lesson]({{ baseUrl }}/book/gitAndGithub/gitPrep/index.html) of the [Git Learning Trail]({{ baseUrl }}/se-book-adapted/git-trail/index.html).

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

##### :fas-envelope: Course email %%(for course related queries, etc.)%%

* **Send all course-related emails to `{{ course | lower }}[at]comp.nus.edu.sg`**.{% if cs2103 %}<br>
  Even if your course code is `CS2103T`, the email to use is `cs2103@...` (i.e., not `cs2103t@...`).
{% endif %}

##### :fas-comment: Forum %%(for discussions, asking admin questions, seeking help, etc.)%%
* **The preferred channels for course-related communication is the `forum` on GitHub** ==[{{url_forum}}]({{url_forum}})== (not the Canvas forum)
* When communicating with instructors, use the forum. Use private channels (e.g., emails, private messages, face-to-face, private chat groups) only when the forum is not suitable. %%Rationale: 1. More classmates can benefit from the discussions, 2. It is also safer because the prof can monitor information you receive for accuracy%%.
<div tags="m--cs2103 m--cs2113">

* You are encouraged to help others in the forum (e.g., share tips, help with technical problems). ==We consider forum participation for grading (for [participation](participation.md)) and when recruiting tutors.==
</div>

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>

We encourage all to ==_watch_ [the forum]({{ url_forum }})== to get alerts when new issues/comments are posted ![image](https://user-images.githubusercontent.com/1673303/44647915-0c761a80-aa12-11e8-98ac-2deb50532643.png)
</box>

<div tags="m--cs2103 m--cs2113">

##### :fas-users-cog: MS Teams {% if cs2103 %}%%(for tutorials)%%{% endif %}

* **MS Teams is used in our tutorials**.<br>
  Install MST on your computer. Installation and login instructions are [here](https://wiki.nus.edu.sg/pages/viewpage.action?spaceKey=THES&title=Before+exams+-+Install+and+log+in+to+Microsoft+Teams). Remember to log in using your NUSNET account.


<div tags="m--cs2113">

* **MS Team for this class**: [{{ course_pair }}-{{ semester }}]({{ url_ms_teams_class }}) {% if cs2103 %}No need to send 'join requests'. We'll be mass-adding you to this around week 2.{% endif %}
</div>

<box type="wrong" light icon=":fas-exclamation:">

**#r#All admin questions and technical help requests** should be sent to the course email or posted in the forum##. Tutors are not allowed to respond to admin questions and technical help requests. See the panel below for more details.

{{ embed_topic("policies-fragment.md#policy-adminQuestions", "Admin " + icon_embedding + " Policies → **Policy on admin questions**", "1", indent=0) }}

</box>
</div>

</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="ide">

## Tool: The IDE

**[IntelliJ IDEA](https://www.jetbrains.com/idea/) is the recommended IDE** for course-related programming work. Using an IDE is strongly recommended but is not compulsory.

Our Intellij **IDEA resources can be found at [se-edu/guides](https://se-education.org/guides/)**.

<box type="warning" seamless>

**Use other IDEs at your own risk**, because,<br>
a) course materials are optimized for IntelliJ, and,<br>
b) we won't be able to help you if you run into problems while using any other IDE.

That said, we have also provided a good amount of **resources for VS Code at [se-edu/guides](https://se-education.org/guides/)**.
</box>

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>
* Install the IDE on your computer. You may use the IntelliJ community edition (free) or the ultimate edition (free for students).
* If you have an older version of the IDE, we recommend updating to the latest version.
</box>

</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="reposense">

## Tool: RepoSense (for authorship tracking)

<include src="tools-reposense-fragment.md" />
</div><!-- ----------------------------------------------------------------------------------------------------- -->
<div id="teammates">

## Tool: TEAMMATES (for Peer Evaluations)

We use the [TEAMMATES](http://teammatesv4.appspot.com/) online peer evaluation system. %%TEAMMATES is a project run by NUS SoC students and used by over a million users from over 1500 universities.%%

<box>

<span style="color:purple">**:fas-hard-hat: Preparation:**</span>
When the first feedback session is open on TEAMMATES, you will receive an email from TEAMMATES. There is nothing for you to do until then.

When you do receive that email, it will contain a unique link that you can use to access TEAMMATES without logging in first. Logging in to TEAMMATES using a Google account is optional (but doing so will allow you to see all your TEAMMATES sessions in one page).
</box>
</div>

</div><!-- ----------------------------------------------------------------------------------------------------- -->
{% if ((current_week | int) >= 7) %}<div id="watcher">

## Tool: WATcher (for monitoring tP work distribution)

You can use WATcher to see **a dashboard view of the tP work distribution** (e.g., number of issues/PRs done by each member). It can also help you **easily spot workflow oversights** (e.g., issues/PRs not assigned to a person/milestone).

**Steps to use:**

1. Go to the [tP teams list page](teamList.md). Locate your team, and click the #b#:fas-w:## icon for your team.
1. When prompted, choose to access `public repos only` and login using your GitHub account.<br>
   <pic src="images/WATcher-authorization.png" width="400" />
1. After the login is complete, you will be able to see the WATcher dashboard showing the `Currently active` milestone of your tP.<br>
   <pic src="images/WATcher-dashboard.png" width="800" /><br>
   This view shows issues/PRs relevant to the most recent/current milestone, each column showing issues/PRs assigned to a specific team member.<br>
   {{ icon_tip }} This view also helps you spot oversights. e.g., it indicates ongoing issues/PRs not assigned to any milestone as #r#:octicon-milestone: ???##.
1. You can switch the view from `Currently active` to `Contributions` to view all issues/PRs contributed by each member for the entire project.
1. The filters at the top of the dashboard can be used to tweak the view further.<br>
   {{ icon_tip }} The page URL changes to match the view, which means you can share/bookmark the current view using the current URL of your Browser.

<box type="warning" light>

WATcher is a tool created by past students, and #r#still in early preview state##.<br>
**Bugs/queries/suggestions**, please post in the [WATcher issue tracker](https://github.com/CATcher-org/WATcher/issues).
</box>
</div>{% endif %}<!-- ----------------------------------------------------------------------------------------------------- -->

</div>

{% endcall %}
