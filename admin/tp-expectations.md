{% from "common/macros.njk" import embed_topic, show_faq with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-expectations") %}
<div id="main">

<span class="keyword d-none">project expectations</span>

<!-- ==================================================================================================== -->

## Outcomes

The high-level learning outcome of the team project (tP):

<box><markdown>{{ icon_outcome }} Can contribute production quality SE work to a small/medium {{ "_brownfield_ " if cs2103 }}software project</markdown></box>

<div tags="m--cs2103">

Accordingly, the tP is structured to resemble a non-trivial real-life brownfield software project in which you will,
 1. conceptualize and implement enhancements to a given product, and,
 1. have it ready to be continued by future developers
</div>
<div tags="m--cs2113">

Accordingly, the tP is structured to resemble an early stage of a small software project in which you will,
 1. conceptualize and implement a product, and,
 1. have it ready to be continued by future developers
</div>

The focus of the tP is to learn the following aspects:
1. ~~coding~~ %%(taken for granted, not focused on specifically)%%
1. working in a team
1. process/workflow
1. documentation
1. scheduling and tracking project progress, meeting delivery deadline
1. quality assurance


<span id="tp-direction">

<!-- ==================================================================================================== -->

## Direction

<div tags="m--cs2103">

The tP uses a generic application called [AddressBook-Level3 (AB3)](https://se-edu.github.io/addressbook-level3/) (from https://se-education.org) as the starting point.

<pic eager src="https://github.com/se-edu/addressbook-level3/raw/master/docs/images/Ui.png" width="600"></pic>
<p/>

</div>

The final product is to be targeted at users who can type fast, and prefer typing over mouse/voice commands. Therefore, ==typed user commands are the primary mode of input.==

{{ embed_topic("tp-constraints.md#Constraint-Typing-Preferred", "Admin " + icon_embedding + " tP Constraints → Constraint-Typing-Preferred", "2", indent="1") }}
{{ embed_topic("tp-constraints.md#Recommendation-CLI-First", "Admin " + icon_embedding + " tP Constraints → Recommendation-CLI-First", "2", indent="1") }}
<p/>

{% set morph_examples %}
  For example, an app to manage one of these:{% if cs2113 %}
    * Contact details{% endif %}
    * Bookmarks of websites
    * Tasks/Schedule
    * Location info
    * Thing to memorize i.e. flash cards, trivia
    * Forum posts, news feeds, Social media feeds
    * Online projects or issue trackers that the user is interested in
    * Emails, possibly from different accounts
    * Multiple types of related things %%e.g. Contacts and Tasks (if Tasks are allocated to Contacts)%%
    * ...
{% endset %}

<div tags="m--cs2103">

<span class="badge rounded-pill bg-dark text-light">++++Direction 1: Evolve++++</span> Evolve <tooltip content="AddressBook-Level3">AB3</tooltip> into a more powerful or more optimized contact management app. Some examples:

* Contact managing optimized for a specific type of user. e.g.,
  * a sales person managing client contacts (can be further optimized for the product/service type e.g., insurance, loans, real estate, etc.)
  * a teacher/tutor managing students (can be further optimized to a specific course or type of teaching)
  * a secretary of an organization managing member details
  * an event organizer managing participants
* Manage more entity types related to contacts %%e.g. Tasks allocated to contacts, loans given, grades, etc.%%<br>
  Note: the contacts should still remain the primary focus, even if there are other things being managed e.g., an address book app that is optimized for a user who lends out money to those contacts (not a loan management app).
* Introduce relationships between contacts e.g., members of a team
* Make existing general features _really_ strong, worthy of a real product e.g.,
  * make the commands more natural, easier to type/remember, allow aliases, etc.
  * make the search feature more powerful (e.g, fuzzy search)
  * tweak the GUI to be more useful (e.g., highlight the contact added/edited
  * provide GUI alternatives to CLI commands where appropriate)
* Add more general features e.g.,
  * import/export data from other formats
  * archive old data
  * more help: guided tours, tool tips, tip of the day etc.
  * stats, analytics, visualizations
  * undo/redo
  * result preview (i.e., show what would happen if the current command is executed)
* Internal improvements e.g., refactor the current design/implementation to make it better in some way

<div class="indented-level1">

{{ pros }} less changes to existing code at the start of the project (i.e., progress will be smoother at the start), can result in a more mature product with deeper features as the product functionality will be moving forward from the start.<br><br>
{{ cons }} less flexibility in product design.
</div>

~~<span class="badge rounded-pill bg-dark text-light">++++Direction 2: Morph++++</span> Morph AB3 in any direction you wish.~~

==**This direction is <span class="text-danger">not available this semester</span>, as it has been observed to increase tP workload**== beyond what students anticipate when making this choice (e.g., 40-50% more work than strictly needed by the tP). Besides, it is less brownfield than direction 1.
<div class="indented-level1">

~~{{ pros }} more flexibility in the project direction.<br><br>
{{ cons }} more changes to the existing code at the start while you are still not very familiar with the codebase, morphing is less common in real projects (compared to direction 1).~~
</div>

Note that **creating a novel/unique/interesting product will NOT earn you extra marks** in this course. While those qualities are important in real world projects, and we do allow you room to go in those directions in this course, they are not the focus of this course {% if cs2103 %}%%(there are other courses such as CS3216, CS3217 that focus on those aspects)%%. Focus your energy on creating a _solid product at a high quality level_, which actually take a lot more energy than you might realize at first. Go for novelty/uniqueness/interesting etc. only if you have energy to spare and can do so without compromising the quality. For example, a bland feature/product implemented well will score more marks than a novel product that is buggy, even if the novel features were harder to implement.

{% endif %}
<div tags="m--cs2113">

* {{ morph_examples | trim }}
</div>
</div>

<div tags="m--cs2113">

==You are strongly discouraged from developing a GUI application== as it can increase the workload unnecessarily.
{{ embed_topic("tp-constraints.md#Recommendation-No-GUI", "Admin " + icon_embedding + " tP Constraints → Recommendation-No-GUI", "2", indent="1") }}
</div>

<!-- ==================================================================================================== -->

## Target User & Value Proposition

You are expected to:
* **Define a very specific _target user profile_.** <br> ==We require you to narrow down the target user profile==  %%as opposed to trying to make it as general as possible. Here is an example of progressively narrowing down target user: anybody → teachers → university teachers → tech-savvy university teachers → instructors of course CS____.%%<br><br>
 {{ icon_important_big_red }} Be careful not to contradict given [project constraints]({{ baseUrl }}/admin/tp-constraints.html) when defining the user profile %%e.g. the target user should still prefer typing to mouse actions%%.

<div class="indented-level1">

<panel type="seamless" header="%%FAQ: Why the need to narrow down the user profile?%%" >

* It is an opportunity to exercise your product design skills because optimizing the product to a very specific target user requires good product design skills.
* It minimizes the overlap between features of different teams which can cause plagiarism issues. Furthermore, higher the number of other teams having the same features, less impressive your work becomes especially if others have done a better job of implementing that feature.
</panel>

<panel type="seamless" header="%%FAQ: How narrow can we make the target market?%%" >

The size of the target market is not a grading criterion. You can make it as narrow as you want. Even a single user target market is fine as long as you can define that single user in a way others can understand (reason: project evaluators need to evaluate the project from the point of view of the target users).
</panel>
</div>

* **Define a clear _value proposition_** that matches the target user profile i.e., what problem does the product solve? how does it make the user's life easier?<br>
  You should also define the _scope_ clearly i.e., boundary beyond which the app will not help %%e.g., the app will manage contact details of a small number of JC-level students (which means the there is no support for managing large number of students or primary/adult students, and will only manage contact details -- not other details such as grades)%%.
* **Aim to optimize the product to the chosen target users** Although you should not decide specific features yet, keep in mind that eventually you should optimize the product for the chosen target user %%i.e., add/tweak features that are especially/only applicable for target users (to make the app especially attractive to them)%%.
  * Example 1: If the product targets {{ course_pair }} instructors, there can be features that are applicable to them only, %%such as the ability to see a link to a student's project on GitHub%%
  * Example 2: If your app manages contacts, you can optimize its features based on,
    * the profession of the target user %%e.g. doctors, salesmen, teachers, etc.%%
    * the nature/scale of contacts %%e.g. huge number of contacts (for HR admins, user group admins), mostly incomplete contacts, highly volatile contact details, contacts become inactive after a specific period (e.g. contract employees)%%
    * what users do with the contacts %%e.g. organize group events, share info, do business, do analytics%%

    {{ icon_tip }} Your project will be graded based on how well the features match the target user profile and how well the features fit-together.

<span id="functionalityExpectations">

<!-- ==================================================================================================== -->

<h2 class="text-white bg-danger p-1">Functionality Expectations</h2>

<div tags="m--cs2103" id="functionality-expectations">

**The expected level of _functionality_ is what you could achieve if each member puts in about ==50% of the implementation effort they put into the iP==** (i.e., it is set at half because, even after adding the extra overheads of doing the project as a team, and working with an exising codebase, we don't want the tP to take more effort than the iP).<br>
Furthermore, we estimate that the above-mentioned bar is roughly equivalent to **writing about 300-400 lines of functional code** (excluding testing and documentation) per person.

<box type="important" seamless>

  In case you happen to look at tP's of past batches (2023 and before) in order to gauge the required effort, note that the above reflects a ==drastically lower bar from previous semesters==. For reference, the bar given to previous batches was 'same as iP effort' (not half), and the median LoC of functional code written by a student was about 850 LoC.
</box>
</div>
<div tags="m--cs2113">

**The expected level of _functionality_ from a team is roughly ==what you can achieve if each member contributes about the same amount of functional code as required by a <tooltip content="i.e., if all requirements were met at the _minimal_ level specified">typical iP</tooltip>==**.
</div>

==There are no extra marks for exceeding implementation _effort_ bar== stated above. Hence, _effort_ is graded on mostly an S/U basis) -- it is the _quality_ of the code that really determines the marks for _implementation_ component (more info <trigger trigger="click" for="modal:tPexpectations-implementationGrading">here</trigger>).  So, you are better off spending more effort in improving other aspects of the project. Try to avoid adding more features than necessary, unless you are doing it out of interest. As mentioned elsewhere, a functionality just the right size and of high quality will earn more marks than a functionality that is bigger (or more difficult, or more interesting/novel) but of lower quality.

<div tags="m--cs2103">
{% call show_faq("If our team implement features x, y, and z, is that enough?") %}
Yes, if it requires each member to put in about a half an iP worth of effort.
{% endcall %}

{% call show_faq("Is it a must to write at least 300 LoC?") %}
Not necessarily. It depends on the effort required, which in turn depends on what the code does. It is quite possible for 100 LoC that implements feature X to take more effort than 300 LoC that implements feature Y (i.e., it depends on the context). So, we measure the effort, not LoC (LoC figure given is just a rough estimate of the _equivalent_ effort).
{% endcall %}

{% call show_faq("Still, if I write 300 LoC, I get full marks for implementation?") %}
There is no such guarantee, for two reasons:

1. Your implementation effort is graded based on how much functionality your team produced (based on peer-testers' and tutors' estimates) and how much of that work was contributed by you (based on team members' estimates). For example, simply copy-pasting 400+ LoC with only minor modifications is unlikely to meet this bar as it is less than an effort _equivalent_ to writing a typical 300-400 LoC (or half of a typical iP effort).
1. Implementation marks are based on both effort and quality, the latter being the primary driver (more info <trigger trigger="click" for="modal:tPexpectations-implementationGrading">here</trigger>). So, meeting the effort bar doesn't guarantee full marks for implementation.
{% endcall %}

<p/>
</div>

<modal large header="tP: Grading [extract] → " id="modal:tPexpectations-implementationGrading">
  <include src="tp-grading.md#grading-implementation"/>
</modal>

<box type="important" tags="m--cs2113" seamless>

In the most recent semester, more than 80% of the students did significantly more work than what was needed to earn full marks for effort. Many of them were likely under the wrong impression that doing more features will earn them more marks. Try to avoid doing the same mistake yourself.

In fact, here is the grading criterion for the individual project effort:
{{ embed_topic("tp-pe-fragment.md#projectGrading-effort-instructions", "Admin " + icon_embedding + " tP → PE → ==Evaluating the  Implementation Effort==", "3") }}
</box>

<box tags="m--cs2103">

{{ icon_tip }} If you wish to add the following features to your app, we recommend (but not require) you to follow similar features in AB4 (not AB3) in order to reduce the effort required.
  * [Undo/redo](https://se-education.org/addressbook-level4/DeveloperGuide.html#undo-redo-feature)
  * [Automated GUI tests](https://se-education.org/addressbook-level4/Testing.html#types-of-tests)
</box>

</span>
<span id="teamExpectations">

<!-- ==================================================================================================== -->

<h2 class="text-white bg-success p-1">{{ icon_team }} Team Expectations</h2>

* <span class="badge bg-success">Expectation</span> <span class="text-success">**Produce a _cohesive_ product:**</span> i.e. ensure,
  1. features fit together to form a cohesive product,
  1. documentation follows a consistent style and presents a cohesive picture to the reader{% if cs2113 %}, and
  1. final project demo presents a cohesive picture to the audience.{% endif %}
* <span class="badge bg-success">Expectation</span> <span class="text-success">**Maintain product integrity/quality:**</span> i.e. prevent breaking other parts of the product as it evolves. <span tags="m--cs2103 m--cs2113">
* <span class="badge bg-success">Expectation</span> <span class="text-success">**Manage the project:**</span> i.e. ensure workflow, code maintenance, integration, releases, etc. are done properly.
</span>

</span>
<div id="individualExpectations">

<!-- ==================================================================================================== -->

<h2 class="text-white bg-info p-1">{{ icon_individual }} Individual Expectations</h2>

#### <span class="badge bg-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Implementation</span>

* <span class="badge bg-info">Expectation</span> <span class="text-info">**Contribute to the functional code of the product.**</span>
  * User-visible features are preferred, but it is not a strict requirement.:
  * **The enhancement(s) should fit with the rest of the software** (and the target user profile) and should have the consent of the team members. %%You will lose marks if you go 'rogue' and add things that don't fit with the product.%%

<div tags="m--cs2103" class="indented-level2">

<panel type="seamless" header="Some example enhancements" >

  * Add a new feature %%e.g. add the ability to view statistics%%
  * Enhance an existing features in a major way %%e.g. make the command syntax more user friendly and closer to natural language%%
  * A redesign of the GUI %%e.g. make it work like a chat application (note: chat is a form of CLI)%%
  * A redesign of the code %%e.g. Improve the design to improve the code quality.%%

</panel><p/>
</div>

* **Tip: Contribute to _all_ aspects of the project** e.g. write backend code, frontend code, test code, user documentation, and developer documentation. %%Reason: If you limit yourself to certain aspects only, you could lose marks allocated for the aspects you did not do. In addition, the final exam assumes that you are familiar with all aspects of the project.%%

* **Tip: Do _all_ the work related to your enhancement yourself.** %%Reason: If there is no clear division of who did which enhancement, it will be difficult to divide project credit (or assign responsibility for bugs detected by testers) later.%%<br>
  In other words, ==we recommend that the work to be divided primarily based on _features/enhancements_== rather than _components_. The latter has the risk of a team member becoming a _single point of failure_ and you becoming _too reliant_ on other team members %%e.g., what if the person assigned to an important component doesn't deliver on time?%%.

<div tags="m--cs2103">

* **Tip: Divide the components of the product among team members**. Notwithstanding the above, you are still recommended to divide the components of the product among team members so that each team member is _in charge_ of one or more components. While others will be modifying those components to fit their features, your role as the _in charge_ of a component is to guide others modifying that component %%(reason: you are supposed to be the most knowledgeable about that component)%% and protect that component from degrading %%e.g., you can review others' changes to your component and suggest possible changes%%.
</div>


#### <span class="badge bg-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Documentation</span>

* **Objective:** showcase your ability to write both _user-facing documentation_ and _developer-facing documentation_.
* <span class="badge bg-info">Expectation</span> <span class="text-info">**Update the User Guide (UG) and the Developer Guide (DG) parts**</span> that are related to the enhancements you added.
* **Tip: If the UG/DG updates for your enhancements are not enough to reach the above requirements**, you can make up the shortfall by documenting 'proposed' features and alternative designs/implementations.{% if cs2113 %}
* <span class="badge bg-info">Expectation</span> <span class="text-info">**Use at least {{ uml_diagrams_per_person }} UML diagrams in your DG updates**</span> i.e., diagrams you added yourself or those you modified significantly.{% endif %}

#### <span class="badge bg-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Testing</span>

<div id="testing-expectations">

* <span class="badge bg-info">Expectation</span> <span class="text-info">**Write _some_ automated tests**</span> so that there is evidence that you _can_ write automated tests.

<div class="indented-level2">

<box>

**:thinking: How much testing is enough?** We expect you to decide. As you learn different types of testing and what they try to achieve, you should decide how much of each type is worth having. Similarly, you can decide to what extent you want to automate tests, depending on the benefits and the effort required.<br>
There is no requirement for a minimum test coverage level. Note that in a high-end production environment you might be required to have high levels of test coverage (e.g., 90%). In this project, it can be less. ==Caveat: The weaker your tests are, the higher the risk of undetected bugs/regressions, which will cost you marks if not detected/fixed before the final submission.==
</box>
</div>

</div>

#### <span class="badge bg-info">{{ icon_individual }} Individual</span> <span class="text-info">Expectations on Teamwork</span>

* <span class="badge bg-info">Expectation</span> <span class="text-info">**Do an equal share of the _team-tasks_**.</span>

<div id="team-tasks" class="indented-level2">

<box>

_Team-tasks_ are the tasks that _someone_ in the team has to do.

<panel type="seamless" header="{{ icon_example }} Examples of team-tasks">

<span id="example-team-tasks">

Here is a non-exhaustive list of team-tasks:

1. Setting up the GitHub team org/repo
1. Necessary general code enhancements{% if cs2103 %} e.g.,
   1. Work related to renaming the product
   1. Work related to changing the product icon{% endif %}
1. Setting up tools e.g., GitHub, Gradle
1. Maintaining the issue tracker
1. Release management
1. Updating user/developer docs that are not specific to a feature %%e.g. documenting the target user profile%%
1. Incorporating more useful tools/libraries/frameworks into the product or the project workflow %%(e.g. automate more aspects of the project workflow using a GitHub plugin)%%

</span>
</panel><p/>
</box>
</div>

* <span class="badge bg-info">Expectation</span> <span class="text-info">**Carry an equal share of project roles and responsibilities**.</span>

<div class="indented-level2">

<box>
<span id="roles">

_Roles_ indicate aspects you are in charge of and responsible for. %%E.g., if you are in charge of documentation, you are the person who should allocate which parts of the documentation is to be done by who, ensure the document is in right format, ensure consistency etc.%%

<panel type="seamless" header="{{ icon_example }} Example roles and responsibilities">

This is a non-exhaustive list; you may define additional roles.

* _Team lead_: Responsible for overall project coordination.
* _Documentation_ (short for ‘in charge of documentation’): Responsible for the quality of various project documents.
* _Testing_: Ensures the testing of the project is done properly and on time.
* _Code quality_: Looks after code quality, ensures adherence to coding standards, etc.
* _Deliverables and deadlines_: Ensure project deliverables are done on time and in the right format.
* _Integration_: In charge of versioning of the code, maintaining the code repository, integrating various parts of the software to create a whole.
* _Scheduling and tracking_: In charge of defining, assigning, and tracking project tasks.
* _[Tool ABC] expert_: %%e.g. IntelliJ expert, Git expert, etc.%% Helps other team member with matters related to the specific tool.

<div tags="m--cs2103">

* _In charge of [Component XYZ]_: %%e.g. In charge of `Model`, `UI`, `Storage`, etc.%% Note that being _in charge_ of a component doesn't mean you are the only one who should be modifying that component. Rather, you are the one who's expected to, know that component best, review changes done to that component in {{ version_penultimate }}-{{ version_final }}, act as the gate keeper of its quality, help others when they face difficulties while modifying that component etc.
</div>
<div tags="m--cs2113">

* _In charge of[Area XYZ]_ of the code: %%e.g. In charge of the code that deals with storage, etc.%% If you are in charge of an area, you are expected to know that area well, and review changes done to that code.
</div>
</panel><p/>

{{ icon_tip }} Ensure each of the important roles are assigned to one person in the team. It is OK to have a 'backup' for each role, but **for each aspect there should be one person who is unequivocally the person responsible for it**. %%Reason: when _everyone is responsible for everything_, no one is.%%
</span>
</box>
</div>

* <span class="badge bg-info">Expectation</span> <span class="text-info">**Review each others work**.</span> %%Reason: reviewing skills is a learning outcome, and it is mutually beneficial.%%

</div>

</div>

{% endcall %}
