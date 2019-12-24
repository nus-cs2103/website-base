{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}

1. {{ icon_individual }} Do final tweaks to the feature
1. {{ icon_team }} Submit the deliverables {{ timing_badge("by Monday 2359") }}
1. {{ icon_team }} Wrap up the milestone {{ timing_badge("by Wednesday 2359") }}
1. {{ icon_team }} Demo the product {{ timing_badge("during Tutorial", "secondary") }}
1. {{ icon_individual }} Prepare for the practical exam {{ timing_badge("before Lecture", "secondary") }}
1. {{ icon_individual }} Attend the practical exam {{ timing_badge("during Lecture") }}
{% endcall %}

<div id="body">

#### {{ thumb(1) }} {{ icon_individual }} Do final tweaks to the feature

* Do the final tweaks to the feature and the documentation. We strongly recommend not to do major changes to the product this close to the submission deadline.


#### {{ thumb(2) }} {{ icon_team }} Submit the deliverables {{ timing_badge("by Monday 2359", "secondary") }}


* **Deadline** for all v1.4 submissions is Week 13 Monday 23.59 unless stated otherwise.<br>
* Submit to LumiNUS folder we have set up, not to your project space.<br>
  {{ module | lower }}T students: documents should be submitted to both modules. It's not enough to submit to CS2101 side only.
* {{ icon_important_big_red }} **Penalty for late submission:**<br>
  ==-1 mark for missing the deadline (up to 2 hour of delay).==<br>
  -2 for an _extended delay_ (up to 24 hours late).<br>
  Penalty for delays beyond 24 hours is determined on a case by case basis.
  * Even a one-second delay is considered late, irrespective of the reason.
  * For submissions done via LumiNUS, the submission time is the timestamp shown by LumiNUS.
  * When determining the late submission penalty, **we take the latest submission** even if the same exact file was submitted earlier. Do not submit the same file multiple times if you want to avoid unnecessary late submission penalties.
  * The whole team is penalized for problems in team submissions. Only the respective student is penalized for problems in individual submissions.
* {{ icon_important_big_red }} Please **follow submission instructions closely**. ==Any non-compliance will be penalized==. e.g. wrong file name/format.
  * For pdf submissions, ensure the file is usable and hyperlinks in the file are correct. Problems in documents are considered bugs too %%e.g. broken links, outdated diagrams/instructions etc.%%.
* **Do not update the code during the 14 days after the deadline.** Get our permission first if you need to update the code in the repo during that _freeze_ period.
  * You can update issues/milestones/PRs even during the _freeze_ period.
  * You can update the code during the freeze period if the change is related to a late submission approved by us.
  * You can continue to evolve your repo after the freeze period.

<div class="indented">

<big>**Submissions:**</big>
</div>

* {{ icon_team }} **Product**:
  * Do a release on GitHub, tagged as `v1.4`.
  * Upload the jar file to LumiNUS. <br>
    File name: `[team][product name].jar` %%e.g. [{{ module }}T-W09-1][ContactsPlus].jar%%

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-executable", "Admin " + icon_embedding + " tP → Deliverables → Executable", "3") }}
</div>


* {{ icon_team }} **Source Code**: Push the code to GitHub and tag with the version number. Source code (==please ensure the code reported by RepoSense as yours is correct;== any updates to RepoSense config files or `@@author` annotations after the deadline will be considered a later submission). Note that the quality of the code attributed to you accounts for a significant component of your final score, graded individually.

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-sourcecode", "Admin " + icon_embedding + " tP → Deliverables → Source Code", "3") }}
</div>


* {{ icon_team }} **User Guide**: Convert the pdf (AB3 dev guide has some instructions on converting project docs to pdf) and upload to LumiNUS.<br>
  File name: `[TEAM_ID][product Name]UG.pdf`  %%e.g.[{{ module }}T-W09-1][Contacts Plus]UG.pdf%%

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-ug", "Admin " + icon_embedding + " tP → Deliverables → User Guide", "3") }}
</div>

* {{ icon_team }} **Developer Guide**: submit similar to UG<br>
  File name: `[TEAM_ID][product Name]DG.pdf` %%e.g. [{{ module }}T-W09-1][Contacts Plus]DG.pdf%%

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-dg", "Admin " + icon_embedding + " tP → Deliverables → Developer Guide", "3") }}
</div>
<p/>


* {{ icon_individual }} **Project Portfolio Page (PPP)**:
  * PDF file: submit similar to UG<br>
    File name: `[TEAM_ID][Your full Name as Given in LumiNUS]PPP.pdf` %%e.g.[{{ module }}T-W09-1][Leow Wai Kit, John]PPP.pdf%%<br>
    {{ icon_info }} Use `-` in place of `/` if your name has it e.g., `Ravi s/o Veegan` → `Ravi s-o Veegan` (reason: Windows does not allow `/` in file names) 
  * HTML version: make available on `github.io`

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-ppp", "Admin " + icon_embedding + " tP → Deliverables → Project Portfolio Page", "3") }}
</div>
<p/>


* {{ icon_team }} **Product Website**: Update (e.g., `README` page, `Ui.png`, `AboutUs`) on GitHub. Ensure the website is auto-published.

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-website", "Admin " + icon_embedding + " tP → Deliverables → Product Website", "3") }}
</div>
<p/>


#### {{ thumb(3) }} {{ icon_team }} Wrap up the milestone {{ timing_badge("by Wednesday 2359", "secondary") }}

* As usual, wrap up the milestone on GitHub. Note that the deadline for this is the same for everyone (i.e., does not depend on your tutorial).

<span id="demo-instructions" >

#### {{ thumb(4) }} {{ icon_team }} Demo the product {{ timing_badge("during Tutorial", "secondary") }}

<div class="indented-level2">

<img src="{{baseUrl}}/admin/images/v05demo.png" style="width: 250px"><p/>

{{ embed_topic("project-deliverables.md#project-deliverables-demo", "Admin " + icon_embedding + " tP → Deliverables → Demo", "3") }}
<p/>
</div>

* **Venue:** Same as the tutorial venue unless informed otherwise. You'll be using the TV at your regular tutorial table (not the projector) for the demo.
* **Schedule:** Your demo timing is same as your tutorial time in week 13.
  * Teams `1` and `3` will start at 05-minutes mark (e.g., 11.05 am), and teams `2` and `4` start at 30-minutes mark (e.g., 11.30 am).
  * Please ==arrive _before_ time== and remain outside the venue until called in. Late arrival or absence is liable to a penalty.
  * Any delay in starting the presentation is deducted out of your time allotment %%e.g., if you are scheduled to demo at 11.05-11.23 am (i.e., 18 minutes), you'll have to stop at 11.23 am even if you start at 11.10 am.%%
* You should bring your own adapter if the display adapters available in your tutorial venue don't work for you.
</span>


#### {{ thumb(5) }} {{ icon_individual }} Prepare for the practical exam {{ timing_badge("before Lecture", "secondary") }}

<div class="indented-level2">

<panel type="primary" header="Admin → Deliverables → **PE Overview**" minimized>

<include src="project-deliverables-pe.md#pe-overview" />
</panel>
<p/>
<panel type="primary" header="Admin → Deliverables → **PE-D/PE Preparation**" minimized>

<include src="project-testing.mbdf#testingPreparations" />
</panel>
</div>


#### {{ thumb(6) }} {{ icon_individual }} Attend the practical exam {{ timing_badge("during Lecture", "secondary") }}

* Attend the practical test, to be done during the lecture.

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-practicalexam", "Admin " + icon_embedding + " tP → Deliverables → Practical Exam", "3") }}
</div>

</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w13-v14", show_main_text) }}
