<tip-box type="important"> 
  
Before you do any coding for the project, please ensure you have set the Git username correctly (see panel below for more details) in all Computers you use for coding.

<panel header="%%Admin » Appendix E → Setting Git Username to Match GitHub Username%%">
  <include src="appendixE-gitHub.md#git-username" />
</panel>

</tip-box>

<tip-box> 

**v1.0 Summary of Milestone**

Here is a summary of items you need to deliver to _reach_ v1.0 individual (:bust_in_silhouette:) and team (:busts_in_silhouette:) milestones. See sections below for more details of each item. 

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
:bust_in_silhouette: Have done some enhancement to the code | at least attempted to enhance the code of a component, even if you did not fully succeed
:busts_in_silhouette: Team org/repo set up | as stated
:busts_in_silhouette: All project documents updated as required | at least have a full draft version of the required document updates in some format (e.g. GoogleDoc), even if you did not have time to update the documents in the repo

:exclamation: ==Reaching weekly individual and team milestones are considered for grading== the _project management_ component of your project grade (expand the panel below for more info).

<panel type="seamless" header="%%Admin » Project Assessment → Project Management%%">
  <include src="project-assessment.md#project-management-grading" />
</panel>

</tip-box>

<div id="documentation">

#### v1.0 Documentation

**Objective**: To analyze requirements, conceptualize the next version of the product (i.e. v2.0), and document it.

#### Step 1 : Decide project direction, target user profile, and problem addressed

Discuss with your team members and decide your project direction, target user profile, and the value proposition of the product, as described in <trigger trigger="click" for="modal:v10-scope">[Admin » Project Scope]</trigger> 

<modal large title="Admin » Project Scope (Extract)" id="modal:v10-scope">
  <include src="project-scope.md#project-direction"/>
</modal>

#### Step 2 : Brainstorm user stories

<img src="{{baseUrl}}/admin/images/v00.png" width="250px">

Get together with your team members and <trigger trigger="click" for="modal:v10-brainstorming">brainstorm</trigger> for <trigger trigger="click" for="modal:v10-userstories">user stories</trigger> **&nbsp;for the v2.0 of the product**. Note that in the module project you will deliver only up to v1.5 but here you should consider up to v2.0 (i.e. beyond the module).

* It is ok to have more user stories than you can deliver in the project. %%Aim to create at least 30 user stories. Include all 'obvious' ones you can think of but also look for 'non obvious' ones that you think are likely to be missed by other teams.%%

* Refer <trigger trigger="click" for="modal:v10-userstoryusagetips">[Textbook » Specifying Requirements → UserStories →  Usage → (section) Tips]</trigger> for tips on how to use user stories in this task.

* You can write each user story in a piece of paper (e.g. yellow sticky note, index card, or just pieces of paper about the size of a playing card). Alternatively you can use an online tool (some examples given in <trigger trigger="click" for="modal:v10-onlinetools">[Textbook » Specifying Requirements → UserStories → Usage → (panel) Tool Examples ]</trigger>).<br>
  
* Note that ==you should not 'evaluate' the value of user stories while doing the above==. %%&nbsp;Reason: an important aspect of brainstorming is not judging the ideas generated.%%  

<modal large title="Textbook »" id="modal:v10-brainstorming">
  <include src="../book/gatheringRequirements/brainstorming/full.md"/>
</modal>

<modal large title="Textbook »" id="modal:v10-userstories">
  <include src="../book/specifyingRequirements/userStories/introduction/full.md"/>
</modal> 

<modal large title="Textbook » Specifying Requirements → UserStories → Usage → (panel)Tool Examples" id="modal:v10-onlinetools">
  <include src="../book/specifyingRequirements/userStories/usage/tools.md"/>
</modal>

<modal large title="Textbook » Specifying Requirements → UserStories →  Usage → (section) Tips" id="modal:v10-userstoryusagetips">
  <include src="../book/specifyingRequirements/userStories/usage/text.md#usageTips"/>
</modal>

<panel header="%%:package: User Story examples (from a different product)%%">

`As a user I can add a task by specifying a task description only, so that I can record tasks that need to be done ‘some day’.`  
`As a user I can find upcoming tasks, so that I can decide what needs to be done soon.`  
`As a user I can delete a task, so that I can get rid of tasks that I no longer care to track.`  
`As a new user I can view more information about a particular command, so that I can learn how to use various commands.`  
`As an advanced user I can use shorter versions of a command, so that type a command faster.`  

</panel>

#### Step 3: Prioritize the user stories

<img src="{{baseUrl}}/admin/images/userstories.png" width="250px">

Suggested workflow:

* Take one user story at a time and get team member opinions about it.
* Based on the team consensus, put the story (i.e. the piece of paper) onto one of these three piles:

  * `Must-Have` : The product will be practically useless to the target user without this feature.
  * `Nice-To-Have` : The target user can benefit from this user story significantly but you are not certain if you'll have time to implement it.
  * `Not-Useful` : No significant benefit to the target user, or does not fit into the product vision.

* %%If using physical paper to record user stories: After all stories have been put in the above three piles, you can make a record of which stories are in the three piles.%%


#### Step 4: Record v2.0 Requirements in the Developer Guide 

Based on your user story categorization in step 1, given project requirements, and the current state of the product, select which user stories you are likely to include in v2.0.

Update the following pages of the Developer Guide:

* **Target user profile**, **value proposition**, and <trigger trigger="click" for="modal:v10-userstories">**user stories**</trigger>: Update the target user profile and value proposition to match the project direction you have selected. Give a list of the user stories (and update/delete existing ones, if applicable), including priorities. This can include user stories considered but will not be included in the final product.
* <trigger trigger="click" for="modal:v10-usecases">**Use cases**</trigger>: Give use cases (textual form) for a few representative user stories that need multiple steps to complete. %%e.g. Adding a tag to a person (assume the user needs to find the person first)%%   
* <trigger trigger="click" for="modal:v10-nfr">**Non-functional requirements**</trigger>:  
  Note: Many of the project constraints mentioned above are NFRs. You can add more. e.g. performance requirements, usability requirements, scalability requirements, etc.
* <trigger trigger="click" for="modal:v10-glossary">**Glossary**</trigger>: Define terms that are worth defining.
*  [Optional]<trigger trigger="click" for="modal:v10-prodsurveys">**Product survey**</trigger>: Explore a few similar/related products and describe your findings i.e. Pros, cons, (from the target user's point of view). 

<modal large title="Textbook » Specifying Requirements → Use Cases" id="modal:v10-usecases">
  <include src="../book/specifyingRequirements/useCases/index.md#main"/>
</modal>

<modal large title="Textbook »" id="modal:v10-nfr">
  <include src="../book/requirements/nonFunctionalRequirements/full.md"/>
</modal>

<modal title="Textbook »" id="modal:v10-glossary">
  <include src="../book/specifyingRequirements/glossary/what/full.md"/>
</modal>

<modal title="Textbook »" id="modal:v10-prodsurveys">
  <include src="../book/gatheringRequirements/productSurveys/full.md"/>
</modal>


**Suggested length**: Follow the existing user guide and developer guides in terms of the level of details.

**Submission**: 

1. One team member: <trigger trigger="click" for="modal:v10-setuporg">Set up the team org</trigger> and <trigger trigger="click" for="modal:v10-setuprepo">team repo</trigger> for your phase B team if you haven't done that already.

<modal large title="Admin » Appendix E: Using GitHub Project Hosting → Organization Setup" id="modal:v10-setuporg">
  <include src="appendixE-gitHub.md#organization-setup"/>
</modal>

<modal large title="Admin » Appendix E: Using GitHub Project Hosting → Repo Setup" id="modal:v10-setuprepo">
  <include src="appendixE-gitHub.md#repo-setup"/>
</modal>

2. Divide among yourselves who will update which parts of the Developer guide.
3. Update the team repo. Recommended: follow the <trigger trigger="click" for="modal:v10-forkingworkflow">forking workflow</trigger>.

<modal large title="TextBook »" id="modal:v10-forkingworkflow">
  <include src="../book/revisionControl/forkingWorkflow/full.md"/>
</modal>

4. One member: create a PR from your ==team repo `master` branch== to [[nus-cs2103-AY1718S2/addressbook-level4](https://github.com/nus-cs2103-AY1718S2/addressbook-level4)] `master` branch. PR name: `[v1.x][Team ID] Product Name` e.g., `[v1.x][T09-B2] Contact List Pro`. %%&nbsp;As you merge code to your team repo's `master` branch, this PR will auto-update to reflect how much your team's product has progressed (that's why we use `v1.x` instead of `v1.0` in the PR title).%% In the PR description <tooltip content="use @githubUserName">mention</tooltip> the other team members so that they get notified when the tutor adds comments to the PR.

</div>
<div id="product">

### v1.0 Product

**Objective**: To familiarize yourself with at least one component the code.

**Description**: Divide the <tooltip content="components as stated in the [Developer Guide: Architecture]">components</tooltip> among yourselves. Each member can do some small enhancements to their component(s) to learn the code of that component. Some suggested enhancements are given in the [AddressBook-Level4 developer guide](https://nus-cs2103-AY1718S2.github.io/addressbook-level4/DeveloperGuide.html#improving-each-component).

:exclamation: Before you start coding, please read our reuse policy given below, in particular, ==how to give credit when you reuse code from Internet or classmates==:

<panel type="seamless" header="%%Admin » Appendix B: Policies → Policy on Reuse%%">
  <include src="appendixB-policies.md#policy-reuse" />
</panel><p/>

**Submission**: Create PRs from your own fork to your team repo. Get it merged by following your team's workflow.

</div>