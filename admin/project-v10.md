<div id="documentation">

#### v1.0 Documentation

**Objective**: To analyze requirements, conceptualize the next version of the product (i.e. v2.0), and document it.

#### Step 1 : Brainstorm user stories

<img src="{{baseUrl}}/admin/images/v00.png" width="250px">

Get together with your team members and brainstorm user stories **for the v2.0 of the product**. Note that in the project you will deliver only up to v1.5 but here you should consider up to v2.0 (i.e. beyond the module).

* It is ok to have more user stories than you can deliver in the project. %%Aim to create at least 30 user stories. Include all 'obvious' ones you can think of but also look for 'non obvious' ones that you think are likely to be missed by other teams.%%

* You can write each user story in a piece of paper (e.g. yellow sticky note, index card, or just pieces of paper about the size of a playing card). Alternatively you can use an online tool (some examples given below).

<tabs> 
  <tab header="GitHub Project Boards">

You can create issues for each of the user stories and use a GitHub _Project Board_ to sort them into categories.

:package: Example Project Board:

<img src="{{baseUrl}}/admin/images/userStoriesInGitHubProjectBoards.png" width="800" /><p/>

:package: Example Issue to represent a user story:

<img src="{{baseUrl}}/admin/images/userStoryAsGitHubIssue.png" width="800" /><p/>

A video on GitHub Project Boards:

@[youtube](C6MGKHkNtxU)

  <hr></tab>
  <tab header="Google Sheets">

:package: Example Google Sheet for recording user stories:

<img src="{{baseUrl}}/admin/images/userStoriesInGoogleSheets.png" width="800" /><p/>

  <hr></tab>  
  <tab header="Trello">

:package: Example [Trello](https://trello.com) Board for recording user stories:

<img src="{{baseUrl}}/admin/images/userStoriesInTrello.png" width="800" /><p/>

  <hr></tab>

</tabs>

* Note that ==you should not 'evaluate' the value of user stories while doing the above==. An important aspect of brainstorming is not judging the ideas generated. 

<include name="%%Textbook &raquo; Gathering Requirements &rarr; Brainstorming%%" src="../book/gatheringRequirements/brainstorming/full.md" dynamic /> 
<include name="%%Textbook &raquo; Specifying Requirements &rarr; UserStories &rarr; Introduction%%" src="../book/specifyingRequirements/userStories/introduction/full.md" dynamic /> 

<panel header="%%:package: User Story examples (from a different product)%%">

`As a user I can add a task by specifying a task description only, so that I can record tasks that need to be done ‘some day’.`  
`As a user I can find upcoming tasks, so that I can decide what needs to be done soon.`  
`As a user I can delete a task, so that I can get rid of tasks that I no longer care to track.`  
`As a new user I can view more information about a particular command, so that I can learn how to use various commands.`  
`As an advanced user I can use shorter versions of a command, so that type a command faster.`  

</panel>

#### Step 2: Prioritize the user stories

<img src="{{baseUrl}}/admin/images/userstories.png" width="250px">

Suggested workflow:

* Take one use story at a time and get team member opinions about it.
* Based on the team consensus, put the story (i.e. the piece of paper) onto one of these three piles:

  * `Must-Have` : The product will be practically useless to the target user without this feature.
  * `Nice-To-Have` : The target user can benefit from this user story significantly but you are not certain if you'll have time to implement it.
  * `Not-Useful` : No significant benefit to the target user, or does not fit into the product vision.

* %%If using physical paper to record user stories: After all stories have been put in the above three piles, you can make a record of which stories are in the three piles.%%

<include name="%%Textbook &raquo; Specifying Requirements &rarr; UserStories &rarr; Usage &rarr; Tips%%" src="../book/specifyingRequirements/userStories/usage/full.md#usageTips" dynamic /> 


#### Step 3: Record v2.0 Requirements in the Developer Guide 

Based on your user story categorization in step 1, given project requirements, and the current state of the product, select which user stories you are likely to include in v2.0.

Update the following pages of the Developer Guide:

* **User Stories**: Give a list of the user stories, including priorities. This can include user stories considered but will not be included in the final product.
* **Use cases**: Give use cases (textual form) for a few representative user stories that need multiple steps to complete. %%e.g. Adding a tag to a person (assume the user needs to find the person first)%%   
* **Non-functional requirements**:  
  Note: Many of the project constraints mentioned above are NFRs. You can add more. e.g. performance requirements, usability requirements, scalability requirements, etc.
* **Glossary**: Define terms that are worth defining.
* **Product survey** [Optional]: Explore a few similar/related products and describe your findings i.e. Pros, cons, (from the target user's point of view). 

<include name="%%Textbook &raquo; Specifying Requirements &rarr; Use Cases%%" src="../book/specifyingRequirements/useCases/index.md#main" dynamic /> 
<include name="%%Textbook &raquo; Requirements &rarr; Non Functional Requirements%%" src="../book/requirements/nonFunctionalRequirements/full.md" dynamic /> 
<include name="%%Textbook &raquo; Specifying Requirements &rarr; Glossary%%" src="../book/specifyingRequirements/glossary/what/full.md" dynamic /> 
<include name="%%Textbook &raquo; Gathering Requirements &rarr; Product Surveys%%" src="../book/gatheringRequirements/productSurveys/full.md" dynamic /><p/>

**Suggested length**: Follow the existing user guide and developer guides in terms of the level of details.

**Submission**: 

1. One team member: Set up the team org and team repo for your phase B team if you haven't done that already.

<include src="appendixE-gitHub.md#organization-setup" name="%%Admin &raquo; Appendix E: Using GitHub Project Hosting &rarr; Organization Setup%%" dynamic />
<include src="appendixE-gitHub.md#repo-setup" name="%%Admin &raquo; Appendix E: Using GitHub Project Hosting &rarr; Repo Setup%%" dynamic />
 
2. Divide among yourselves who will update which parts of the Developer guide.
3. Update the team repo. Recommended: follow the forking workflow.

<include src="../book/revisionControl/forkingWorkflow/full.md" name="%%TextBook &raquo; Revision Control &rarr; Forking Workflow%%" dynamic />

**Grading**: ==Reaching this milestone (and future milestones) will be counted under 'Project management' component of the final project grade.== 
To claim this milestone as 'reached', you should at least have a full draft version of the above documents in some format (e.g. GoogleDoc), even if you did not have time to update the documents in the repo.

</div>
<div id="product">

### v1.0 Product

**Objective**: To familiarize yourself with the code.

**Description**: Divide the <tooltip content="components as stated in the [Developer Guide: Architecture]">components</tooltip> among yourselves. Each member can do some small enhancements to their component(s) to learn the code of that component. Some suggested enhancements are given in the [AddressBook-Level4 developer guide](https://nus-cs2103-AY1718S1.github.io/addressbook-level4/DeveloperGuide.html#improving-each-component).


**Submission**: Create PRs from your own fork to your team repo. 

**Grading**: This is an individual milestone. Considered reached if you have at least attempted to enhance the code of a component, even if you did not fully succeed.

</div>