<div id="title">

## Project → mid-v1.2 [week 8]
</div>
<div id="body">

Given below are some recommended progress for you to achieve in the various aspects of the project.

<div id="product">

**Project Management:**

* :busts_in_silhouette: Fix any errors in org/repo set up %%&nbsp;(e.g. wrong repo name)%%.

* Set up [auto-publishing of docs](https://nus-cs2103-ay1718s2.github.io/addressbook-level4/UsingTravis.html#enabling-auto-publishing-of-documentation)

* **If tests are causing too much pain ...**

  Automated tests have benefits, but they can be a pain to write/maintain; GUI tests are especially hard to maintain because their behavior can sometimes depend on things such as the OS, resolution etc.
  
  It is OK to get rid of some of the troublesome tests and rely more on manual testing instead. The less automated test coverage you have, the higher the risk of regressions; but it may be an acceptable trade-off under the circumstances if tests are slowing you down too much. There is no direct penalty for removing GUI tests.
  
  Also note <trigger trigger="click" for="modal:v12-testingExpectations">our expectation on test code</trigger>. 

<modal title="Admin {{ icon_embedding }} Project Asessement → Expectation on testing" id="modal:v12-testingExpectations">
  <include src="project-testing.md#expectations"/>
</modal>

**Product:**

* Each member should try to add some enhancements that are in line with the vision for v2.0. Preferably, these enhancements ==should go beyond the component you are in charge of==, touching as many other components as possible. Refer to the AddressBook-Level4 Developer Guide has [some guidance on how to implement a new feature end-to-end](https://nus-cs2103-ay1718s2.github.io/addressbook-level4/DeveloperGuide.html#creating-a-new-command-code-remark-code).

</div>
<div id="documentation">

**Documentation:** Update the following pages in your project repo:  

* **User Guide**:  
    Update the user guide to describe what the product would be like when it is at 2.0.  Mark features not implemented yet as `Coming in v2.0`. You may use UI mockups where necessary. 

  <tip-box> 
  
  :bulb: It is highly recommended that you **divide documentation work (in the User Guide and the Developer Guide) among team members based on enhancements/features each person would be adding** %%&nbsp;e.g., If you are the person planing to add a feature X, you should be the person to describe the feature X in the User Guide and in the Developer Guide%%. For features that are not planned to be implemented by v1.4, you can divide them based on who will be implementing them _if_ the project were to continue until v2.0 (hypothetically).
  
  %%Reason: In the final project evaluation your documentation skills will be graded based on sections of the User/Developer Guide you have written.%%
    
  </tip-box>

* **About Us page**:  
  This page is used for module admin purposes. ==Please follow the format closely to avoid penalties==. 
  * Replace info of SE-EDU developers with info of your team, including a ==suitable photo== as described <trigger trigger="click" for="modal:mid-v12-photo">here</trigger>.  
  * Including the name/photo of the supervisor/lecturer is optional. 
  * The photo of a team member should be `doc/images/githbub_username_in_lower_case.png` %%e.g. `docs/images/damithc.png`%%.

<modal large title="Admin {{ icon_embedding }} Choosing a profile photo" id="modal:mid-v12-photo">
  <include src="profilePhoto.md"/>
</modal>

  * Indicate the different roles played and responsibilities held by each team member. You can reassign these roles and responsibilities later in the project, if necessary.  

<div class="indented-twice">

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
  * _In charge of[Component XYZ]_: %%e.g. In charge of `Model`, `UI`, `Storage`, etc.%% If you are in charge of a component, you are expected to know that component well, and review changes done to that component in v1.3-v1.4.

  You may define additional roles.

  Please make sure each of the important roles are assigned to one person in the team. It is OK to have a 'backup' for each role, but **for each aspect there should be one person who is unequivocally the person responsible for it**.
    
</panel><p/>
</div>

* **README.adoc** page: Update it to match your project. 
  * Add a UI mockup of your intended final product.   
    Note that the ==image of the UI should be `docs/images/Ui.png`== so that it can be downloaded by our scripts.  
  * The original `README.adoc` file (which doubles as the landing page of your project website) is written to read like the introduction to an SE learning/teaching resource. You should ==restructure this page to look like the home page of a real product== (not a school project) targeting real users %%&nbsp;e.g. remove references to addressbook-level3, Learning Outcomes etc. mention target users, add a marketing blurb etc.%% On a related note, also remove `Learning Outcomes` link and related pages.
  * Acknowledge the original source of the code i.e. AddressBook-Level4 project created by SE-EDU initiative at `https://github.com/se-edu/`

</div>

</div>