{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Set up project repo
1. Get familiar with the code base
1. Draft the UG
{% endcall %}

<div id="body">


#### {{ thumb(1) }} Set up project repo

<div id="product">

**<big>Project Management:</big>**

* Set up the team org and the team repo as explained below:

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#organization-setup", "Admin " + icon_embedding + " Appendix E(extract): **Organization setup**", "midv11-orgSetup", "1") }}
</div>

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#repo-setup", "Admin " + icon_embedding + " Appendix E(extract): **Repo setup**", "midv11-repoSetup", "1") }}
</div>

</div>

#### {{ thumb(2) }} Get familiar with the code base

* Do the provided tutorials to get familiar with the codebase
* When updating code in the repo, follow the workflow explained below:

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#workflow", "Admin " + icon_embedding + " Appendix E(extract): **Workflow**", "midv11-workflow", "1") }}
</div>

#### {{ thumb(3) }} Draft the UG

* **User Guide**:
  Draft a user guide in a convenient medium (e.g., a GoogleDoc) to describe what the product would be like when it is at v2.0.
  * We recommend that you follow the existing [AB3 User Guide](https://nus-{{ module }}-{{ semester | lower }}.github.io/addressbook-level3/UserGuide.html) in terms of structure and format.
  * As this is a very rough draft and the final version will be in a different format altogether %%(i.e., in asciidoc format)%%, don't waste time in formatting, copy editing etc. It is fine as long as the tutor can get a rough idea of the features from this draft. You can also do just the 'Features' section and omit the other parts.
  * Do try to come up with concrete command syntax for feature that you would implement (at least for those that you will implement by v1.4).
  * Consider including some UI mock-ups too %%(they can be hand-drawn or created using a tool such as PowerPoint, PlantUML or [Balsamiq](https://balsamiq.com/))%%.<br><br>

  <tip-box>

  {{ icon_tip }} It is highly recommended that you **divide documentation work (in the User Guide and the Developer Guide) among team members based on enhancements/features each person would be adding** %%&nbsp;e.g., If you are the person planing to add a feature X, you should be the person to describe the feature X in the User Guide and in the Developer Guide%%. For features that are not planned to be implemented by v1.4, you can divide them based on who will be implementing them _if_ the project were to continue until v2.0 (hypothetically).

  %%Reason: In the final project evaluation your documentation skills will be graded based on sections of the User/Developer Guide you have written.%%
   
  </tip-box>

</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w06-mid-v11", show_main_text) }}