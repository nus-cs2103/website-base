`rc` = Release Candidate

<tip-box> 

**v1.5 Summary of Deliverables**

* :bust_in_silhouette: Individual:
  - [ ] Contributed code to v1.5rc
  - [ ] Project Portfolio Page merged
* :busts_in_silhouette::busts_in_silhouette: Team:
  - [ ] Well-prepared for the demo
  - [ ] v1.5rc released properly on GitHub
  - [ ] v1.5rc milestone wrapped up properly on GitHub

</tip-box>

### v1.5rc Project Management

We strongly recommend you to **freeze features** after reaching this milestone. As this is a release candidate, it should have all the features you intend to release at v1.5. Adding more features after this point is risky. The remaining time should be left aside for fixing problems discovered late.  

### v1.5rc Product

* As before, you can continue to add more enhancements.
* Also, consider increasing code coverage by adding more tests if it is lower than the level you would like it to be. Take note of <trigger trigger="click" for="modal:v15rc-testingExpectations">our expectation on test code</trigger>. 
* After you have sufficient code coverage, fix remaining code quality problems and bring up the quality to your target level.

<modal title="Admin &raquo; Project Asessement &rarr; Expectation on testing" id="modal:v15rc-testingExpectations">
  <include src="project-testing.md#expectations"/>
</modal>

<panel header=":bulb: Tips: how to score high for code quality" no-close>

* Ensure your code has at least some evidence of these (see [here](../book/errorHandling/index.html) for more info)
  * logging
  * exceptions
  * assertions
  * defensive coding
  
* Ensure there are no [coding standard](https://oss-generic.github.io/process/codingStandards/CodingStandard-Java.html) violations %%&nbsp;e.g. all boolean variables/methods sounds like booleans%%. Checkstyle can prevent only _some_ coding standard violations; others need to be checked manually.

* Ensure [SLAP](../book/codeQuality/maximiseReadability/intermediate/index.html) is applied at a reasonable level. Long methods or deeply-nested code are symptoms of low-SLAP and may be penalized.

* Reduce code duplications %%&nbsp;i.e. if there multiple blocks of code that vary only in minor ways, try to extract out similarities into one place%%, especially in test code. 

* In addition, tyr to apply as many of the <trigger trigger="click" for="modal:v15-codeQuality">code quality guidelines covered in the module</trigger> as you can.

</panel>

<modal large title="Textbook &raquo; Implementation &rarr;" id="modal:v15-codeQuality">
  <include src="../book/codeQuality/index.md"/>
</modal>

**Submission**: as before.

**Grading**: as before.

### v1.5rc Documentation

Update to match the product.

<tip-box type="important"> 

**Each member must create a _Project Portfolio_ page** to describe your contribution to the project. 

</tip-box>

<tip-box> 

<div id="project-portfolio">

#### Project Portfolio Page (PPP)

* **Objective:** 
  * For you to use (e.g. in your resume) as a well-documented data point of your SE experience 
  * For us to use as a data point to evaluate your contributions to the project and your documentation skills

* **What to include:**
  * Main things to include: 
    * links to collated code
    * features you implemented %%&nbsp;(include relevant extracts from the user guide and the developer guide)%%
    * features you propose to implement in future %%&nbsp;(include relevant extracts from the user guide and the developer guide if applicable)%%<br>
      Note: the purpose of allowing you to include _proposed_ features is to provide you more flexibility to show your documentation skills. %%&nbsp;e.g. you can bring in a proposed feature just to give you an opportunity to use a UML diagram type not used by the actual features.%%
    * other significant contributions to the project %%&nbsp;e.g. tweaks to existing features, setting up project tools%%
  * Other things you can include: 
    * Evidence of helping others %%&nbsp;e.g. responses you posted in our forum, bugs you reported in other team's products%%, 
    * Evidence of technical leadership %%&nbsp;e.g. offering features for others to reuse, evidence of those features being reused by others%%
  * If you plan to use the PPP in your Resume, you can also include your SE work outside of the module (will not be graded)

* **Format**:
  * :package: Follow the [example in the AddressBook-Level4](https://nus-cs2103-ay1718s2.github.io/addressbook-level4/team/johndoe.html).
  * :bulb: You can use the [Asciidoc's `include` feature](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/#include-files) to include sections from the developer guide or the user guide in your PPP. Follow the example in the [sample](https://nus-cs2103-ay1718s2.github.io/addressbook-level4/team/johndoe.html). 
  * :exclamation: It is assumed that sections _included_ in this way were written primarily by you. If those sections were written by someone else %%&nbsp;e.g. someone else wrote described the feature in the User Guide but you implemented the feature%%, clearly state that the section was written by someone else %%&nbsp;(e.g. `Start of Extract [from: User Guide] written by Jane Doe`)%%. %%&nbsp;Reason: Your writing skills will be evaluated based on the PPP%%

</div>
</tip-box>

**Submission**: Must be included in the version tagged `v1.5rc`. 

### v1.5rc Demo

* Objective: to serve as a rehearsal for the final project demo at v1.5
* Duration: ~3 minutes (max) per person %%&nbsp; a 4-member team will have 12 minutes%%
* Organize the demo to present a cohesive picture of the product as a whole. Unlike in v1.2-v1.4 demos, there is no need for each person to demo their own features.
* ==Cover all features==, not just the ones added in the recent iteration.
* It ==should be a 'well prepared' demo==. You should know in advance exactly what you'll do in the demo.
* It is ==a _sitting down_ demo==: You'll be demonstrating the features using the TV while sitting down.
* It will be uninterrupted demo: The tutor will not interrupt you during the demo. That means you should finish within the given time.
* The app should be populated with a significant amount of realistic data at the start. e.g at least 20 contacts.
