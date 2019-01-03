{% macro show_main_text() %}
<div id="main">

<span class="keyword d-none">project expectations</span>

#### Project Direction

<div id="project-direction">
In general, each team is expected to take one of these two directions:

* **[Direction 1]  _Optimize_** AddressBook for a more specific target user group:
   
  <panel type="seamless" header="%%{{ icon_example }} Examples for the _optimize_ direction%%">
     
  An AddressBook,
     * for users in a specific profession %%&nbsp;e.g. doctors, salesmen, teachers, etc.%%
     * based on the nature/scale of contacts %%&nbsp;e.g. huge number of contacts (for HR admins, user group admins), mostly incomplete contacts, highly volatile contact details, contacts become inactive after a specific period (e.g. contract employees)%%
     * based on what users do with the contacts %%&nbsp;e.g. organize group events, share info, do business, do analytics%%   
     
  </panel><p/>

   
* **[Direction 2] _Morph_** AddressBook into a different product: Given that AddressBook is a generic app that manages a type of elements (i.e. contacts), you can use it as a starting point to create an app that manages something else.<br>
  {{ icon_important_big_red }} This is a high-risk high-reward option because morphing requires extra work but a morphed product may earn more marks than an optimized product of similar complexity.
   
  <panel type="seamless" header="%%{{ icon_example }} Examples for the _morph_ direction%%">
     
  An app to manage, 
  * Bookmarks of websites
  * Tasks/Schedule
  * Location info
  * Thing to memorize i.e. flash cards, trivia
  * Forum posts, news feeds, Social media feeds
  * Online projects or issue trackers that the user is interested in
  * Emails, possibly from different accounts
  * Multiple types of related things %%&nbsp;e.g. Contacts and Tasks (if Tasks are allocated to Contacts)%%
     
  </panel><p/>
   
For either direction, you need to define a target user profile and a value proposition:

* **Target user profile**: Define a very specific target user profile. <br> :bulb: We require you to narrow down the target user profile %%&nbsp;as opposed to trying to make it as general as possible. Here is an example direction of narrowing down target user: anybody → teachers → university teachers → tech savvy university teachers → {{ module_pair }} instructors.%%<br><br>
 {{ icon_important_big_red }} Be careful not to contradict given [project constraints]({{ baseUrl }}/admin/project-constraints.html) when defining the user profile %%&nbsp;e.g. the target user should still prefer typing over mouse actions%%.<br><br>
  **It is expected that your product will be optimized for the chosen target users** %%i.e., add features that are especially/only applicable for target users (to make the app especially attractive to them). w.r.t. the example above, there can be features that are applicable to {{ module_pair }} instructors only, such as the ability to navigate to a student's project on GitHub%%<br>
    :bulb: Your project will be graded based on how well the features match the target user profile and how well the features fit-together.
  
  <panel type="seamless" header="%%Why the need to narrow down the user profile?%%" >
  
  * It is an opportunity to exercise your product design skills because optimizing the product to a very specific target user requires good product design skills.
  * It minimizes the overlap between features of different teams which can cause plagiarism issues. Furthermore, higher the number of other teams having the same features, less impressive your work becomes especially if others have done a better job of implementing that feature.
  </panel>
  <br>
  * **Value proposition**: Define a clear _value proposition_ %%(what problem does the product solve? how does it make the the user's life easier?)%% that matches the target user profile.

</div>
   
#### {{ icon_individual }} Individual Expectations

<span id="individual-expectations">

##### [Individual] Expectations on Features

* You are expected to add at least one feature to the product.
* ==One big feature can earn you more marks than multiple small features.== %%Reason: When grading your work for depth and completeness, only your biggest feature you will be considered.%%
* At lest one feature should be end-user visible and end-user testable. %%Reason: If your feature cannot be identified and tested by the testers, we will not be able to give marks for the quality assurance of that feature.%%
* The features should fit with the rest of the software (and the target user profile) and should have the consent of the team members.. %%You will lose marks if you go 'rogue' and add features that don't fit with the product.%%


<panel type="seamless" header="%%{{ icon_example }} Examples of suitable enhancements%%" >

1. Add a new feature
1. Enhance an existing features in a major way %%e.g. make the command syntax more user friendly and closer to natural language%%
1. A major redesign of the GUI %%e.g. make it work like a chat application (note: chat is a form of CLI)%%
1. Integrate with online services %%e.g. Google contacts, Facebook, GitHub, etc.%%

</panel>


<panel type="seamless" header="%%{{ icon_example }} Enhancement vs Grade: Examples%%">

Here are some examples of different enhancements and the grade the student is likely to earn for the relevant parts of the project grade.
* Example 1 (Expected grade: `A`) : [Add support for undo/redo](https://github.com/se-edu/addressbook-level4/pull/610/files)
* Example 2 (Expected grade: `B`) : [Add support for viewing history](https://github.com/se-edu/addressbook-level4/pull/440/files)

</panel><p/>

* Although we prefer one big feature over multiple small features, it is fine to do small features at first to build up confidence before you start a big feature.

<panel type="seamless" header="%%{{ icon_example }} Examples of minor enhancements%%">

Here is a non-exhaustive list of minor enhancements:

1. Support different themes for the Look & Feel %%&nbsp;dark, light, etc.%%
1. Support more fields %%&nbsp;e.g. Birthday%%
1. Load a different page instead of the default Google search page %%&nbsp;e.g. Google Maps page or Twitter page%%
1. Sort items
1. Multiple panels %%&nbsp;e.g. an additional panel to show recently accessed items%%
1. Marking some items as favorites
1. Ability to search by labels
1. Ability to specify colors for labels

</panel><p/>

We strongly recommend that you contribute to multiple (preferably, all) aspects of the project e.g. write backend code, frontend code, test code, user documentation, and developer documentation. If you limit yourself to certain aspects only, you will lose marks allocated for the aspects you did not do.

In particular, ==you are required to divide work based on features rather than components==:
   * By the <tooltip content="i.e. by `v1.4`">end of this project</tooltip> each team member is expected to have implemented at least one feature end-to-end, doing required changes in _almost all_ components. %%&nbsp;Reason: to encourage you to learn all components of the software, instead of limiting yourself to just one/few components%%.
   * Nevertheless, you are ==still expected to divide the components of the product among team members== so that each team member is _in charge_ of one or more components. While others will be modifying those components as necessary for the features they are implementing, your role as the _in charge_ of a component is to guide others modifying that component %%(reason: you are supposed to be the most knowledgeable about that component)%% and protect that component from degrading %%&nbsp;e.g., you can review others' changes to your component and suggest possible changes%%.

##### [Individual] Expectations on Code

* Based on past experience, ==it is possible for a feature consisting of **~300-500 LoC of code** to earn full marks== provided the feature do well in all grading criteria.

##### [Individual] Expectations on Documentation

* You are expected to write user documentation and developer documentation for your features.
* **The objective is to showcase your ability to write the two types of documentation.** If the documentation for your features is not enough to meet that objective, or does not reach the following minimal requirement, you can make up the shortfall by documenting 'proposed' features and alternative designs/implementations.
  * Contribution to the user guide: 1 page
  * Contribution to the developer guide: 3 pages
* You are expected to ==showcase your ability to use the various UML diagrams (at least 2 types)==. As mentioned in the previous point, if the documentation of your features doesn't give you enough opportunities to do so %%e.g., your features only required minor updates to existing diagrams%%, you are expected to create those opportunities yourself by documenting proposed features or alternative designs. Evaluators will not be able to give you marks unless there is sufficient evidence of your documentation skills.
* You are recommended to, but not required to, update all existing AB-4 documentation to match your product. However, all diagrams that are included in the part of documentation claimed as done by you should be updated to match the current product.

##### [Individual] Expectations on Testing

<div id="testing-expectations">

* There is no requirement for a minimum coverage level. Note that in a production environment you are often required to have at least 90% of the code covered by tests. In this project, it can be less. The less coverage you have, the higher the risk of regression bugs, which will cost marks if not fixed before the final submission.
* You ==must write _some_ tests== so that we can evaluate your ability to write tests.
* How much of each type of testing should you do? We expect you to decide. You learned different types of testing and what they try to achieve. Based on that, you should decide how much of each type is required. Similarly, you can decide to what extent you want to automate tests, depending on the benefits and the effort required.

</div>


##### [Individual] Expectations on Teamwork

_Team-tasks_ are the tasks that _someone_ in the team has to do. Marks allocated to team-tasks will be divided among team members based on how much each member contributed to those tasks.

<span id="scope-example-team-tasks"></span>

<panel type="seamless" header="%%{{ icon_example }} Examples of team-tasks%%">

<span id="example-team-tasks">

Here is a non-exhaustive list of team-tasks:

1. Necessary general code enhancements e.g.,
   1. Work related to renaming the product
   1. Work related to changing the product icon
   1. Morphing the product into a different product
1. Setting up the GitHub, Travis, AppVeyor, etc.
1. Maintaining the issue tracker
1. Release management
1. Updating user/developer docs that are not specific to a feature %%e.g. documenting the target user profile%%
1. Incorporating more useful tools/libraries/frameworks into the product or the project workflow %%(e.g. automate more aspects of the project workflow using a GitHub plugin)%%

</span>

</panel><p/>
   
<span id="roles">

_Roles_ indicate aspects you are in charge of and responsible for. %%E.g., if you are in charge of documentation, you are the person who should allocate which parts of the documentation is to be done by who, ensure the document is in right format, ensure consistency etc.%%

<panel type="seamless" header="{{ icon_example }} Recommended roles and responsibilities">

This is a non-exhaustive list; you may define additional roles.

* _Team lead_: Responsible for overall project coordination.
* _Documentation_ (short for ‘in charge of documentation’): Responsible for the quality of various project documents.
* _Testing_: Ensures the testing of the project is done properly and on time.
* _Code quality_: Looks after code quality, ensures adherence to coding standards, etc.
* _Deliverables and deadlines_: Ensure project deliverables are done on time and in the right format.
* _Integration_: In charge of versioning of the code, maintaining the code repository, integrating various parts of the software to create a whole.
* _Scheduling and tracking_: In charge of defining, assigning, and tracking project tasks.
* _[Tool ABC] expert_: %%e.g. Intellij expert, Git expert, etc.%% Helps other team member with matters related to the specific tool.
* _In charge of[Component XYZ]_: %%e.g. In charge of `Model`, `UI`, `Storage`, etc.%% If you are in charge of a component, you are expected to know that component well, and review changes done to that component in v1.3-v1.4.

</panel>
<p/>

Please make sure each of the important roles are assigned to one person in the team. It is OK to have a 'backup' for each role, but **for each aspect there should be one person who is unequivocally the person responsible for it**.
</span>

</span>
<span id="team-expectations">

#### {{ icon_team }} Team Expectations

1. **Preserve _product integrity_**: i.e. ensure,
   1. features fit together to form a cohesive product,
   1. documentation follows a consistent style and presents a cohesive picture to the reader, and
   1. final project demo presents a cohesive picture to the audience.
1. **Maintain product quality**: i.e. prevent breaking other parts of the product as it evolves. Note that bugs local to a specific feature will be counted against the author of that feature. However, if a new enhancement breaks the entire product, the whole team will have to share the penalty.
1. **Manage the project smoothly**: i.e. ensure workflow, code maintenance, integration, releases, etc. are done smoothly.

</span>


</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-scope", show_main_text) }}
