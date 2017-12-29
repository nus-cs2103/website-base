<tip-box> 

**v1.1 Summary of Milestone**

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
:bust_in_silhouette: Have modified in multiple components | Minimal : Your enhancement touches components other than the ones you modified in v1.0 and you are able to demo it using your own computer <br> On track : In addition, you have created a PR for the enhancement, it covers tests and documentation updates for the new feature, and the PR passes Travis checks<br> Ahead : Your PR has been reviewed and merged.
:busts_in_silhouette: All project documents updated as required | At least there is a PR containing all required changes
:busts_in_silhouette: v1.0 document updates are merged | as stated
:busts_in_silhouette: Any errors in org/repo set up fixed %%&nbsp;(e.g. wrong repo name)%%.<br>[Auto-publishing of docs](https://nus-cs2103-ay1718s2.github.io/addressbook-level4/UsingTravis.html#enabling-auto-publishing-of-documentation) is set up and working | as stated

</tip-box>

<div id="product">

### v1.1 Product

<img src="{{baseUrl}}/admin/images/v01demo.png" width="125px"><br/>

%%[An early version of the mobile phone]%%

**Objective**: Move the product from v1.0 towards v2.0 in a small incremental step.

**Description**: 
* Each member should add some enhancements that are in line with the vision for v2.0. We recommend this to be your <trigger trigger="click" for="modal:v11-individual-expectations">_minor enhancement_</trigger>, but it can also be an initial step in your _major enhancement_.
 
<modal title="" id="modal:v11-individual-expectations">
  <include src="project-scope.md#individual-expectations"/>
</modal>

* These enhancements ==should go beyond the component you are in charge of==, touching as many other components as possible. Refer to the AddressBook-Level4 Developer Guide has [some guidance on how to implement a new feature end-to-end](https://nus-cs2103-ay1718s2.github.io/addressbook-level4/DeveloperGuide.html#creating-a-new-command-code-remark-code).

**Submission**: Demo of the new functionality during the tutorial.

</div>
<div id="documentation">

### v1.1 Documentation

Update the following pages:  


* **User Guide**:  
    Update the user guide to describe what the product would be like when it is at 2.0.  Mark features not implemented yet as `Coming in v2.0`. You may use UI mockups where necessary. 

<tip-box> 

:bulb: It is highly recommended that you **divide documentation work (in the User Guide and the Developer Guide) among team members based on enhancements/features each person would be adding** %%&nbsp;e.g., If you are the person planing to add a feature X, you should be the person to describe the feature X in the User Guide and in the Developer Guide%%. For features that are not planned to be implemented by v1.5, you can divide them based on who will be implementing them _if_ the project were to continue until v2.0 (hypothetically).

%%Reason: In the final project evaluation your documentation skills will be graded based on sections of the User/Developer Guide you have written.%%
  
</tip-box>

* **About Us page**:  
  This page is used for module admin purposes. ==Please follow the format closely to avoid penalties==. 
  * Replace info of SE-EDU developers with info of your team, including a ==suitable photo== as described <trigger trigger="click" for="modal:v11-photo">here</trigger>.  
  * Including the name/photo of the supervisor/lecturer is optional. 
  * The photo of a team member should be `doc/images/githbub_username_in_lower_case.png` %%e.g. `docs/images/damithc.png`%%.

<modal large title="Admin » Choosing a profile photo" id="modal:v11-photo">
  <include src="profilePhoto.md"/>
</modal>

* Indicate the different roles played and responsibilities held by each team member. You can reassign these roles and responsibilities later in the project, if necessary.  

<panel header="More info on _roles and responsibilities_">

  **Roles indicate aspects you are in charge of and responsible for.** %%E.g., if you are in charge of documentation, you are the person who should allocate which parts of the documentation is to be done by who, ensure the document is in right format, ensure consistency etc.%%  
  
  Here are some example roles:

  * _Team lead_: Responsible for overall project coordination.
  * _Documentation_ (short for ‘in charge of documentation’): Responsible for the quality of various project documents.
  * _Testing_: Ensures the testing of the project is done properly and on time.
  * _Code quality_: Looks after code quality, ensures adherence to coding standards, etc.
  * _Deliverables and deadlines_: Ensure project deliverables are done on time and in the right format.
  * _Integration_: In charge of versioning of the code, maintaining the code repository, integrating various parts of the software to create a whole.
  * _Scheduling and tracking_: In charge of defining, assigning, and tracking project tasks.
  * _[Tool ABC] expert_: %%e.g. Intellij expert, Git expert, etc.%% Helps other team member with matters related to the specific tool.
  * _In charge of[Component XYZ]_: %%e.g. In charge of `Model`, `UI`, `Storage`, etc.%% If you are in charge of a component, you are expected to know that component well, and review changes done to that component in v1.3-v1.5.

  You may define additional roles.

  Please make sure each of the important roles are assigned to one person in the team. It is OK to have a 'backup' for each role, but **for each aspect there should be one person who is unequivocally the person responsible for it**.
    
</panel><p/>

* **README.adoc** page: Update it to match your project. 
  * Add a UI mockup of your intended final product.   
    Note that the ==image of the UI should be `docs/images/Ui.png`== so that it can be downloaded by our scripts.  
  * The original `README.adoc` file (which doubles as the landing page of your project website) is written to read like the introduction to an SE learning/teaching resource. You should ==restructure this page to look like the home page of a real product== (not a school project) targeting real users %%&nbsp;e.g. remove references to addressbook-level3, Learning Outcomes etc. mention target users, add a marketing blurb etc.%% On a related note, also remove `Learning Outcomes` link and related pages.
  * Acknowledge the original source of the code i.e. AddressBook-Level4 project created by SE-EDU initiative at `https://github.com/se-edu/`

</div>