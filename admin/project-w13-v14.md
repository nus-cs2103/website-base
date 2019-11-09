{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}

1. {{ icon_individual }} Do final tweaks to the feature
1. {{ icon_team }} Submit the deliverables {{ timing_badge("by Monday 2359") }}
1. {{ icon_team }} Wrap up the milestone {{ timing_badge("by Wednesday 2359") }}
1. {{ icon_team }} Demo the product {{ timing_badge("during Tutorial", "secondary") }}
1. {{ icon_team }} Prepare for the practical exam {{ timing_badge("before Lecture", "secondary") }}
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
* **Do not update the repo during the 14 days after the deadline.** Get our permission first if you need to update the repo during that _freeze_ period. You can continue to evolve your repo after that.


<big>**Submissions:**</big>
* {{ icon_team }} **Product**:
  * Do a release on GitHub, tagged as `v1.4`.
  * Upload the jar file to LumiNUS. <br>
    File name: `[team][product name].jar` %%e.g. [{{ module }}T-W09-1][ContactsPlus].jar%%

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-executable", "Admin " + icon_embedding + " Project → Deliverables → Executable", "v14-executable", "3") }}
</div>


* {{ icon_team }} **Source Code**: Push the code to GitHub and tag with the version number. Source code (==please ensure the code reported by RepoSense as yours is correct;== any updates to RepoSense config files or `@@author` annotations after the deadline will be considered a later submission). Note that the quality of the code attributed to you accounts for a significant component of your final score, graded individually.

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-sourcecode", "Admin " + icon_embedding + " Project → Deliverables → Source Code", "v14-sourcecode", "3") }}
</div>


* {{ icon_team }} **User Guide**: Convert the pdf (AB3 dev guide has some instructions on converting project docs to pdf) and upload to LumiNUS.<br>
  File name: `[TEAM_ID][product Name]UserGuide.pdf`  %%e.g.[{{ module }}T-W09-1][Contacts Plus]UserGuide.pdf%%

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-ug", "Admin " + icon_embedding + " Project → Deliverables → User Guide", "v14-deliverableUg", "3") }}
</div>

* {{ icon_team }} **Developer Guide**: submit similar to UG<br>
  File name: `[TEAM_ID][product Name]DeveloperGuide.pdf` %%e.g. [{{ module }}T-W09-1][Contacts Plus]DeveloperGuide.pdf%%

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-dg", "Admin " + icon_embedding + " Project → Deliverables → Developer Guide", "v14-deliverableDg", "3") }}
</div>
<p/>


* {{ icon_individual }} **Project Portfolio Page (PPP)**:
  * PDF file: submit similar to UG<br>
    File name: `[TEAM_ID][Your Name]Portfolio.pdf` %%e.g.[{{ module }}T-W09-1][John Doe]Portfolio.pdf%%
  * HTML version: make available on `github.io`

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-ppp", "Admin " + icon_embedding + " Project → Deliverables → Project Portfolio Page", "v14-deliverablePpp", "3") }}
</div>
<p/>


* {{ icon_team }} **Product Website**: Update (e.g., `README` page, `Ui.png`, `AboutUs`) on GitHub. Ensure the website is auto-published.

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-website", "Admin " + icon_embedding + " Project → Deliverables → Product Website", "v14-deliverableWebsite", "3") }}
</div>
<p/>


#### {{ thumb(3) }} {{ icon_team }} Wrap up the milestone {{ timing_badge("by Wednesday 2359", "secondary") }}

* As usual, wrap up the milestone on GitHub. Note that the deadline for this is the same for everyone (i.e., does not depend on your tutorial).

#### {{ thumb(4) }} {{ icon_team }} Demo the product {{ timing_badge("during Tutorial", "secondary") }}

<img src="{{baseUrl}}/admin/images/v05demo.png" style="width: 250px"><p/>

{{ embed_topic("project-deliverables.md#project-deliverables-demo", "Admin " + icon_embedding + " Project → Deliverables → Demo", "v14-deliverableDemo", "3") }}
<p/>

* **Venue:** Same as the tutorial venue unless informed otherwise.
* **Schedule:** Your demo timing is same as your tutorial time in week 13.
  * Please arrive on time and remain outside the venue until called in.
  * There is an ==automatic penalty if you are not ready to start on time.==<br>
  * You should bring your own adapter if the display adapters available in your tutorial venue don't work for you.


#### {{ thumb(5) }} {{ icon_team }} Prepare for the practical exam {{ timing_badge("before Lecture", "secondary") }}

* **Download the zip file containing the product to be tested.** More information to be released later.


#### {{ thumb(6) }} {{ icon_individual }} Attend the practical exam {{ timing_badge("during Lecture", "secondary") }}

* Attend the practical test, to be done during the lecture. 
  {{ embed_topic("project-deliverables.md#project-deliverables-practicalexam", "Admin " + icon_embedding + " Project → Deliverables → Practical Exam", "v14-deliverablePe", "3") }}


</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w13-v14", show_main_text) }}