The objective of this deliverable is for you to analyze requirements, conceptualize the product, and document it.

### Step 1 : Brainstorm user stories

<img src="images/v00.png" width="250px">

Get together with your team members and brainstorm user stories for the product.

*   e.g.  
    `As a user I can add a task by specifying a task description only, so that I can record tasks that need to be done ‘some day’.`  
    `As a user I can find upcoming tasks, so that I can decide what needs to be done soon.`  
    `As a user I can delete a task, so that I can get rid of tasks that I no longer care to track.`  
    `As a new user I can view more information about a particular command, so that I can learn how to use various commands.`  
    `As an advanced user I can use shorter versions of a command, so that type a command faster.`  
    Note how the story covers who (the user), what (the functionality) and why (the value) aspects.
*   It is ok to have more user stories than you can deliver in the project.You should have at least 30 user stories. Include all 'obvious' ones you can think of but also look for 'non obvious' ones that you think are likely to be missed by other teams.
*   Write each use story in a piece of paper (e.g. yellow sticky note, index card, or just pieces of paper about the size of a playing card). Alternatively you can use an online tool such as Trello for recording the initial collection of user stories.
*   Note that ==you should not 'evaluate' the value of user stories while doing the above==. An important aspect of brainstorming is not judging the ideas generated.  

### Step 2: Prioritize the user stories

<img src="images/userstories.png" width="250px">

Suggested workflow:

*   Take one use story at a time and get team member opinions about it.
*   Based on the team consensus, put the story (i.e. the piece of paper) onto one of these three piles:

    *   `Must-Have` : The product will be practically useless to Jim without this feature.
    *   `Nice-To-Have` : Jim can benefit from this user story significantly but you are not certain if you'll have time to implement it.
    *   `Not-Useful` : No significant benefit to Jim.

*   After all stories have been put in the above three piles, you can make a record of which stories are in the three piles.

Here are some tips to improve the effectiveness of the above activity:

*   **Define Jim:**  
    Decide our target user Jim's work patterns. e.g. Does he work in groups or alone? Does he share his computer with others? (answer: no). Having a clear picture of Jim's work patterns will help when deciding the importance of a user story.
*   **Don't be biased by the implementation plans:**  
    This exercise is for identifying user needs. Clear your mind of ideas you have about what your product will look like. Assume that you do not know yet what product you will build.
*   **Don't discuss implementation details or whether you are actually going to implement it:**  
    At this point, your decision is whether the user's need is important enough for you to want to fulfil it. Implementation details can be discussed later. If a user story in the Nice-To-Have pile turn out to be too difficult to implement later, you can always not implement it.
*   **Don't be too hasty to discard 'unusual' user stories:**  
    Those might make your product unique and stand out from the rest, at least for some potential users.
*   **Don't go into too much details when sorting user stories:**  
    For example, consider this user story:  
    * As a user, I want to see a list of tasks that needs my attention most at the present time, so that I pay attention to them first.*  
    When discussing this user story, you do not need to worry about what tasks should be considered 'needs my attention most at the present time'. Those details can be worked out later.

### Step 3: Survey existing products

See how well existing products meet Jim's needs.

*   Select a few competing products to study. Each person should study at least one existing product. Identify strengths and weaknesses of the product w.r.t. how well it can cater for Jim’s requirements.

    Here are some popular 'task manager' type products out there you can consider exploring (you are not limited to these): Google Calendar + Google Tasks | [HiTask](https://hitask.com) | [Remember The Milk](https://www.rememberthemilk.com/) | [Todo.txt](http://todotxt.com/) | [Todoist](https://todoist.com/) | [Trello](https://trello.com/) | Microsoft Outlook | [Wunderlist](https://www.wunderlist.com/)

*   **Note**: Don’t get discouraged if an existing product meets Jim’s needs quite well. We are trying to learn SE, not sell a product.
*   After looking at existing products, you may want to go back and revise some of the user stories.

### Step 4: Conceptualize the product as a user guide

*   Based on your user story categorization in step 1 and given project requirements (note that the project requirements specify some must-have features), select which user stories you are likely to include in V0.5.
*   Based on the user stories you selected above, specify the product you are going to build, in the form of a user guide. Yes, strangely enough, in this project we draft the user guide before we build the product. This will help you/us visualize the final product before you start implementing it.
*   ==Remember to take into account the UI design and the functionalities available in AddressBook Level 4==. As you will be using that software as the starting point of your implementation, it makes sense to align your product with it (within reason) to minimize the implementation effort.
*   Remember to include the exact command format because it is the core part of your UI.

Use the documentation in the sample project as an example. Given below are pages to update.

*   **User guide**:  
    Describe what the product would be like when it is submitted at the end of the semester. Starting from the time user starts using the product for the first time, describe how the user uses the product to accomplish various tasks.  
    Here are some ‘quick start guides’ you can look at for inspiration when writing your user guide:  
    [Collate project](https://github.com/se-edu/collate/blob/master/docs/User-Guide.md), [iPhone :How to get started](https://support.apple.com/en-sg/HT202033), [TEAMMATES (for instructors)](https://teammatesv4.appspot.com/instructorHelp.jsp#gs)  
    Use UI prototypes/sketches if necessary. They can be simple sketches drawn on whiteboard/paper and scanned/photographed or created using a tool such as PowerPoint, HTML, or [Balasmiq](https://balsamiq.com/).  
    State what you honestly believe you can do, based on information you have at this point. You will not be penalized if you cannot deliver what you proposed to deliver. It is OK to tweak the project scope along the way.  
    ==Specify the command format in detail== as it is an important part of the product functionality.  

*   **Developer guide**: Update the following appendices.
    *   **User Stories**: Give a list of the user stories, including priorities. This can include user stories considered but will not be included in the final product.
    *   **Use cases**: Give use cases (textual form) for a few representative user stories that need multiple steps to complete. e.g.
        *   Rescheduling a task, which may require two steps: locating the task first and then updating it.
        *   Checking a day's schedule at the end of the day: requires filtering the day's tasks, marking complete tasks as done, and rescheduling or deleting remaining tasks.
        *   Finding something to do where here is a free time.
    *   **Non-functional requirements**:  
        Note: User stories capture functional requirements. What are the non-functional requirements of your project? Many of the project constraints mentioned above are NFRs. You can add more. e.g. performance requirements, usability requirements, scalability requirements, etc.
    *   **Glossary**: Define terms that are worth defining.
    *   **Product survey**: Describe a summary of the product survey. i.e. Pros, cons, (from Jim's point of view). Each student should document the product they explored. If multiple students have explored the same product, you may have to explore more products to complete this section.

**Suggested length**: Take the sample project as a baseline.

**Submission**: Update the relevant sections of the relevant markdown documents (i.e. `UserGuide.md, DeveloperGuide.md`) in your repo. [git tag](http://git-scm.com/book/en/v2/Git-Basics-Tagging) as `V0.0`.

**Grading**: Reaching this milestone (and future milestones) will be counted under 'Project management' component of the final project grade.  
To claim this milestone as 'reached', you should at least have a full draft version of the above documents in some format (e.g. GoogleDoc), even if you didn't have time to update the markdown documents in the repo.