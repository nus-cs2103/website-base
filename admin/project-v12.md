<tip-box> 

**v1.2 Summary of Deliverables**

Here is a summary of individual and team deliverables for v1.2 to consider it as _reached_. See sections below for more details of each deliverable. Individual deliverables and team deliverables are considered separately for grading %%&nbsp;e.g. if a team member fail individual deliverables for more than two milestones, only that member's marks will be affected%%.

* :bust_in_silhouette: Individual:
  - [ ] Contributed code to the product
  - [ ] Described implementation details in the Developer Guide
* :busts_in_silhouette::busts_in_silhouette: Team:
  - [ ] v1.2 managed using GitHub features (issue tracker, milestones, etc.)

</tip-box>

  
### v1.2 Project Management

<tip-box type="important">

Starting from this version, ==there are additional requirements to follow== regarding how you **use GitHub to manage your milestones**, as described in <trigger trigger="click" for="modal:v12-projectTracking">[Admin &raquo; Appendix E: GitHub: Project Schedule Tracking]</trigger>.

</tip-box>

As before, you are _recommended_ (but not required) to **follow the forking workflow** when evolving the product.

<modal large title="Admin &raquo; Appendix E: Github: Project Schedule Tracking" id="modal:v12-projectTracking">
  <include src="appendixE-gitHub.md#project-schedule-tracking"/>
</modal>

**From v1.2 onwards each member is expected to contribute <tooltip content="the amount of code does not matter; even small contributions are acceptable">some</tooltip> code to each <tooltip content="v1.2, v1.3, ...">weekly milestone</tooltip>; only merged code is considered as contributions** %%<popover content="The ability to deliver code incrementally is an important LO of this module because incremental delivery improves the _visibility_ of your work.">(Reason)</popover>%%.  ==If you <tooltip content="failed to contribute code to">miss</tooltip> more than two weekly milestones, you will start losing marks.== <br>
  If an enhancement is too big to complete in one week, here are some options:
   * [Preferred] Deliver it in smaller incremental steps e.g. deliver a basic version of the enhancement first. 
   * Do a different, smaller, enhancement for the current week while working on a bigger enhancement to deliver in a future week.
   * Choose not contribute to the weekly milestone. This should be fine as long as you don't miss more than two milestones.

### v1.2 Product

**Submission**: Update code in GitHub.

**Grading**: Criteria to consider this milestone as reached
* A new version tagged `v1.2` is in your repo. %%&nbsp;If `v1.2` is already used by a past commit, you can use something similar such as `V1.2` or `v1.2.0`.%%
* The version `v1.2` is step towards `v2.0` (but it does not matter how big a step it is)

### v1.2 Documentation

* **User Guide**: Update as necessary.
  * If a feature has been released in this version, replace the `Coming in v2.0` annotation with a `Since v1.2`. Also replace UI mockups with actual screenshots.
  * If a feature design has changed, update the descriptions accordingly.

* **Developer Guide**:
  * ==Each member should describe the implementation of at least one enhancement she has added== (or planning to add). <br>
    Expected length: ~1 page per person
  * The description can contain things such as,
    * How the feature is implemented.
    * Why it is implemented that way.
    * Alternatives considered.
  * The stated objective is to explain the implementation to a future developer, but a hidden objective is to show evidence that you can document deeply-technical content using prose, examples, diagrams, code snippets, etc. appropriately. To that end, you may also describe features that you plan to implement in the future, even beyond v1.5 (hypothetically).
  * For an example, see [the description of the undo/redo feature implementation in the AddressBook-Level4 developer guide](https://nus-cs2103-ay1718s1.github.io/addressbook-level4/DeveloperGuide.html#undo-redo-mechanism).
  

### v1.2 Demo

Do an informal demo of the new feature during the tutorial. ==Each team member should demo their own work, using the `master` branch.==