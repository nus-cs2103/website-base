{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. {{ icon_team }} Update project website: `AboutUs`, `ContactUs`, `README`
1. {{ icon_individual }} Update the UG
1. {{ icon_team }} Update the DG: user stories, glossary, NFRs, use cases
1. {{ icon_team }} Wrap up **v1.1**
1. {{ icon_individual }} Draft a rough project plan
1. {{ icon_individual }} Start implementing a minimal version of your feature
{% endcall %}

<div id="body">

#### {{ thumb(1) }} {{ icon_team }} Update project website: `AboutUs`, `ContactUs`, `README`

<box type="info">

**Recommended procedure for updating docs**:

1. Divide among yourselves who will update which parts of the document(s).
1. Update the team repo by following the recommended workflow.

{{ embed_topic("appendixE-gitHub.md#workflow-before-v11", "Admin " + icon_embedding + " Appendix E(extract): **Workflow**", "v11-workflowBeforeV11", "3") }}

</box>

Update the following pages in your project repo:

* **_About Us_ page**:
  This page is used for module admin purposes. ==Please follow the format closely== or else our scripts will not be able to give credit for your work.
  * Replace info of SE-EDU developers with info of your team. Include a ==suitable photo== as described <trigger trigger="click" for="modal:mid-v12-photo">here</trigger>.
  * Including the name/photo of the supervisor/lecturer is optional.
  * The filename of the profile photo (even a placeholder image) should be `doc/images/githbub_username_in_lower_case.png` %%e.g. `docs/images/damithc.png`%%. ==If you photo is in jpg format, name the file as `.png` anyway==.
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
    Note that the ==image of the UI should be `docs/images/Ui.png`== so that it can be downloaded by our scripts. Limit the file to contain one screenshot/mockup only and ensure the new image is roughly the same `height x width` proportions as the original one. %%Reason: when we compile these images from all teams into one page ([example](projectList.html)), yours should not look out of place.%%

  * The original `README.adoc` file (which doubles as the landing page of your project website) is written to read like the introduction to an SE learning/teaching resource. You should ==restructure this page to look like the home page of a real product== (not a school project) targeting real users. For instance,
    * remove references to addressbook-level2
    * remove Learning Outcomes
    * mention your target users
    * add a marketing blurb

  * Update the link of the Travis _build status badge_ (<img src="https://travis-ci.org/se-edu/addressbook-level3.svg?branch=master" alt="Build Status">) so that it reflects the build status of your team repo. For the other badges,
    * either set up the respective tool for your project (AB3 Developer Guide has instructions on how to set up AppVeyor and Coveralls) and update the badges accordingly,
    * or remove the badge.

  * Acknowledge the original source of the code i.e. AddressBook-Level3 project created by SE-EDU initiative at `https://se-education.org`

* **Website heading**: Update the website heading to match your product. Currently it is set to `AddressBook Level 3 - ...`.<br>
    <img src="images/addressBookWebsiteHeading.png" />

<box>

{{ icon_tip }} If you updated the above pages correctly, details of your project in the [**Project List Page**](projectList.html) should look neat and complete %%i.e., no broken links%%.
</box>

#### {{ thumb(2) }} {{ icon_individual }} Update the UG

* Move the draft UG into the User Guide page in your repository. If a feature is not implemented, mark it as 'Coming in v2.0' ([example]({{ ab3_website }}/UserGuide.html#encrypting-data-files-code-coming-in-v2-0-code)).<br>
  As <trigger trigger="click" for="modal:v11-divideDocs">mentioned in week 6</trigger>, we recommend that **each person updates their own part of the docs** so that we can easily track the contribution of each member using [RepoSense]({{ tp_dashboard }}).<br>
  {{ icon_tip }} While it is more convenient for one person to update the entire UG, splitting the work will give you a good opportunity to learn to deal with merge conflicts.

<modal large title="About Dividing Documentation Work" id="modal:v11-divideDocs">
  <include src="project-w06-mid-v11.md#divideDocs"/>
</modal>

#### {{ thumb(3) }} {{ icon_team }} Update the DG: user stories, glossary, NFRs, use cases

* Update the following in the DG, based on your project notes from the previous weeks.<br>
  {{ icon_tip }} Some examples of these can be found in the [AB3 Developer Guide]({{ ab3_website }}/DeveloperGuide.html#product-scope).

  * **Target user profile**, **value proposition**, and <trigger trigger="click" for="modal:v10-userstories">**user stories**</trigger>: Update the target user profile and value proposition to match the project direction you have selected. Give a list of the user stories (and update/delete existing ones, if applicable), including priorities. This can include user stories considered but will not be included in the final product.
  * <trigger trigger="click" for="modal:v10-usecases">**Use cases**</trigger>: Give use cases (textual form) for a few representative user stories that need multiple steps to complete. %%e.g. Adding a tag to a person (assume the user needs to find the person first)%%
  * <trigger trigger="click" for="modal:v10-nfr">**Non-functional requirements**</trigger>:
    Note: Many of the given project constraints can be considered NFRs. You can add more. e.g. performance requirements, usability requirements, scalability requirements, etc.
  * <trigger trigger="click" for="modal:v10-glossary">**Glossary**</trigger>: Define terms that are worth recording.
  *  [Optional] <trigger trigger="click" for="modal:v10-prodsurveys">**Product survey**</trigger>: Explore a few similar/related products and describe your findings i.e. Pros, cons, (from the target user's point of view).

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

#### {{ thumb(4) }} {{ icon_team }} Wrap up v1.1

* After all changes that _can_ be merged before the milestone deadline have been merged, use `git tag` feature to tag the current version with the milestone `v1.1` and push the tag to the team repo.


#### {{ thumb(5) }} {{ icon_team }} {{ icon_individual }} Draft a rough project plan

* {{ icon_team }} **Decide which enhancements each member will do by v1.4.** %%We realize that it will be hard for you to estimate the effort required for each feature as you are not very familiar with the code base yet. Nevertheless, come up with a project plan as per your best estimate; this plan can be revised at later stages. It is better to start with _some_ plan rather than no plan at all. If in doubt, choose to do _less_ than _more_; we don't expect you to deliver a lot of big features anyway.%%
* {{ icon_individual }} **Divide each of those features into two increments**, to be released at v1.2, v1.3 (v1.4 omitted deliberately as a buffer). ==Each increment should deliver a end-user visible enhancement.==
  ```
  * Jake Woo: Profile photo feature
    * v1.2: show a place holder for photo, showing a generic default image
    * v1.3: can specify photo location if it is in local hard disk,
            show photo from local hard disk
  ```

* {{ icon_individual }} **Reflect the above plan in the issue tracker** by assigning the corresponding issues (create new issues if necessary) to yourself and to the corresponding milestone. %%For example, the user story pertaining to the increment `show a place holder for photo, showing a generic default image` should be assigned to Jake and to milestone `v1.2`%%

#### {{ thumb(6) }} {{ icon_individual }} start implementing a minimal version of your feature

* While we do not _require_ you to do functionality changes in v1.1, if you have time, start implementing the version of your feature to be delivered in v1.2. We recommend that you break your v1.2 feature down to even smaller increments.


</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w07-v11", show_main_text) }}