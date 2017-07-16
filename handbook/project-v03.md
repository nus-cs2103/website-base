### V0.3 Product

This version should be a more functional version than V0.2 and should contain at least a basic version of features you intend to release in the final version.

Ideally, V0.3 should be good enough for [dog fooding](http://www.urbandictionary.com/define.php?term=dogfooding%20(to%20dogfood)). Try to reach a dogfooding-ready version of the 'must have' features at least.

From V0.3, ==you are required to divide work based on features== rather than component. That is, each team member should implement 0 or more features end-to-end, doing required changes in *all* components. The objective of this switch is to force you to learn all components of the software, instead of limiting yourself to your own components.  
Note that you will continue to be in charge of your own components although others will be modifying your components' code. Your new role is to help others modify code in your components (you are supposed to be the most knowledgeable about those components) and protect your components from degrading. For example, you can review others' changes to your components and suggest possible changes. This is also a good time to switch to a PR based workflow (if you haven't done that already) as PRs can be reviewed by other team members before merging.

**Submission**: V0.3 (and future milestones) ==should be released using GitHub's release mechanism==. The release should include an executable JAR file. Refer the ['Making a Release' section of the sample developer guide](https://github.com/nus-cs2103-AY1617S2/addressbook-level4/blob/master/docs/DeveloperGuide.md#making-a-release) for more info.

**Grading**: To pass this checkpoint, your product should be noticeably better than an MVP. It goes without saying that other project management requirements expected at reaching a milestone (mentioned in the ['Using Milestones' section of Appendix E](#using-milestones)) are applicable too.  

### V0.3 Documentation

Follow the documentation in the sample project in terms or organization, level of details, etc.

*   **User Guide**: Update User Guide to match what you plan to deliver at V0.5
*   **Developer Guide**: Update Developer Guide to match your current design or the design you plan to have at V0.5.  
    [1] While it is OK for some sections to be written collectively, ==each student should have some sections that were written individually==. For example, the section describing the design of Logic component should be written by the person in charge of the Logic component.  
    [2] It is ==not enough to simply do minor tweaks to the existing document== to match your project if your design is very similar to the sample given. We need to see a significant amount of content written by each student to judge how well you can document technical details and use relevant models.  
    Here are some things you can add:
    *   Compare the current design with other alternative designs possible.
    *   Add more descriptions e.g. show at least one interaction within each component.
    *   Use object diagrams to show sample object structures at runtime (if it helps the reader).
    *   Explain how you implemented complicated features such as undo/redo.
    *   In future (after these topics have been covered):  
        * Use Activity Diagrams and OO Domain Models where applicable.  
        * Mention where design patterns/principles are applied.

**Submission**: Must be included in the version tagged `V0.3`.

**Grading**: To pass this checkpoint, your documentation should have been updated to match your project.  

### V0.3 Demo

**Submission**: Demo to the tutor during the tutorial. **Use jar** file for the demo, not the IDE.

**Grading**: Must use the version tagged `V0.3` and should be at least very close to a dog-fooding-ready state.