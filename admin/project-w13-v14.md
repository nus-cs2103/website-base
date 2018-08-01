{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<tip-box>

Overview: <include src="project-timeline.md#v14-overview" inline />
</tip-box>

**Summary of submissions**:

Team/Individual Item | Name format | Upload to
-------------------- | ----------- | ---------
{{ icon_team }} Source code |  tag as `v1.4` | GitHub
{{ icon_team }} Jar file |  `[team][product name].jar`<br>%%e.g. [T09-B1][ContactsPlus].jar%% | IVLE
{{ icon_team }} User Guide | `[TEAM_ID][Project Name]UserGuide.pdf`<br>  %%e.g.[T09-B1][Contacts Plus]UserGuide.pdf%% | IVLE
{{ icon_team }} Developer Guide | `[TEAM_ID][Project Name]DeveloperGuide.pdf`<br> %%e.g. [T09-B1][Contacts Plus]DeveloperGuide.pdf%% | IVLE
{{ icon_team }} Product Website | `README.adoc`, `Ui.png`, `AboutUs.adoc` | GitHub
{{ icon_individual }} Project Portfolio Page | `[TEAM_ID][Your Name]Portfolio.pdf`<br> %%e.g.[T09-B1][John Doe]Portfolio.pdf%% | IVLE
{{ icon_individual }} Collated files | | GitHub

**Deadline** for all v1.4 submissions is Week 13 Monday 23.59 unless stated otherwise.

<tip-box> 

* :exclamation: **Penalty for late submission:** ==-1 mark for each hour delayed, up to 3 hours.== Even a 1-second delay is considered late, irrespective of the reason. Penalty for delays beyond 3 hours are determined on a case by case basis. 
  * For submissions done via IVLE, the submission time is the timestamp shown by IVLE.
  * When determining the late submission penalty, **we take the latest submission** even if the same exact file was submitted earlier. Do not submit the same file multiple times if you want to avoid unnecessary late submission penalties.
* The whole team is penalized for problems in team submissions. Only the respective student is penalized for problems in individual submissions. 
* :exclamation: Please **follow submission instructions closely**. ==Any non-compliance will be penalized==. e.g. wrong file name, team member photos not suitable, etc.
* For pdf submissions, ensure the file is usable and hyperlinks in the file are correct. Problems in documents are considered bugs too %%&nbsp;e.g. broken links, outdated diagrams/instructions etc.%%.
* **Do not update the repo during the 14 days after the deadline.** Get our permission first if you need to update the repo during that _freeze_ period. You can continue to evolve your repo after that. 
</tip-box>

**Grading**:

<span class="flat">Described in [[Admin: Project: Assessment](#admin-project-assessment-anchor)]</span>

<panel src="project-assessment.md#main" header="%%Admin {{ icon_embedding }} Project: Assessment%%" class="embedding" />


### v1.4 Product

<span class="flat">Described in [[Admin: Project: Deliverables: Executable](#deliverable-executable)]</span>
<panel src="project-deliverables.md#project-deliverables-executable" header="%%Admin {{ icon_embedding }} Project → Deliverables → Executable%%"  class="embedding" />
<p/>

**Submission**: See summary of submissions above


### v1.4 Source Code

<span class="flat">Described in [[Admin: Project: Deliverables: Source Code](#deliverable-source-code)]</span>
<panel src="project-deliverables.md#project-deliverables-sourcecode" header="%%Admin {{ icon_embedding }} Project → Deliverables → Source Code%%" class="embedding" />
<p/>

**Submission**: Push the code to GitHub and tag with the version number. Source code (==including collated .md files==; please ensure the collated `.md` files are up to date; any updates to collated code files after the deadline will be considered a later submission). Note that the quality of the code in these ==collated code files accounts for a significant component of your final score==, graded individually.


### v1.4 User Guide

<span class="flat">Described in [[Admin: Project: Deliverables: User Guide](#deliverable-user-guide-ug)]</span>
<panel src="project-deliverables.md#project-deliverables-ug" header="%%Admin {{ icon_embedding }} Project → Deliverables → User Guide%%" class="embedding" />
<p/>

**Submission**: Convert the pdf (AB4 dev guide has some instructions on converting project docs to pdf) and upload to IVLE. See _summary of submissions_ above for the file name format.


### v1.4 Developer Guide

<span class="flat">Described in [[Admin: Project: Deliverables: Developer Guide](#deliverable-developer-guide-dg)]</span>
<panel src="project-deliverables.md#project-deliverables-dg" header="%%Admin {{ icon_embedding }} Project → Deliverables → Developer Guide%%" class="embedding" />
<p/>

**Submission**: Similar to UG


### v1.4 Product Website

<span class="flat">Described in [[Admin: Project: Deliverables: Product Website](#deliverable-product-website)]</span>
<panel src="project-deliverables.md#project-deliverables-website" header="%%Admin {{ icon_embedding }} Project → Deliverables → Product Website%%" class="embedding" />
<p/>

**Submission**: Push the code to GitHub


### v1.4 Demo

<img src="{{baseUrl}}/admin/images/v05demo.png" style="width: 250px">

<span class="flat">Described in [[Admin: Project: Deliverables: Demo](#deliverable-demo)]</span>
<panel src="project-deliverables.md#project-deliverables-demo" header="%%Admin {{ icon_embedding }} Project → Deliverables → Demo%%" class="embedding" />
<p/>

* **Venue:** Same as the tutorial venue unless informed otherwise.
* **Schedule:** Your demo timing is same as your tutorial time in week 13.
    Starting times: `Team B1: 00 minutes, B2: 20 minutes, B3: 40 minutes, B4: TBA`<br>
    At least some team members need to arrive 15 minutes ahead of the allocated time to set up your computer.<br>
    There is an ==automatic penalty if you are not ready to start on time.==<br>
    Wait outside the venue until you are called in.


### v1.4 Practical Exam

<span class="flat">Described in [[Admin: Project: Deliverables: Practical Exam](#deliverable-practical-exam)]</span>
<panel src="project-deliverables.md#project-deliverables-practicalexam" header="%%Admin {{ icon_embedding }} Project → Deliverables → Practical Exam%%" class="embedding" />
<p/>

**Time/venue:** week 13 lecture slot

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w13-v14", show_main_text) }}