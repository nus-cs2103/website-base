<div id="title">

## Project → mid-v1.2 [week 8]
</div>
<div id="body">

Given below are some recommended progress for you to achieve in the various aspects of the project.

<div id="product">

**<big>Project Management:</big>**

* :busts_in_silhouette: Fix any errors in org/repo set up %%&nbsp;(e.g. wrong repo name)%%.

* Set up [auto-publishing of docs](https://nus-cs2103-ay1718s2.github.io/addressbook-level4/UsingTravis.html#enabling-auto-publishing-of-documentation)

* **If tests are causing too much pain ...**

  Automated tests have benefits, but they can be a pain to write/maintain; GUI tests are especially hard to maintain because their behavior can sometimes depend on things such as the OS, resolution etc.
  
  It is OK to get rid of some of the troublesome tests and rely more on manual testing instead. The less automated test coverage you have, the higher the risk of regressions; but it may be an acceptable trade-off under the circumstances if tests are slowing you down too much. There is no direct penalty for removing GUI tests.
  
  Also note <trigger trigger="click" for="modal:v12-testingExpectations">our expectation on test code</trigger>. 

<modal title="Admin {{ icon_embedding }} Project Asessement → Expectation on testing" id="modal:v12-testingExpectations">
  <include src="project-testing.md#expectations"/>
</modal>

**Product:**

Each member should try to add some enhancements that are in line with the vision for v2.0. Preferably, these enhancements ==should go beyond the component you are in charge of==, touching as many other components as possible. Refer to the AddressBook-Level4 Developer Guide has [some guidance on how to implement a new feature end-to-end](https://nus-cs2103-ay1718s2.github.io/addressbook-level4/DeveloperGuide.html#creating-a-new-command-code-remark-code).

**Objective**: To familiarize yourself with at least one component the code.

**Description**: Divide the <tooltip content="components as stated in the [Developer Guide: Architecture]">components</tooltip> among yourselves. Each member can do some small enhancements to their component(s) to learn the code of that component. Some suggested enhancements are given in the [AddressBook-Level4 developer guide](https://nus-cs2103-AY1718S2.github.io/addressbook-level4/DeveloperGuide.html#improving-each-component).

:exclamation: Before you start coding, please read our reuse policy given below, in particular, ==how to give credit when you reuse code from Internet or classmates==:

<panel type="seamless" header="%%Admin {{ icon_embedding }} Appendix B: Policies → Policy on Reuse%%">
  <include src="appendixB-policies.md#policy-reuse" />
</panel><p/>

**Submission**: Create PRs from your own fork to your team repo. Get it merged by following your team's workflow.

</div>
<div id="documentation">

**Documentation:** Update the following pages in your project repo:  

</div>

* **README.adoc** page: Update it to match your project. 
  * Add a UI mockup of your intended final product.   
    Note that the ==image of the UI should be `docs/images/Ui.png`== so that it can be downloaded by our scripts.  
  * The original `README.adoc` file (which doubles as the landing page of your project website) is written to read like the introduction to an SE learning/teaching resource. You should ==restructure this page to look like the home page of a real product== (not a school project) targeting real users %%&nbsp;e.g. remove references to addressbook-level3, Learning Outcomes etc. mention target users, add a marketing blurb etc.%% On a related note, also remove `Learning Outcomes` link and related pages.
  * Acknowledge the original source of the code i.e. AddressBook-Level4 project created by SE-EDU initiative at `https://github.com/se-edu/`

</div>

</div>