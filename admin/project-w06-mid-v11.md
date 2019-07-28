{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. {{ icon_team }} Set up project repo
1. {{ icon_individual }} Get familiar with the code base
1. {{ icon_team }}  Conceptualize v2.0
1. {{ icon_individual }} Draft the UG
1. {{ icon_team }} Refine product design
{% endcall %}

<div id="body">

<box dismissible>

{{ icon_individual }} indicates an individual milestone %%(i.e., each team member has to do their part of the milestone, graded individually)%% while {{ icon_team }} indicates a team milestone %%(some or all members may do the work, graded for the whole team)%%.

{{ icon_important_big_red }} **Milestone progress is graded**. Be reminded that reaching individual and team milestones are considered for <trigger trigger="click" for="modal:v11-projectMgtGrading">grading the _project management_ component</trigger> of your project grade.

{{ icon_important_big_red }} **Most aspects project progress are tracked using automated scripts.** ==Please follow our instructions closely or else the script will not be able to detect your progress==. We prefer not to spend admin resources processing requests for partial credit for work that did not follow the instructions precisely, unless the progress was not detected due to a bug in the script.

{{ icon_important_big_red }} **Milestone requirements are cumulative**. The recommended progress for the mid-milestone is an implicit requirement for the actual milestone unless a milestone requirement overrides a mid-milestone requirement %%e.g., mid-milestone requires a document to be in a temp format while the actual milestone requires it to be in the proper format%%. Similarly, a requirement for milestone `n` is also an implicit requirement for milestone `n+1` unless `n+1` overrides the `n` requirement. This means ==if you miss some requirement at milestone `n`, you should try to achieve it before milestone `n+1`== or else it could be noted again as a 'missed requirement' at milestone `n+1`.
</box>

#### {{ thumb(1) }} {{ icon_team }} Set up project repo

* Set up the team org and the team repo as explained below:

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#organization-setup", "Admin " + icon_embedding + " Appendix E(extract): **Organization setup**", "midv11-orgSetup", "1") }}
</div>

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#repo-setup", "Admin " + icon_embedding + " Appendix E(extract): **Repo setup**", "midv11-repoSetup", "1") }}
</div>

#### {{ thumb(2) }} {{ icon_individual }} Get familiar with the code base

* Do the provided tutorials to get familiar with the codebase
* When updating code in the repo, follow the workflow explained below:

<div class="indented-level2">

{{ embed_topic("appendixE-gitHub.md#workflow", "Admin " + icon_embedding + " Appendix E(extract): **Workflow**", "midv11-workflow", "1") }}
</div>

#### {{ thumb(3) }} {{ icon_team }} Conceptualize v2.0

* Based on your user story categorization in the previous week, given module requirements/constraints for the project, and the current state of the product, select which user stories you are likely to include in v2.0.

* Conceptualize the product in terms of how it will look like at v2.0.

#### {{ thumb(4) }} {{ icon_individual }} Draft the UG

* Draft a user guide in a convenient medium (e.g., a GoogleDoc) to describe what the product would be like when it is at v2.0.
  * We recommend that you follow the existing [AB3 User Guide](https://nus-{{ module }}-{{ semester | lower }}.github.io/addressbook-level3/UserGuide.html) in terms of structure and format.
  * As this is a very rough draft and the final version will be in a different format altogether %%(i.e., in asciidoc format)%%, don't waste time in formatting, copy editing etc. It is fine as long as the tutor can get a rough idea of the features from this draft. You can also do just the 'Features' section and omit the other parts.
  * Do try to come up with concrete command syntax for feature that you would implement (at least for those that you will implement by v1.4).
  * Consider including some UI mock-ups too %%(they can be hand-drawn or created using a tool such as PowerPoint, PlantUML or [Balsamiq](https://balsamiq.com/))%%.
  * {{ icon_important_big_red }} **Submission**: Save the draft UG as a PDF file, name it `{team-id}.pdf` e.g., `CS2103T-W09-1.pdf`, and upload to LumiNUS.<br><br>

  <tip-box>

  {{ icon_tip }} It is highly recommended that you **divide documentation work (in the User Guide and the Developer Guide) among team members based on enhancements/features each person would be adding** %%&nbsp;e.g., If you are the person planing to add a feature X, you should be the person to describe the feature X in the User Guide and in the Developer Guide%%. For features that are not planned to be implemented by v1.4, you can divide them based on who will be implementing them _if_ the project were to continue until v2.0 (hypothetically).

  %%Reason: In the final project evaluation your documentation skills will be graded based on sections of the User/Developer Guide you have written.%%
   
  </tip-box>

#### {{ thumb(5) }} {{ icon_team }} Refine product design

* Review the UG to ensure the features written by each member fit together to form a cohesive product. Note that cohesiveness of the product is a grading criterion.

</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w06-mid-v11", show_main_text) }}