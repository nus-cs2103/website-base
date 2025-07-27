{% from "common/macros.njk" import embed_topic, show_faq with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-overview") %}
<div id="main">

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


<div id="tp-direction">

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
* Multiple types of related things %%e.g., Contacts and Tasks (if Tasks are allocated to Contacts)%%
* ...
{% endset %}

<div tags="m--cs2103">

<span class="badge rounded-pill bg-dark text-light">++++Direction 1: Evolve++++</span> Evolve <tooltip content="AddressBook-Level3">AB3</tooltip> into a more powerful or more optimized contact management app. Some examples:

* Contact managing optimized for a specific type of user. e.g.,
  * a sales person managing client contacts (can be further optimized for the product/service type e.g., insurance, loans, real estate, etc.)
  * a teacher/tutor managing students (can be further optimized to a specific course or type of teaching)
  * a secretary of an organization managing member details
  * an event organizer managing participants
* Manage more entity types related to contacts %%e.g., Tasks allocated to contacts, loans given, grades, etc.%%<br>
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
 {{ icon_important_big_red }} Be careful not to contradict given [project constraints]({{ baseUrl }}/admin/tp-constraints.html) when defining the user profile %%e.g., the target user should still prefer typing to mouse actions%%.

<box type="warning" seamless>

**Narrow down only to the extent you intend to optimize**: The narrowing down the target user should be tied to an intention (and the feasibility) to optimize the application to that 'narrowed down' target user. For example, it doesn't make sense to narrow down the target user to _NUS students_ if the application will not be optimized to NUS students specifically (i.e., the app can be used irrespective of which university the user is from).
</box>

<div class="indented-level1">

{{ show_faq("tpWhyNarrowTarget") }}
{{ show_faq("tpHowNarrowTargetCanBe") }}
</div>

* **Define a clear _value proposition_** that matches the target user profile i.e., what problem does the product solve? how does it make the user's life easier?<br>
  You should also define the _scope_ clearly i.e., boundary beyond which the app will not help %%e.g., the app will manage contact details of a small number of JC-level students (which means the there is no support for managing large number of students or primary/adult students, and will only manage contact details -- not other details such as grades)%%.
* **Aim to optimize the product to the chosen target users** Although you should not decide specific features yet, keep in mind that eventually you should optimize the product for the chosen target user %%i.e., add/tweak features that are especially/only applicable for target users (to make the app especially attractive to them)%%.
  * Example 1: If the product targets {{ course_pair }} instructors, there can be features that are applicable to them only, %%such as the ability to see a link to a student's project on GitHub%%
  * Example 2: If your app manages contacts, you can optimize its features based on,
    * the profession of the target user %%e.g., doctors, salesmen, teachers, etc.%%
    * the nature/scale of contacts %%e.g., huge number of contacts (for HR admins, user group admins), mostly incomplete contacts, highly volatile contact details, contacts become inactive after a specific period (e.g., contract employees)%%
    * what users do with the contacts %%e.g., organize group events, share info, do business, do analytics%%

    {{ icon_tip }} Your project will be graded based on how well the features match the target user profile and how well the features fit-together.

</div>

{% endcall %}
