{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<p class="lead" style="color: purple"><md>{{ far_calendar_check }} <include src="project-timeline.md#v14-overview" inline /></md></p>

**Summary of submissions**:

Team/Individual Item | Name format | Upload to
-------------------- | ----------- | ---------
{{ icon_team }} Source code |  tag as `v1.4` | GitHub
{{ icon_team }} Jar file |  `[team][product name].jar`<br>%%e.g. [W09-1][ContactsPlus].jar%% | IVLE
{{ icon_team }} User Guide | `[TEAM_ID][product Name]UserGuide.pdf`<br>  %%e.g.[W09-1][Contacts Plus]UserGuide.pdf%% | IVLE
{{ icon_team }} Developer Guide | `[TEAM_ID][product Name]DeveloperGuide.pdf`<br> %%e.g. [W09-1][Contacts Plus]DeveloperGuide.pdf%% | IVLE
{{ icon_team }} Product Website | `README` page, `Ui.png`, `AboutUs` page | github.io
{{ icon_individual }} Project Portfolio Page | `[TEAM_ID][Your Name]Portfolio.pdf`<br> %%e.g.[W09-1][John Doe]Portfolio.pdf%%<br>html version of PPP page on the product website | IVLE<br><br>github.io

**Deadline** for all v1.4 submissions is Week 13 Monday 23.59 unless stated otherwise.

* {{ icon_important_big_red }} **Penalty for late submission:** ==-1 mark for each hour delayed, up to 3 hours.== Even a one-second delay is considered late, irrespective of the reason. Penalty for delays beyond 3 hours are determined on a case by case basis.
  * For submissions done via IVLE, the submission time is the timestamp shown by IVLE.
  * When determining the late submission penalty, **we take the latest submission** even if the same exact file was submitted earlier. Do not submit the same file multiple times if you want to avoid unnecessary late submission penalties.
* The whole team is penalized for problems in team submissions. Only the respective student is penalized for problems in individual submissions. 
* {{ icon_important_big_red }} Please **follow submission instructions closely**. ==Any non-compliance will be penalized==. e.g. wrong file name, team member photos not suitable, etc.
* For pdf submissions, ensure the file is usable and hyperlinks in the file are correct. Problems in documents are considered bugs too %%&nbsp;e.g. broken links, outdated diagrams/instructions etc.%%.
* **Do not update the repo during the 14 days after the deadline.** Get our permission first if you need to update the repo during that _freeze_ period. You can continue to evolve your repo after that.

**Grading**:

<span class="flat">Described in [[Admin: Project: Assessment](#admin-project-assessment-anchor)]</span>

<panel src="project-assessment.md#main" header="%%Admin {{ icon_embedding }} Project: Assessment%%" class="embedding" />


### v1.4 Product

{{ embed_topic("project-deliverables.md#project-deliverables-executable", "Admin " + icon_embedding + " Project → Deliverables → Executable", "v14-executable", "3") }}
<p/>

**Submission**: See summary of submissions above


### v1.4 Source Code

{{ embed_topic("project-deliverables.md#project-deliverables-sourcecode", "Admin " + icon_embedding + " Project → Deliverables → Source Code", "v14-sourcecode", "3") }}
<p/>

**Submission**: Push the code to GitHub and tag with the version number. Source code (==please ensure the code reported by RepoSense as yours is correct;== any updates to RepoSense config files or `@@author` annotations after the deadline will be considered a later submission). Note that the quality of the code attributed to you accounts for a significant component of your final score, graded individually.


### v1.4 User Guide

{{ embed_topic("project-deliverables.md#project-deliverables-ug", "Admin " + icon_embedding + " Project → Deliverables → User Guide", "v14-deliverableUg", "3") }}
<p/>

**Submission**: Convert the pdf (AB4 dev guide has some instructions on converting project docs to pdf) and upload to IVLE. See _summary of submissions_ above for the file name format.


### v1.4 Developer Guide

{{ embed_topic("project-deliverables.md#project-deliverables-dg", "Admin " + icon_embedding + " Project → Deliverables → Developer Guide", "v14-deliverableDg", "3") }}
<p/>

**Submission**: Similar to UG

### v1.4 Project Portfolio Page (PPP)

{{ embed_topic("project-deliverables.md#project-deliverables-ppp", "Admin " + icon_embedding + " Project → Deliverables → Project Portfolio Page", "v14-deliverablePpp", "3") }}
<p/>

**Submission**: Similar to UG


### v1.4 Product Website

{{ embed_topic("project-deliverables.md#project-deliverables-website", "Admin " + icon_embedding + " Project → Deliverables → Product Website", "v14-deliverableWebsite", "3") }}
<p/>

**Submission**: Push the code to GitHub. Ensure the website is auto-published.


### v1.4 Demo

<img src="{{baseUrl}}/admin/images/v05demo.png" style="width: 250px"><p/>

{{ embed_topic("project-deliverables.md#project-deliverables-demo", "Admin " + icon_embedding + " Project → Deliverables → Demo", "v14-deliverableDemo", "3") }}
<p/>

* **Venue:** Same as the tutorial venue unless informed otherwise.
* **Schedule:** Your demo timing is same as your tutorial time in week 13.
  * Please arrive on time and remain outside the venue until called in.
  * There is an ==automatic penalty if you are not ready to start on time.==<br>
  * You should bring your own adapter if the display adapters available in your tutorial venue don't work for you.

### v1.4 Practical Exam

{{ embed_topic("project-deliverables.md#project-deliverables-practicalexam", "Admin " + icon_embedding + " Project → Deliverables → Practical Exam", "v14-deliverablePe", "3") }}
<p/>

**Time/venue:** week 13 lecture slot

</div>
</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w13-v14", show_main_text) }}