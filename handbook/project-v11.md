### v1.1 Product

<img src="{{baseUrl}}/handbook/images/v01demo.png" width="125px"><br/>

%%[An early version of the mobile phone]%%

**Objective**: Move the product from v1.0 towards v2.0 in a small incremental step.

**Description**: 
* Each member should try to add some enhancements that is in line with the vision for v2.0. Create a PR for the enhancement. 
* Note that the enhancement may go beyond the component you are in charge of. Refer to the AddressBook-Level4 Developer Guide for suggested features implementing of which can help you learn how to implement a feature end-to-end.

<tip-box type="important">

**You are required to divide work based on features rather than component**

 * Each team member should implement 1 or more features end-to-end, doing required changes in *all* components. The objective is to force you to learn all components of the software, instead of limiting yourself to your own components.
 * You will continue to be in charge of your own components although others will be modifying your components' code. Your new role is to help others modify code in your components (you are supposed to be the most knowledgeable about those components) and protect your components from degrading. For example, you can review others' changes to your components and suggest possible changes.
 
</tip-box>

**Submission**: If you manage to merge any of the PRs, do a proper release on GitHub. Do a demo of the new functionality during the tutorial.

**Grading**: Criteria to consider this milestone as reached
* Minimal :star: : At least some ongoing PRs.
* On track :star::star: : At least some PRs merged.
* Ahead :star::star::star: : Each member has merged at least one PR. 

### v1.1 Documentation

Update the following pages:  


* **User Guide**:  
    Update the user guide to describe what the product would be like when it is at 2.0.  Mark features not implemented yet as `Coming in v2.0`. You may use UI mockups where necessary.

* **About Us page**:  
  This page is used for module admin purposes. ==Please follow the format closely to avoid penalties==. 
  * Remove photos of the SE-EDU developers. 
  * Including the name/photo of the supervisor/lecturer is optional. 
  * The photo of a team member should be `doc/images/githbub_id_in_lower_case.png` %%e.g. `docs/images/damithc.png`%%.

<panel header="==Choosing a profile photo==" expandable>
  <include src="profilePhoto.md" />
</panel>

* Indicate the different roles played and responsibilities held by each team member. You can reassign these roles and responsibilities later in the project, if necessary.  

<Panel header="Roles and responsibilities" expandable>

  Roles imply aspects you are in charge of and responsible for. E.g., if you are in charge of documentation, you are the person who should allocate who should write which part, ensure the document is in right format, ensure consistency etc.  
  Here are some typical roles:

  * _Team lead_: Responsible for overall project coordination.
  * _Documentation_ (short for ‘in charge of documentation’): Responsible for the quality of various project documents.
  * _Testing_: Ensures the testing of the project is done properly and on time.
  * _Code quality_: Looks after code quality, ensures adherence to coding standards, etc.
  * _Deliverables and deadlines_: Ensure project deliverables are done on time and in the right format.
  * _Integration_: In charge of versioning of the code, maintaining the code repository, integrating various parts of the software to create a whole.
  * _Scheduling and tracking_: In charge of defining, assigning, and tracking project tasks.
  * _[Tool ABC] expert_: e.g. Eclipse expert, Git expert, etc. Helps other team member with matters related to the specific tool.
  * _In charge of[Component XYZ]_: e.g. In charge of `Model`, `UI`, `Storage`, etc. If you are in charge of a component, you are expected to know that component well, and review changes done to that component in v1.3-v1.5.
  * You may define additional roles.

Please make sure each of the above roles are assigned to one person in the team. It is OK to have a ‘backup’ for each role, but you should still have one person who is unequivocally the main person playing that role.
    
</Panel>

* **README.md** page: Update it to match your project. In particular, add a UI mockup of your intended final product.  
    Note that the ==image of the UI should be `docs/images/ui.png`== so that it can be downloaded by our scripts.  
    Also, remember to acknowledge the original source of the code i.e. AddressBook-Level4 project created by SE-EDU initiative at `https://github.com/se-edu/`

**Grading**: To consider this milestone as reached, you should have all v1.0 deliverables completed and the two documents mentioned above updated.

