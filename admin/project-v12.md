<tip-box> 

**v1.2 Summary of Milestone**

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
:bust_in_silhouette: Contributed code to the product | some code merged
:bust_in_silhouette: Described implementation details in the Developer Guide | some text and some diagrams added to the developer guide (at least in a PR), comprising at least one page worth of content
:busts_in_silhouette: v1.2 managed using GitHub features (issue tracker, milestones, etc.) | A new version tagged `v1.2` is in your repo. There is evidence of an attempt (even if not completely successful) to use GitHub features as described in <trigger trigger="click" for="modal:v12-projectTracking">[Admin » Appendix E: GitHub: Project Schedule Tracking]</trigger>. 

</tip-box>

  
### v1.2 Project Management

<tip-box type="important">

Starting from this version, ==there are additional requirements to follow== regarding how you **use GitHub to manage your milestones**, as described in <trigger trigger="click" for="modal:v12-projectTracking">[Admin » Appendix E: GitHub: Project Schedule Tracking]</trigger>.

</tip-box>

As before, you are _recommended_ (but not required) to **follow the forking workflow** when evolving the product.

<modal large title="Admin » Appendix E: Github: Project Schedule Tracking" id="modal:v12-projectTracking">
  <include src="appendixE-gitHub.md#project-schedule-tracking"/>
</modal>

**From v1.2 onwards each member is expected to contribute <tooltip content="the amount of code does not matter; even small contributions are acceptable">some</tooltip> code to each <tooltip content="v1.2, v1.3, ...">weekly milestone</tooltip>; only merged code is considered as contributions** %%<popover content="The ability to deliver code incrementally is an important LO of this module because incremental delivery improves the _visibility_ of your work.">(Reason)</popover>%%. <br>
  If an enhancement is too big to complete in one week, here are some options:
   * [Preferred] Deliver it in smaller incremental steps e.g. deliver a basic version of the enhancement first. 
   * Choose not to contribute to the weekly milestone. This should be fine as long as you don't miss more than two milestones.

### v1.2 Product

**Submission**: Update code in GitHub.

<tip-box>

:bulb: **If tests are causing too much pain ...**

Automated tests have benefits, but they can be a pain to write/maintain; GUI tests are especially hard to maintain because their behavior can sometimes depend on things such as the OS, resolution etc.

If you find tests too big a burden, it is OK to get rid of some of the troublesome tests and rely more on manual testing instead. The less automated test coverage you have, the higher the risk of regressions; but it may be an acceptable trade-off under the circumstances if tests are slowing you down too much.

Also note <trigger trigger="click" for="modal:v12-testingExpectations">our expectation on test code</trigger>. 

<modal title="Admin » Project Asessement → Expectation on testing" id="modal:v12-testingExpectations">
  <include src="project-testing.md#expectations"/>
</modal>

</tip-box>

<tip-box> 

:bulb: We use a tool called _Collate_ to extract out code written by each member in your final project submission. The tool requires you to annotate code with special tags to mark code written by you. Adding those annotations is usually done at v1.4 but you are welcome to start early. 

<panel header="**How to collate code for grading**" no-close>
  <include src="collate.md" />
</panel><p/>

</tip-box>

### v1.2 Documentation

* **User Guide**: Update as necessary.
  * If a feature has been released in this version, replace the `Coming in v2.0` annotation with a `Since v1.2`. Also replace UI mockups with actual screenshots.
  * If a feature design has changed, update the descriptions accordingly.

* **Developer Guide**:
  * ==Each member should describe the implementation of at least one enhancement she has added== (or planning to add). <br>
    Expected length: 1+ page per person
  * The description can contain things such as,
    * How the feature is implemented.
    * Why it is implemented that way.
    * Alternatives considered.
  * The stated objective is to explain the implementation to a future developer, but a hidden objective is to show evidence that you can document deeply-technical content using prose, examples, diagrams, code snippets, etc. appropriately. To that end, you may also describe features that you plan to implement in the future, even beyond v1.5 (hypothetically).
  * For an example, see [the description of the undo/redo feature implementation in the AddressBook-Level4 developer guide](https://nus-cs2103-ay1718s2.github.io/addressbook-level4/DeveloperGuide.html#undo-redo-mechanism).
  

### v1.2 Demo

Do an informal demo of the new feature during the tutorial. ==Each team member should demo their own work, using commit tagged as `v1.2` in the `master` branch== %%&nbsp;i.e. only features included in the current release should be demoed%%.