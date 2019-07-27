{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb with context %}

{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body"> 

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


{{ icon_important_big_red }} ==Reaching individual and team milestones are considered for grading== the _project management_ component of your project grade (expand the panel below for more info).

{{ icon_important_big_red }} The deadline for reaching a milestone is ==the midnight before your tutorial== %%e.g., if your tutorial is on Wednesday, you need to reach the milestone by Tuesday midnight.%%

{{ embed_topic("project-grading.md#project-management-grading", "Admin " + icon_embedding + " Project Grading → Project Management", "v10-projectMgsGrading", "3") }}



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


<div id="documentation">

**<big>Documentation:</big>**

<tip-box>

**Recommended procedure for updating docs**:

1. Divide among yourselves who will update which parts of the document(s).
1. Update the team repo by following the workflow mentioned above.

</tip-box>

<div class="indented">

  Update the following pages in your project repo:
</div>

* **_About Us_ page**:
  This page is used for module admin purposes. ==Please follow the format closely== or else our scripts will not be able to give credit for your work.
  * Replace info of SE-EDU developers with info of your team, including a ==suitable photo== as described <trigger trigger="click" for="modal:mid-v12-photo">here</trigger>.
  * Including the name/photo of the supervisor/lecturer is optional.
  * The photo of a team member should be `doc/images/githbub_username_in_lower_case.png` %%e.g. `docs/images/damithc.png`%%. ==If you photo is in jpg format, name the file as `.png` anyway==.
  * Indicate the different roles played and responsibilities held by each team member. You can reassign these <trigger trigger="click" for="modal:midv11-rolesAndResponsibilities">roles and responsibilities %%(as explained in Admin {{ icon_embedding }} Project Scope)%%</trigger> later in the project, if necessary.

<modal large title="Admin {{ icon_embedding }} Choosing a profile photo" id="modal:mid-v12-photo">
  <include src="project-deliverables.md#profile-photo"/>
</modal>

<modal large title="Admin {{ icon_embedding }} Project Scope (extract): roles and responsibilities" id="modal:midv11-rolesAndResponsibilities">
  <include src="project-scope.md#roles"/>
</modal>

* **_Contact Us_ Page**: Update to match your product.

* **README.adoc** page: Update it to match your project.

  * Add a UI mockup of your intended final product.
    Note that the ==image of the UI should be `docs/images/Ui.png`== so that it can be downloaded by our scripts. Limit the file to contain one screenshot/mockup only and ensure the new image is roughly the same `height x width` proportions as the original one. %%Reason: when we compile these images from all teams into one page ([example](https://nus-cs2103-ay1819s1.github.io/cs2103-website/admin/projectList.html)), yours should not look out of place.%%

  * The original `README.adoc` file (which doubles as the landing page of your project website) is written to read like the introduction to an SE learning/teaching resource. You should ==restructure this page to look like the home page of a real product== (not a school project) targeting real users %%&nbsp;e.g. remove references to addressbook-level3, Learning Outcomes etc. mention target users, add a marketing blurb etc.%% On a related note, also remove `Learning Outcomes` link and related pages.

  * Update the link of the Travis _build status badge_ (<img src="https://travis-ci.org/se-edu/addressbook-level4.svg?branch=master" alt="Build Status">) so that it reflects the build status of your team repo.<br>
    For the other badges,
    * either set up the respective tool for your project (AB-4 Developer Guide has instructions on how to set up AppVeyor and Coveralls) and update the badges accordingly,
    * or remove the badge.

  * Acknowledge the original source of the code i.e. AddressBook-Level4 project created by SE-EDU initiative at `https://github.com/se-edu/`

* **User Guide**: Start moving the content from your User Guide (draft created in previous weeks) into the User Guide page in your repository. If a feature is not implemented, mark it as 'Coming in v2.0' ([example](https://se-edu.github.io/addressbook-level4/UserGuide.html#encrypting-data-files-code-coming-in-v2-0-code)).

* **Developer Guide**: Similar to the User Guide, start moving the content from your Developer Guide (draft created in previous weeks) into the Developer Guide page in your team repository.



</div>

{{ icon_important_big_red }} **Milestone progress is graded**. Be reminded that reaching individual and team milestones are considered for <trigger trigger="click" for="modal:v11-projectMgtGrading">grading the _project management_ component</trigger> of your project grade.

{{ icon_important_big_red }} **Most aspects project progress are tracked using automated scripts.** ==lease follow our instructions closely or else the script will not be able to detect your progress==. We prefer not to spend admin resources processing requests for partial credit for work that did not follow the instructions precisely, unless the progress was not detected due to a bug in the script.

{{ icon_important_big_red }} **Milestone requirements are cumulative**. The recommended progress for the mid-milestone is an implicit requirement for the actual milestone unless a milestone requirement overrides a mid-milestone requirement %%e.g., mid-milestone requires a document to be in a temp format while the actual milestone requires it to be in the proper format%%. Similarly, a requirement for milestone `n` is also an implicit requirement for milestone `n+1` unless `n+1` overrides the `n` requirement. This means ==if you miss some requirement at milestone `n`, you should try to achieve it before milestone `n+1`== or else it could be noted again as a 'missed requirement' at milestone `n+1`.

**v1.1 Summary of Milestone**

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
{{ icon_team }} Team org/repo set up | as stated in <trigger trigger="click" for="modal:v11summary-midv11">mid-v1.1</trigger> (i.e., _team PR_ created, _auto-publishing_ of docs set up)
{{ icon_individual }} Some code enhancements done | created PRs to do local/global changes
{{ icon_individual }} Photo uploaded | a photo complying to <trigger trigger="click" for="modal:v11-photo">our guidelines</trigger> is in the master branch of your team repo
{{ icon_team }} Project docs updated | updated docs are merged to the master branch
{{ icon_team }} Milestone wrapped up | a commit in the master branch tagged as `v1.1`


<modal large title="Admin {{ icon_embedding }} Project: mid-v1.1" id="modal:v11summary-midv11">
  <include src="project-w06-mid-v11.md#body"/>
</modal>

<modal large title="Admin {{ icon_embedding }} Project Grading → Project Management" id="modal:v11-projectMgtGrading">
  <include src="project-grading.md#project-management-grading"/>
</modal>

<modal large title="Admin {{ icon_embedding }} Choosing a profile photo" id="modal:v11-photo">
  <include src="project-deliverables.md#profile-photo"/>
</modal>

<div id="documentation">

### v1.1 Project Management

* {{ icon_team }} Fix any errors in org/repo set up %%&nbsp;(e.g. wrong repo name)%%.
* **Wrap up the milestone using a git tag `v1.1`** as explained below:
  * When the milestone deadline is near (e.g., 0.5 days before the deadline), if you think some of the ongoing work intended for the current milestone may not finish in time, reassign them to a future milestone.
  * After all changes that _can_ be merged before the milestone deadline has been merged, use `git tag` feature to tag the current version with the milestone and push the tag to the team repo.


### v1.1 Documentation

* Update User Guide, Developer Guide, README, and About Us pages as described earlier in <trigger trigger="click" for="modal:v11docs-midv11">mid-v1.1 progress guide</trigger>.

  **Submission**: merge your changes to the master branch of your repo.

<modal large title="Admin {{ icon_embedding }} Project: mid-v1.1" id="modal:v11docs-midv11">
  <include src="project-w06-mid-v11.md#body"/>
</modal>

</div>
<div id="product">

### v1.1 Product

* Each member should try to add some enhancements that are in line with the vision for v2.0. After adding some _local-impact_ changes as recommended in <trigger trigger="click" for="modal:v11docs-midv11">mid-v1.1 progress guide</trigger>, attempt to do some ==<tooltip content="should go beyond the component you are in charge of">_global-impact_</tooltip> enhancements==, touching as many other components as possible. Refer to the AddressBook-Level4 Developer Guide has [some guidance on how to implement a new feature end-to-end](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/addressbook-level4/DeveloperGuide.html#creating-a-new-command-code-remark-code).

</div>

</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w07-v11", show_main_text) }}