{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<p class="lead" style="color: purple"><md>:far-calendar-check: <include src="project-timeline.md#v10-overview" inline /></md></p>

**v1.0 Summary of Milestone**

Here is a summary of items you need to deliver to _reach_ v1.0 individual ({{ icon_individual }}) and team ({{ icon_team }}) milestones. See sections below for more details of each item.

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
{{ icon_team }} requirements documented | a draft of v2.0 requirements in some form
{{ icon_individual }} [optional] product survey documented | none
{{ icon_team }} v2.0 conceptualized | a draft of v2.0 user guide in some form
{{ icon_team }} feature releases planned | a rough feature release plan

{{ icon_important_big_red }} ==Reaching individual and team milestones are considered for grading== the _project management_ component of your project grade (expand the panel below for more info).

{{ icon_important_big_red }} The deadline for reaching a milestone is ==the midnight before your tutorial== %%e.g., if your tutorial is on Wednesday, you need to reach the milestone by Tuesday midnight.%%

{{ embed_topic("project-grading.md#project-management-grading", "Admin " + icon_embedding + " Project Grading → Project Management", "v10-projectMgsGrading", "3") }}


* **Step 1 : Brainstorm user stories**

  <img src="{{baseUrl}}/admin/images/v00.png" width="250px">

  Get together with your team members and <trigger trigger="click" for="modal:v10-brainstorming">brainstorm</trigger> for <trigger trigger="click" for="modal:v10-userstories">user stories</trigger> **&nbsp;for the v2.0 of the product**. Note that in the module project you will deliver only up to v1.4 but here you should consider up to v2.0 (i.e. beyond the module).

  * It is ok to have more user stories than you can deliver in the project. %%Aim to create at least 30 user stories. Include all 'obvious' ones you can think of but also look for 'non obvious' ones that you think are likely to be missed by other teams.%%

  * Refer <trigger trigger="click" for="modal:v10-userstoryusagetips">[Textbook {{ icon_embedding }} Specifying Requirements → UserStories →  Usage → (section) Tips]</trigger> for tips on how to use user stories in this task.

  * You can write each user story in a piece of paper (e.g. yellow sticky note, index card, or just pieces of paper about the size of a playing card). Alternatively you can use an online tool (some examples given in <trigger trigger="click" for="modal:v10-onlinetools">[Textbook {{ icon_embedding }} Specifying Requirements → UserStories → Usage → (panel) Tool Examples ]</trigger>).<br>

  * Note that ==you should not 'evaluate' the value of user stories while doing the above==. %%&nbsp;Reason: an important aspect of brainstorming is not judging the ideas generated.%%


<modal large title="Textbook {{ icon_embedding }}" id="modal:v10-brainstorming">
  <include src="../book/gatheringRequirements/brainstorming/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

<modal large title="Textbook {{ icon_embedding }}" id="modal:v10-userstories">
  <include src="../book/specifyingRequirements/userStories/introduction/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

<modal large title="Textbook {{ icon_embedding }} Specifying Requirements → UserStories → Usage → (panel)Tool Examples" id="modal:v10-onlinetools">
  <include src="../book/specifyingRequirements/userStories/usage/tools.md"/>
</modal>

<modal large title="Textbook {{ icon_embedding }} Specifying Requirements → UserStories →  Usage → (section) Tips" id="modal:v10-userstoryusagetips">
  <include src="../book/specifyingRequirements/userStories/usage/text.md#usageTips"/>
</modal>

<div class="indented-level3">
<box>

:bulb: Recommended: **You can use GitHub issue tracker to manage user stories**, but for that you need to set up your team's GitHub organization, project fork, and issue tracker first. Instructions for doing those steps are in the panel below.

<panel header="%%Admin {{ icon_embedding }} Appendix E: GitHub (extract)%%">
  <include src="appendixE-gitHub.md#organization-setup"/>
  <include src="appendixE-gitHub.md#repo-setup"/>
  <include src="appendixE-gitHub.md#issue-tracker-setup"/>
  <include src="appendixE-gitHub.md#project-schedule-tracking"/>
</panel>

</box>

<panel header="{{ icon_example }} User Story examples (from a different product)" minimized>

`As a user I can add a task by specifying a task description only, so that I can record tasks that need to be done ‘some day’.`
`As a user I can find upcoming tasks, so that I can decide what needs to be done soon.`
`As a user I can delete a task, so that I can get rid of tasks that I no longer care to track.`
`As a new user I can view more information about a particular command, so that I can learn how to use various commands.`
`As an advanced user I can use shorter versions of a command, so that type a command faster.`

</panel>
</div>

<br>

* **Step 2: Prioritize the user stories**

  <img src="{{baseUrl}}/admin/images/userstories.png" width="250px">

  Suggested workflow:

  * Take one user story at a time and get team member opinions about it.
  * Based on the team consensus, put the story (i.e. the piece of paper) onto one of these three piles:

    * `Must-Have` : The product will be practically useless to the target user without this feature.
    * `Nice-To-Have` : The target user can benefit from this user story significantly but you are not certain if you'll have time to implement it.
    * `Not-Useful` : No significant benefit to the target user, or does not fit into the product vision.

  * %%If using physical paper to record user stories: After all stories have been put in the above three piles, you can make a record of which stories are in the three piles.%%

* **Step 3: Document requirements of the product**

  Based on your user story categorization in the step above, given module requirements/constraints for the project, and the current state of the product, select which user stories you are likely to include in v2.0.

  Document the following items using a convenient format (e.g., a GoogleDoc). %%Do not spend time on formatting the content nicely; reason: these will be ported to the actual Developer Guide in your project repo later.%%<br>
  :bulb: Some examples of these can be found in the [AB4 Developer Guide](https://se-edu.github.io/addressbook-level4/DeveloperGuide.html#product-scope).

  * **Target user profile**, **value proposition**, and <trigger trigger="click" for="modal:v10-userstories">**user stories**</trigger>: Update the target user profile and value proposition to match the project direction you have selected. Give a list of the user stories (and update/delete existing ones, if applicable), including priorities. This can include user stories considered but will not be included in the final product.
  * <trigger trigger="click" for="modal:v10-usecases">**Use cases**</trigger>: Give use cases (textual form) for a few representative user stories that need multiple steps to complete. %%e.g. Adding a tag to a person (assume the user needs to find the person first)%%
  * <trigger trigger="click" for="modal:v10-nfr">**Non-functional requirements**</trigger>:
    Note: Many of the project constraints mentioned above are NFRs. You can add more. e.g. performance requirements, usability requirements, scalability requirements, etc.
  * <trigger trigger="click" for="modal:v10-glossary">**Glossary**</trigger>: Define terms that are worth defining.
  *  [Optional]<trigger trigger="click" for="modal:v10-prodsurveys">**Product survey**</trigger>: Explore a few similar/related products and describe your findings i.e. Pros, cons, (from the target user's point of view).

<modal large title="Textbook {{ icon_embedding }} Specifying Requirements → Use Cases" id="modal:v10-usecases">
  <include src="../book/specifyingRequirements/useCases/introduction/unit-inElsewhere-asFlat.md" boilerplate />
</modal>

<modal large title="Textbook {{ icon_embedding }}" id="modal:v10-nfr">
  <include src="../book/requirements/nonFunctionalRequirements/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

<modal title="Textbook {{ icon_embedding }}" id="modal:v10-glossary">
  <include src="../book/specifyingRequirements/glossary/what/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>

<modal title="Textbook {{ icon_embedding }}" id="modal:v10-prodsurveys">
  <include src="../book/gatheringRequirements/productSurveys/unit-inElsewhere-asFlat.md" boilerplate/>
</modal>


### v1.0 Documentation

* **Developer Guide**:
  Have a draft of the requirements of your project, as described in <trigger trigger="click" for="modal:v10-midv10">mid-v1.0 progress guide</trigger>.

<modal large title="Admin » Project → mid-v1.0" id="modal:v10-midv10">
  <include src="project-w04-inception.md#body"/>
</modal>
  
* **User Guide**:  
  Draft a user guide in a convenient medium (e.g., a GoogleDoc) to describe what the product would be like when it is at v2.0.
  * We recommend that you follow the existing [AB4 User Guide](https://nus-{{ module }}-{{ semester | lower }}.github.io/addressbook-level4/UserGuide.html) in terms of structure and format.
  * As this is a very rough draft and the final version will be in a different format altogether %%(i.e., in asciidoc format)%%, don't waste time in formatting, copy editing etc. It is fine as long as the tutor can get a rough idea of the features from this draft. You can also do just the 'Features' section and omit the other parts.
  * Do try to come up with concrete command syntax for feature that you would implement (at least for those that you will implement by v1.4).
  * Consider including some UI mock-ups too %%(they can be hand-drawn or created using a tool such as PowerPoint or [Balsamiq](https://balsamiq.com/))%%.

  <tip-box> 
  
  :bulb: It is highly recommended that you **divide documentation work (in the User Guide and the Developer Guide) among team members based on enhancements/features each person would be adding** %%&nbsp;e.g., If you are the person planing to add a feature X, you should be the person to describe the feature X in the User Guide and in the Developer Guide%%. For features that are not planned to be implemented by v1.4, you can divide them based on who will be implementing them _if_ the project were to continue until v2.0 (hypothetically).
  
  %%Reason: In the final project evaluation your documentation skills will be graded based on sections of the User/Developer Guide you have written.%%
    
  </tip-box>


**Suggested length**: Follow the existing user guide and developer guides in terms of the level of details.

=={{ icon_important_big_red }} **Submission**==: Save your draft a single pdf file, name it `{Your Team ID}.pdf` %%e.g., `W09-3.pdf`%% and upload to IVLE.

### v1.0 Project Management

* After the v2.0 is conceptualized, decide which features each member will do by v1.4. %%We realize that it will be hard for you to estimate the effort required for each feature as you are not familiar with the code base. Nevertheless, come up with a project plan as per your best estimate; this plan can be revised at later stages. It is better to start with _some_ plan rather than no plan at all. If in doubt, choose to do _less_ than _more_; we don't expect you to deliver a lot of big features.%%
* Divide each of those features into three increments, to be released at v1.1, v1.2, v1.3 (v1.4 omitted deliberately as a buffer). ==Each increment should deliver a end-user visible enhancement.==
* Document the above two items somewhere e.g., in a Google doc/sheet. An example is given below:

  ```
  * Jake Woo: Profile photo feature
    * v1.1: show a place holder for photo, showing a generic default image
    * v1.2: can specify photo location if it is in local hard disk,
            show photo from local hard disk
    * v1.3: auto-copy the photo to app folder, support using online photo
            as profile pic, stylize photo e.g., round frame
  ```


=={{ icon_important_big_red }} **Submission**==: Include in the pdf file you upload to IVLE.

</div>
</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w05-v10", show_main_text) }}