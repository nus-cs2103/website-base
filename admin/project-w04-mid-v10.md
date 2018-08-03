{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

Given below are some guidance on the recommended progress at this point of the project %%(i.e., at week 4, which is the midway point of the milestone v1.0)%%

<tip-box>

Overview: <include src="project-timeline.md#mid-v10-overview" inline />
</tip-box>

This is a good time to analyze requirements with a view to conceptualizing the next version of the product (i.e. v2.0).

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

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w04-mid-v10", show_main_text) }}