<tip-box> 

**v1.4 Summary of Milestone**

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
:bust_in_silhouette: Contributed code to v1.4 | code merged
:bust_in_silhouette: Code collated | as stated
:busts_in_silhouette: v1.4 jar file released properly on GitHub | as stated
:busts_in_silhouette: v1.4 milestone properly wrapped up on GitHub | as stated
:busts_in_silhouette: Documentation updated to match v1.4 | at least the User Guide and the `README.adoc` is updated

</tip-box>

### v1.4 Project Management

<tip-box type="important">

You are required to <tooltip content="extract your own code and put in one file">collate</tooltip> code at this milestone. %%&nbsp;Reason: You will be required to collated code at your final submission. As an early preparation for that, we require you to collate code once at v1.4 so that you can iron out any code collation glitches early.%% 

</tip-box>

<panel header="**How to collate code for grading**">
  <include src="collate.md" />
</panel><p/>

### v1.4 Product

As before, move the product towards v2.0.

**Submission**: Push the code (==including the `collated` folder== and files created above) to GitHub.

### v1.4 Documentation

<tip-box type="important"> 

v1.4 user guide should be updated to match the current version of the product. %%&nbsp;Reason: v1.4 will be subjected to a trial _acceptance testing_ session%%
  
</tip-box>

* **README page**: Update to look like a real product (rather than a project for learning SE) if you haven't done so already. In particular,
  * ==Describe the profile of the target user==
  * Remove irrelevant content such as _Learning Outcomes_
  * ==Update the `Ui.png` to match the current product==
  
* **User Guide**: ==This document will be used by acceptance testers==. Update to match the current version. In particular,
  * Clearly indicate which features are not implemented yet %%&nbsp;e.g. tag those features with a `Coming in v2.0`%%. 
  * For those features already implemented, ensure their description match the exact behavior of the product %%&nbsp;e.g. replace mockups with actual screenshots%% 
 
* **Developer Guide**: As before, update if necessary.
  
* **AboutUs page**: Update to reflect current state of roles and responsibilities.  

**Submission**: Must be included in the version tagged `v1.4`.


### v1.4 Demo

As before.


### v1.4 Testing

v1.4 is subjected to a round of _peer testing_.

**Objectives**:
* **To train you** to do manual testing, bug reporting, bug <tooltip content="assigning of priority order">triaging</tooltip>, bug fixing, communicating with users, evaluating products etc. 
* **To help you improve your product** before the final submission.
  
**When, where**: 
* To be done **during Lecture 11** (but you can do it from anywhere, not necessarily lecture venue). Suggested duration: **30 minutes** (we'll stop the lecture for a 30 minute block for you do do the testing).

**During the session**:
* Each student will be assigned a product from another team to test.
* Download the latest jar file from the team's GitHub page. ==Copy it to an empty folder==. 
* Test the product based on the user guide. First, _acceptance test_ it from the perspective of the target user profile. If there is any time left, you can switch to _system testing_ mode.
* Post bugs you find in the team's issue tracker. 
  * Each bug should be a separate issue.
  * Even problems in the user guide %%&nbsp;e.g. lack of explanations%% can be posted as issues.
  * Feel free to ==post other suggestions for improvements== too %%&nbsp;e.g. ways to improve the command format%%.
* ==Do not use the session time to read bug reports your team is receiving.==
* Before posting a report/suggestion, check if it is already posted by someone else. If it is, post in the same thread to confirm/support the issue and add your input.
* Use descriptive titles for the issues. Give a good description of the bug/suggestion, including steps required to reproduce.
  * :bulb: Be diplomatic when reporting bugs or suggesting improvements. For example, instead of criticising the current behavior, simply suggest alternatives to consider.
  
**Grading**:
* Considered for phase B participation. In addition, issues you created can be include it in your <trigger trigger="click" for="modal:v1.4-ppp">project portfolio page</trigger> to show how you contributed to another project.
* There is **no penalty for bugs reported** in your product.
  
<modal large title="Admin &raquo; Project &rarr;" id="modal:v1.4-ppp">
  <include src="project-v15rc.md#project-portfolio"/>
</modal>
  
<include src="project-testing.md#testingPreparations" />
  
**After the session**:
* It is up to you to decide whether you will act on reported issues before the final submission v1.5. For some issues, the correct decision could be to reject or postpone.
* You can post in the issue thread to communicate with the tester %%&nbsp;e.g. to ask for more info%%, etc. However, the tester is not obliged to respond.
  * :bulb: Do not argue with the issue reporter to try to convince that person that your way is correct/better. If at all, you can gently explain the rationale for the current behavior but do not waste time getting involved in long arguments. If you think the suggestion/bug is unreasonable, just thank the reporter for their view and close the issue.