<div id="project-direction">
In general, each team is expected to take one of these two directions:

**[Direction 1]  _Optimize_** AddressBook for a more specific target user group:
   
<panel header="Examples for the _optimize_ direction" expanded> 
   
An AddressBook,
   * for users in a specific profession %%&nbsp;e.g. doctors, salesmen, teachers, etc.%%
   * based on the nature/scale of contacts %%&nbsp;e.g. huge number of contacts (for HR admins, user group admins), mostly incomplete contacts, highly volatile contact details, contacts become inactive after a specific period (e.g. contract employees)%%
   * based on what users do with the contacts %%&nbsp;e.g. organize group events, share info, do business, do analytics%%   
   
</panel><p/>

   
**[Direction 2] _Morph_** AddressBook into a different product: Given that AddressBook is a generic app that manages a type of elements (i.e. contacts), you can use it as a starting point to create an app that manages something else.<br>
 :exclamation: This is a high-risk high-reward option because morphing requires extra work but a morphed product may earn more marks than an optimized product of similar complexity.
   
<panel header="Examples for _morph_ direction" expanded> 
   
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

* **Target user profile**: Define a very specific target user profile. <br> :bulb: We recommend you narrow down the target user profile quite a lot %%&nbsp;as opposed to trying to make it as general as possible. Here is an example direction of narrowing down target user: anybody &rarr; teachers &rarr; university teachers &rarr; tech savvy university teachers &rarr; CS2103 instructors.%%<br>
 :exclamation: Be careful not to contradict given project constraints when defining the user profile %%&nbsp;e.g. the target user should still prefer typing over mouse actions%%.

* **Value proposition**: Define a clear _value proposition_ %%&nbsp;what problem does the product solve? how does it make the the user's life easier%% that matches the target user profile.

**It is expected that your product will be optimized for those specific target users** %%&nbsp;i.e., add features that are especially/only applicable for target users (to make the app especially attractive to them). To add to the example above, there can be features that are applicable to CS2103 instructors only, such as the ability to navigate to a student's project on GitHub%%<br>
 :bulb: Your project will be graded based on how well the features match the target user profile and how well the features fit-together.

<panel header="%%Why the need to narrow down the user profile?%%"> 
 
* It is an opportunity to exercise your product design skills because optimizing the product to a very specific target user requires good product design skills.
* It minimizes the overlap between features of different teams which can cause plagiarism issues. Furthermore, higher the number of other teams having the same features, less impressive your work becomes especially if others have done a better job of implementing that feature.   
 
</panel><p/>

</div>
   
<span id="individual-expectations">

:bust_in_silhouette: **Individually**, each student is expected to,

1. **Contribute ==one major enhancement== to the product**<br>
   * Each enhancement should be stand-alone but,
     * should fit with the rest of the software (and the target user profile),
     * and should have the consent of the team members.
  
   <panel header="Allowed enhancements" expanded>
   
   Here are the allowed options for enhancing AddressBook:
   
   1. Add a new feature
   1. Enhance an existing features in a major way %%e.g. make the command syntax more user friendly and closer to natural language%%
   1. Modify the internal design in a major way %%e.g. change the architecture%%
   1. A major redesign of the GUI %%e.g. make it work like a chat application (note: chat is a form of CLI)%%
   1. Integrate with online services %%e.g. Google contacts, Facebook, GitHub, etc.%%
   
   </panel><p/>
   
   <panel header="Major enhancements vs Grade: Examples" expanded> 
   
   Here are some examples of different major enhancements and the grade the student is likely to earn for the relevant parts of the project grade.
   * Example 1 (Expected grade: `A`) : [Add support for undo/redo](https://github.com/se-edu/addressbook-level4/pull/610/files)
   * Example 2 (Expected grade: `B`) : [Add support for viewing history](https://github.com/se-edu/addressbook-level4/pull/440/files)
   
   </panel><p/>

1. **Contribute ==one _minor_ enhancement== to the product**: 
   * In the initial stages of the project you are required to add one small generic enhancements in order to get familiar with the project.
   * Minor enhancements earn a minimal amount of marks. You are advised not to spend a lot of effort on the minor enhancement.
   * The minor enhancement must touch multiple components %%&nbsp;so that it helps you to familiarize yourself wit the codebase%%. 
   
   <panel header="Examples of minor enhancements" expanded>
   
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
 
1. **Contribute to all aspects of the project**: e.g. write backend code, frontend code, test code, user documentation, and developer documentation. If you limit yourself to certain aspects only, you will lose marks allocated for the aspects you did not do.<br>
  In particular, ==you are required to divide work based on features rather than components==:
 * By the end of this project (i.e. by v1.5) each team member is expected to have implemented one minor and one major enhancement/feature end-to-end, doing required changes in _almost all_ components. %%&nbsp;Reason: to force you to learn all components of the software, instead of limiting yourself to just one/few components%%.
 * Nevertheless, you are ==still expected to divide the components of the product among team members== so that each team member is _in charge_ of one or more components. While others will be modifying those components as necessary for the features they are implementing, your role as the _in charge_ of a component is to guide others modifying that component %%&nbsp;(reason: you are supposed to be the most knowledgeable about that component)%% and protect that component from degrading %%&nbsp;e.g., you can review others' changes to your component and suggest possible changes%%.

1. **Do a share of team-tasks**: These are the tasks that _someone_ in the team has to do. Marks allocated to team-tasks will be divided among team members based on how much each member contributed to those tasks.

   <panel header="Examples of team-tasks" expanded>
   
   Here is a non-exhaustive list of team-tasks:
   
   1. Necessary general code enhancements
      1. Work related to renaming the product
      1. Work related to changing the product icon
      1. Morphing the product into a different product
   1. Setting up the GitHub, Travis, AppVeyor, etc.
   1. Maintaining the issue tracker
   1. Release management
   1. Updating user/developer docs that are not specific to a feature %%&nbsp;e.g. documenting the target user profile%%
   1. Incorporating more useful tools/libraries/frameworks into the product or the project workflow %%(e.g. automate more aspects of the project workflow using a GitHub plugin)%%
   
   </panel><p/>

1. Write **~0.5 KLoC of code**, on average.

</span>
<span id="team-expectations">

:busts_in_silhouette: **As a team**, you are expected to work together to,

1. **Preserve product integrity**: i.e.
   1. Enhancements added fit together to form a cohesive product.
   1. Documentation follows a consistent style and presents a cohesive picture to the reader.
   1. Final project demo presents a cohesive picture to the audience.
1. **Maintain product quality**: i.e. prevent regressions in other parts of the product as the product evolves. Note that bugs local to a specific feature will be counted against the author of that feature. However, if a new enhancement breaks the entire product, the whole team will have to share the penalty.
1. **Manage the project smoothly**: i.e. ensure PR workflow, repo maintenance, integration, releases, etc. are done smoothly.

</span>
