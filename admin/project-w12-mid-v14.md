{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}

1. {{ icon_individual }} Tweak the product as per peer-testing results.
1. {{ icon_individual }} Draft the PPP
1. {{ icon_team }} Prepare for the demo rehearsal
{% endcall %}

<div id="body">

<box background-color="white" border-color="red">

**Remind yourself of the project grading criteria:**

<panel type="seamless" src="project-grading.md#main" header="%%Admin {{ icon_embedding }} Project: Grading%%" class="embedding" />
</box>

#### {{ thumb(1) }} {{ icon_individual }} Tweak the product as per peer-testing results

* Learn the procedure for dealing with PED bugs you received:

<div class="indented-level2">
{{ embed_topic("project-deliverables.md#after-ped", "Admin " + icon_embedding + " Project → Deliverables → **After the PED**", "midv14_afterPed", "3") }}
</div>

* **Freeze features** around this time. Ensure the current product have all the features you intend to release at v1.4. Adding major changes after this point is risky. The remaining time is better spent fixing problems discovered late or on fine-tuning the product.
* **Update documentation** to match the product.
* **Consider increasing test coverage** by adding more tests if it is lower than the level you would like it to be. Take note of <trigger trigger="click" for="modal:mid-v14-testingExpectations">our expectation on test code</trigger>. 
* After you have sufficient code coverage, **fix remaining code quality problems** and bring up the quality to your target level.

<modal title="Admin {{ icon_embedding }} Project Asessement → Expectation on testing" id="modal:mid-v14-testingExpectations">
  <include src="project-scope.md#testing-expectations"/>
</modal>

<div class="indented-level2">
{{ embed_topic("project-grading.md#projectGrading-codeQuality-criteria", "Admin " + icon_embedding + " Project Grading → Code Quality Tips", "midv14_codeQualityTips", "3") }}
</div>

#### {{ thumb(2) }} {{ icon_individual }} Draft the PPP

* Create the first version of your _Project Portfolio Page (PPP)_. Reason: **Each member needs to create a PPP** to describe your contribution to the project. Creating a PPP takes a significant effort; it is ==too risky to leave it to the last week of the project==. 

<div class="indented-level2">
{{ embed_topic("project-deliverables.md#project-deliverables-ppp", "Admin " + icon_embedding + " Project → Deliverables → Project Portfolio Page", "midv14_deliverablesPpp", "2") }}
</div>

#### {{ thumb(3) }} {{ icon_team }} Prepare for the demo rehearsal

* You will do a product demo during the tutorial to serve as a rehearsal for the final project demo at v1.4
  * ==Follow <trigger trigger="click" for="modal:mid-v14-demo-instructions">final demo instructions</trigger>== as much as possible.
  * **Cover all features**, not just the ones added in the recent iteration.
  * Try to make it **a 'well prepared' demo** i.e., know in advance exactly what you'll do in the demo.

<modal large title="Admin {{ icon_embedding }} Project → v1.4 Demo (extract)" id="modal:mid-v14-demo-instructions">
  <include src="project-deliverables.md#project-deliverables-demo"/>
</modal>

#### {{ thumb("+") }} {{ icon_team }} Other things to note

* {{ icon_important_big_red }} Once again, double-check to ensure the code attributed to you by RepoSense is correct, as reported in the [tp Code Dashboard]({{ tp_dashboard }}). Click on the `</>` icon against your name and verify that the ==lines attributed to you (i.e., lines marked as green)== reflects your code contribution correctly. This is important becaues some aspects of your project grade (e.g., code quality) will be graded based on those lines.<br>
  &nbsp;&nbsp;&nbsp;&nbsp;<img src="images/greenLines.png" width="600">
<p/>
<div class="indented-level2">
{{ embed_topic("tools.md#reposense", "Admin " + icon_embedding + " Tools → Using RepoSense", "midv14_repoSenseCompatibility", "1") }}
</div>

</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w12-mid-v14", show_main_text) }}