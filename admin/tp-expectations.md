{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-expectations") %}
<div id="main">

<span class="keyword d-none">project expectations</span>

### <div class="text-white bg-dark p-1">Outcomes</div>

The high-level learning outcome of the team project (tP):

<box> {{ icon_outcome }} Can contribute production quality SE work to a small/medium software project </box>

Accordingly, the tP is structured to resemble an intermediate stage of a non-trivial real-life brownfield software project in which you will,
 1. conceptualize and implement enhancements to a given product, and,
 1. have it ready to be continued by future developers

<span id="tp-direction">

### <div class="text-white bg-dark p-1">Direction</div>

The tP uses a generic application called [AddressBook-Level3 (AB3)](https://se-edu.github.io/addressbook-level3/) (from https://se-education.org) as the starting point.

<img src="https://github.com/se-edu/addressbook-level3/raw/master/docs/images/Ui.png" width="600"/>
<p/>

This product is meant for users who can type fast, and prefer typing over mouse/voice commands. Therefore, ==Command Line Interface (CLI) is the primary mode of input.== 

{{ embed_topic("tp-constraints.md#Constraint-Typing-Preferred", "Admin " + icon_embedding + " tP Contstraints → Constraint-Typing-Preferred", "2", indent="1") }}
{{ embed_topic("tp-constraints.md#Recommendation-CLI-First", "Admin " + icon_embedding + " tP Contstraints → Recommendation-CLI-First", "2", indent="1") }}
<p/>

**You may evolve/morph the <tooltip content="AddressBook-Level3">AB3</tooltip> any direction you wish.** For example, an app to manage one of these: 
* Contact details
* Bookmarks of websites
* Tasks/Schedule
* Location info
* Thing to memorize i.e. flash cards, trivia
* Forum posts, news feeds, Social media feeds
* Online projects or issue trackers that the user is interested in
* Emails, possibly from different accounts
* Multiple types of related things %%e.g. Contacts and Tasks (if Tasks are allocated to Contacts)%%
* ...
</span>

### <div class="text-white bg-dark p-1">Target User & Value Proposition</div>

You are expected to:
* **Define a very specific _target user profile_.** <br> ==We require you to narrow down the target user profile==  %%as opposed to trying to make it as general as possible. Here is an example direction of narrowing down target user: anybody → teachers → university teachers → tech savvy university teachers → {{ module_pair }} instructors.%%<br><br>
 {{ icon_important_big_red }} Be careful not to contradict given [project constraints]({{ baseUrl }}/admin/tp-constraints.html) when defining the user profile %%e.g. the target user should still prefer typing over mouse actions%%.

<div class="indented-level2">

<panel type="seamless" header="%%Why the need to narrow down the user profile?%%" >

* It is an opportunity to exercise your product design skills because optimizing the product to a very specific target user requires good product design skills.
* It minimizes the overlap between features of different teams which can cause plagiarism issues. Furthermore, higher the number of other teams having the same features, less impressive your work becomes especially if others have done a better job of implementing that feature.
</panel>
</div>

* **Define a clear _value proposition_** that matches the target user profile i.e., what problem does the product solve? how does it make the the user's life easier?
* **Optimize the product to the chosen target users** i.e., add features that are especially/only applicable for target users (to make the app especially attractive to them). 
  * Example 1: If the product targets {{ module_pair }} instructors, there can be features that are applicable to them only, %%such as the ability to navigate to a student's project on GitHub%% 
  * Example 2: If your app manages contacts, you can optimize its features based on,
    * the profession of the target user %%e.g. doctors, salesmen, teachers, etc.%%
    * the nature/scale of contacts %%e.g. huge number of contacts (for HR admins, user group admins), mostly incomplete contacts, highly volatile contact details, contacts become inactive after a specific period (e.g. contract employees)%%
    * what users do with the contacts %%e.g. organize group events, share info, do business, do analytics%%

    {{ icon_tip }} Your project will be graded based on how well the features match the target user profile and how well the features fit-together.

<span id="functionalityExpectations">

### <div class="text-white bg-danger p-1">Functionality Expectations</div>

**The expected level of _functionality_ from a 5-person team is roughly the ==equivalent effort taken to create AB3 _functionality_==**. Some examples meeting that criterion:
* Example 1: A fictional contact management app optimized for a specific target user group:
  * Existing AB3 features are optimized to the new target user group.
  * Person objects are enhanced to contain more details.
  * There are a 4-5 new functionality that are specific to the target user group.
* Example 2: a FooBar app that keeps track of two different types of entities _Foo_ entities and _Bar_ entities.
  * Foo and Bar entities are tightly-connected e.g., a Foo entity can contain Bar entities. Each type is similar to AB3 Person objects in terms of complexity.
  * In addition to <tooltip content="Creat Read Update Delete">CRUD</tooltip> for Foo and Bar entities, there are a 4-5 FooBar-specific functionality, some of which involves both Foo and Bar entities e.g., link a Foo entity to a Bar entity.

<box>

{{ icon_tip }} If you wish to add the following features to your app, we recommend (but not require) you to follow similar features in AB4 in order to reduce the effort required.
  * [Undo/redo](https://se-education.org/addressbook-level4/DeveloperGuide.html#undo-redo-feature)
  * [Automated GUI tests](https://se-education.org/addressbook-level4/Testing.html#types-of-tests)
</box>

<box type="important">

Note that we have reduced the tP functionality expectations for this semester by about 40-50% compared to the previous semester, in order to reduce your workload. ==Adding more functionality than the expected level will not increase your marks==. You are better off spending that effort in improving other aspects of the project.
</box>
</span>
<span id="teamExpectations">

### <div class="text-white bg-success p-1">{{ icon_team }} Team Expectations</div>

* <span class="badge badge-success">Expectation</span> <span class="text-success">**Preserve _product integrity_**</span> i.e. ensure,
  1. features fit together to form a cohesive product,
  1. documentation follows a consistent style and presents a cohesive picture to the reader, and
  1. final project demo presents a cohesive picture to the audience.
* <span class="badge badge-success">Expectation</span> <span class="text-success">**Maintain product quality**</span> i.e. prevent breaking other parts of the product as it evolves. Note that bugs local to a specific feature will be counted against the author of that feature. However, if a new enhancement breaks the entire product, the whole team will have to share the penalty.
* <span class="badge badge-success">Expectation</span> <span class="text-success">**Manage the project**</span> i.e. ensure workflow, code maintenance, integration, releases, etc. are done smoothly.
</span>

<span id="individualExpectations">

### <div class="text-white bg-info p-1">{{ icon_individual }} Individual Expectations</div>

#### <span class="badge badge-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Implementation</span>

* <span class="badge badge-info">Expectation</span> <span class="text-info">**Enhance the product in some way(s).**</span>
  * User-visible enhancements are preferred, but it is not a strict requirement.:
  * **The enhancement(s) should fit with the rest of the software** (and the target user profile) and should have the consent of the team members. %%You will lose marks if you go 'rogue' and add things that don't fit with the product.%%
  * Given below are some examples:

<div class="indented-level4">
<panel type="seamless" header="Example enhancements" minimized >

  * Add a new feature %%e.g. add the ability to view statistics%%
  * Enhance an existing features in a major way %%e.g. make the command syntax more user friendly and closer to natural language%%
  * A redesign of the GUI %%e.g. make it work like a chat application (note: chat is a form of CLI)%%
  * A redesign of the code %%e.g. Improve the design to improve the code quality.%%

</panel><p/>
</div>

* **Tip: Contribute to all aspects of the project** e.g. write backend code, frontend code, test code, user documentation, and developer documentation. %%Reason: If you limit yourself to certain aspects only, you could lose marks allocated for the aspects you did not do. In addition, the final exam assumes that you are familiar with all aspects of the project.%%

* **Tip: Do _all_ the work related to your enhancement yourself.** %%Reason:If there is no clear division of who did which enhancement, it will be difficult to divide project credit (or assign responsibility for bugs detected by testers) later.%%

* **Tip: Divide the components of the product among team members**. Notwithstanding the above, you are still recommended to divide the components of the product among team members so that each team member is _in charge_ of one or more components. While others will be modifying those components as necessary for the features they are implementing, your role as the _in charge_ of a component is to guide others modifying that component %%(reason: you are supposed to be the most knowledgeable about that component)%% and protect that component from degrading %%e.g., you can review others' changes to your component and suggest possible changes%%.


#### <span class="badge badge-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Documentation</span>

* **Objective:** showcase your ability to write both _user-facing documentation_ and _developer-facing documentation_.
* <span class="badge badge-info">Expectation</span> <span class="text-info">**Update the User Guide (UG) and the Developer Guide (DG) parts**</span> that are related to the enhancements you added.The minimum requirement is given below. %%(Reason: Evaluators will not be able to give you marks unless there is sufficient evidence of your documentation skills.)%%
  * UG: at least 1 page
  * DG: at least 3 pages
* **Tip: If the UG/DG updates for your enhancements are not enough to reach the above requirements**, you can make up the shortfall by documenting 'proposed' features and alternative designs/implementations. 
* <span class="badge badge-info">Expectation</span> <span class="text-info">**Use at least 2 types of UML diagrams in your DG updates**</span> i.e., diagrams you added yourself or those you modified significantly.

#### <span class="badge badge-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Testing</span>

<div id="testing-expectations">

* <span class="badge badge-info">Expectation</span> <span class="text-info">**Write _some_ automated tests**</span> so that we can evaluate your ability to write tests.

<div class="indented">

<box>

**:thinking: How much testings is enough?** We expect you to decide. You learned different types of testing and what they try to achieve. Based on that, you should decide how much of each type is required. Similarly, you can decide to what extent you want to automate tests, depending on the benefits and the effort required.<br>
There is no requirement for a minimum coverage level. Note that in a production environment you are often required to have at least 90% of the code covered by tests. In this project, it can be less. ==The weaker your tests are, the higher the risk of bugs, which will cost marks if not fixed before the final submission.==
</box>
</div>

</div>

#### <span class="badge badge-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Teamwork</span>

* <span class="badge badge-info">Expectation</span> <span class="text-info">**Do a fair share of the _team-tasks_**.</span>

<div id="team-tasks" class="indented-level2">

<box>

_Team-tasks_ are the tasks that _someone_ in the team has to do. Marks allocated to team-tasks will be divided among team members based on how much each member contributed to those tasks.

<panel type="seamless" header="{{ icon_example }} Examples of team-tasks">

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
</box>
</div>

* <span class="badge badge-info">Expectation</span> <span class="text-info">**Assume a fair share of project roles and responsibilities**.</span>

<div class="indented-level2">

<box>
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
* _In charge of[Component XYZ]_: %%e.g. In charge of `Model`, `UI`, `Storage`, etc.%% If you are in charge of a component, you are expected to know that component well, and review changes done to that component in {{ penultimate_version }}-{{ final_version }}.
</panel><p/>

{{ icon_tip }} Ensure each of the important roles are assigned to one person in the team. It is OK to have a 'backup' for each role, but **for each aspect there should be one person who is unequivocally the person responsible for it**. %%Reason: when _everyone is responsible for everything_, no one is.%%
</span>
</box>
</div>

* <span class="badge badge-info">Expectation</span> <span class="text-info">**Review each others work**.</span> %%Reason: reviewing skills is a learning outcome, and it is mutually beneficial.%%

</span>

</div>

{% endcall %}
