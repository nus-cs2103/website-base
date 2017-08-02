#### v1.0 Documentation

**Objective**: To analyze requirements, conceptualize the next version of the product (i.e. v2.0), and document it.

#### Step 1 : Brainstorm user stories

<img src="{{baseUrl}}/admin/images/v00.png" width="250px">

Get together with your team members and brainstorm user stories **for the v2.0 of the product**. Note that in the project you will deliver only up to v1.5 but here you should consider up to v2.0 (i.e. beyond the module).

<panel header="%%User Story examples (from a different product)%%">

`As a user I can add a task by specifying a task description only, so that I can record tasks that need to be done ‘some day’.`  
`As a user I can find upcoming tasks, so that I can decide what needs to be done soon.`  
`As a user I can delete a task, so that I can get rid of tasks that I no longer care to track.`  
`As a new user I can view more information about a particular command, so that I can learn how to use various commands.`  
`As an advanced user I can use shorter versions of a command, so that type a command faster.`  

</panel>

* It is ok to have more user stories than you can deliver in the project.You should have at least 30 user stories. Include all 'obvious' ones you can think of but also look for 'non obvious' ones that you think are likely to be missed by other teams.
* Write each use story in a piece of paper (e.g. yellow sticky note, index card, or just pieces of paper about the size of a playing card). Alternatively you can use an online tool such as Trello for recording the initial collection of user stories.
* Note that ==you should not 'evaluate' the value of user stories while doing the above==. An important aspect of brainstorming is not judging the ideas generated.  

#### Step 2: Prioritize the user stories

<img src="{{baseUrl}}/admin/images/userstories.png" width="250px">

Suggested workflow:

* Take one use story at a time and get team member opinions about it.
* Based on the team consensus, put the story (i.e. the piece of paper) onto one of these three piles:

  * `Must-Have` : The product will be practically useless without this feature.
  * `Nice-To-Have` : The target user can benefit from this user story significantly but you are not certain if you'll have time to implement it.
  * `Not-Useful` : No significant benefit to the target use.

* After all stories have been put in the above three piles, you can make a record of which stories are in the three piles.

Here are some tips to improve the effectiveness of the above activity:

* **Define the target user:**  
  Decide our target user's profile (e.g. a student, office worker, programmer, sales person) and work patterns (e.g. Does he work in groups or alone? Does he share his computer with others?). A clear understanding of the target user will help when deciding the importance of a user story.
* **Don't be biased by the implementation plans:**  
    This exercise is for identifying user needs. Clear your mind of ideas you have about what your end product will look like. 
* **Don't discuss implementation details or whether you are actually going to implement it:**  
  At this point, your decision is whether the user's need is important enough for you to want to fulfil it. Implementation details can be discussed later. If a user story in the Nice-To-Have pile turn out to be too difficult to implement later, you can always not implement it.
* **Don't be too hasty to discard 'unusual' user stories:**  
  Those might make your product unique and stand out from the rest, at least for some potential users.
* **Don't go into too much details when sorting user stories:**  
  For example, consider this user story:  
  * `As a user, I want to see a list of tasks that needs my attention most at the present time, so that I pay attention to them first.`  
  When discussing this user story, you do not need to worry about what tasks should be considered 'needs my attention most at the present time'. Those details can be worked out later.


#### Step 3: Record v2.0 Requirements in the Developer Guide 

Based on your user story categorization in step 1, given project requirements, and the current state of the product, select which user stories you are likely to include in v2.0.

Update the following pages of the Developer Guide:

* **User Stories**: Give a list of the user stories, including priorities. This can include user stories considered but will not be included in the final product.
* **Use cases**: Give use cases (textual form) for a few representative user stories that need multiple steps to complete. e.g.
  * Adding a tag to a person (assume the user needs to find the person first).   
* **Non-functional requirements**:  
  Note: Many of the project constraints mentioned above are NFRs. You can add more. e.g. performance requirements, usability requirements, scalability requirements, etc.
* **Glossary**: Define terms that are worth defining.
* **Product survey** [Optional]: Explore a few similar/related products and describe your findings i.e. Pros, cons, (from the target user's point of view). 

**Suggested length**: Follow the existing user guide and developer guides in terms of the level of details.

**Submission**: Update the relevant sections of the relevant asciidoc documents in your repo. 

**Grading**: Reaching this milestone (and future milestones) will be counted under 'Project management' component of the final project grade.  
To claim this milestone as 'reached', you should at least have a full draft version of the above documents in some format (e.g. GoogleDoc), even if you did not have time to update the documents in the repo.

### v1.0 Product

**Objective**: To familiarize yourself with the code.

**Description**: Divide the component among yourselves. Each member can do some small enhancements to the component they are in charge of to learn the code of that component. Some suggested enhancements are given in the AddressBook-Level4 developer guide.


**Submission**: Create PRs from your own fork to your team repo. 

**Grading**: This is an individual milestone. Considered reached if you have at least attempted to enhance the code of a component, even if you did not fully succeed.
