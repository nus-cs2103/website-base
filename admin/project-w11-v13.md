{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<p class="lead" style="color: purple"><md>{{ far_calendar_check }} <include src="project-timeline.md#v13-overview" inline /></md></p>

**v1.3 Summary of Milestone**

Milestone | Minimum acceptable performance to consider as 'reached'
--------- | -------------------------------------------------------
{{ icon_individual }} Contributed code to v1.3 | code merged
{{ icon_individual }} Code is RepoSense-compatible | as stated in mid-v1.3
{{ icon_team }} v1.3 jar file released on GitHub | as stated
{{ icon_team }} v1.3 milestone properly wrapped up on GitHub | as stated
{{ icon_team }} Documentation updated to match v1.3 | at least the User Guide and the `README.adoc` is updated

### v1.3 Project Management

Ensure your code is RepoSense-compatible, <trigger trigger="click" for="modal:v13-reposense">as explained in mid-v1.3</trigger>.

<modal large title="Admin {{ icon_embedding }} Project → v1.3 (extract)" id="modal:v13-reposense">
  <include src="reposenseCompatibility.md" />
</modal>

### v1.3 Product

* As before, move the product towards v2.0.

* {{ icon_important_big_red }} **Do a <tooltip content="resulting in a jar file on GitHub that can be downloaded by potential users">proper product release</tooltip>** [as described in the Developer Guide](https://nus-{{ module | lower }}-{{ semester }}.github.io/addressbook-level4/DeveloperGuide.html#making-a-release). Do some manual tests to ensure the jar file works.

### v1.3 Documentation

<tip-box>

{{ icon_important_big_red }} v1.3 user guide should be updated to match the current version of the product. %%&nbsp;Reason: v1.3 will be subjected to a trial _acceptance testing_ session%%

</tip-box>

* **README page**: Update to look like a real product (rather than a project for learning SE) if you haven't done so already. In particular,
  * ==Describe the profile of the target user==
  * Remove irrelevant content such as _Learning Outcomes_
  * ==Update the `Ui.png` to match the current product==
  
* **User Guide**: ==This document will be used by acceptance testers==. Update to match the current version. In particular,
  * Clearly indicate which features are not implemented yet %%&nbsp;e.g. tag those features with a `Coming in v2.0`%%. 
  * For those features already implemented, ensure their descriptions match the exact behavior of the product %%&nbsp;e.g. replace mockups with actual screenshots%% 
 
* **Developer Guide**: As before, update if necessary.
  
* **AboutUs page**: Update to reflect current state of roles and responsibilities.  

**Submission**: Must be included in the version tagged `v1.3`.


### v1.3 Demo

* Do a quick demo of the main features ==using the jar file==. Objective: demonstrate that the jar file works.


### v1.3 Testing (_aka_ Practical Exam Dry Run)

**When, where**: To be done **during Lecture 11**. Duration: **30 minutes** (we'll stop the lecture for a 30 minute block for you do do the testing).

==The info below are from the previous semester. We'll let you know when the updated instructions are ready.==

Your v1.3 is subjected to a round of peer _acceptance/system testing_, also called the _Practical Exam Dry Run_ as this round of testing will be similar to the graded <trigger trigger="click" for="modal:v13peDryRun-pe">Practical Exam that will be done at v1.4</trigger>.

<modal large title="Admin {{ icon_embedding }} Project → Deliverables" id="modal:v13peDryRun-pe">
  <include src="project-deliverables.md#project-deliverables-practicalexam"/>
</modal>

<box>

{{ icon_important_big_red }} **Taking part in the PE dry run is strongly encouraged as it ==can affect your grade in the following ways==.**
* If the product you are allocated to test in the Practical Exam (at v1.4) had a very low bug count, we will consider your performance in PE dry run as well when grading the PE.
* PE dry run will help you practice for the actual PE.
* Taking part in the PE dry run will earn you participation points.

</box>

**Objectives**:
* **To train you** to do manual testing, bug reporting, bug <tooltip content="assigning of priority order">triaging,</tooltip> bug fixing, communicating with users/testers/developers, evaluating products etc.
* **To help you improve your product** before the final submission.


**During the session**:
* Each student will be assigned a product from another team to test.
* Download the latest jar file from the team's GitHub page. ==Copy it to an empty folder==. 
* Test the product based on the user guide (the UG is most likely accessible using the `help` command). First, _acceptance test_ it from the perspective of the target user profile. If there is any time left, you can switch to _system testing_ mode.
* Post bugs you find in the team's issue tracker. 
  * Each bug should be a separate issue.
  * Even problems in the user guide %%&nbsp;e.g. lack of explanations%% can be posted as issues.
  * Feel free to ==post other suggestions for improvements== too %%&nbsp;e.g. ways to improve the command format%%.
* ==Do not use the session time to read bug reports your team is receiving.==
* Before posting a report/suggestion, check if it is already posted by someone else. If it is, post in the same thread to confirm/support the issue and add your input.
* Use descriptive titles for the issues. Give a good description of the bug/suggestion, including steps required to reproduce.
  * :bulb: Be diplomatic when reporting bugs or suggesting improvements. For example, instead of criticising the current behavior, simply suggest alternatives to consider.

* Issues you created can be included in your <trigger trigger="click" for="modal:v1.3-ppp">project portfolio page</trigger> to show how you contributed to another project.
* There is **no penalty for bugs reported** in your product.
  
<modal large title="Admin {{ icon_embedding }} Project →" id="modal:v1.3-ppp">
  <include src="project-deliverables.md#project-deliverables-ppp"/>
</modal>
  
<include src="project-testing.fr#testingPreparations" />
  
**After the session**:
* It is up to you to decide whether you will act on reported issues before the final submission v1.4. For some issues, the correct decision could be to reject or postpone.
* You can post in the issue thread to communicate with the tester %%&nbsp;e.g. to ask for more info%%, etc. However, the tester is not obliged to respond.
  * :bulb: Do not argue with the issue reporter to try to convince that person that your way is correct/better. If at all, you can gently explain the rationale for the current behavior but do not waste time getting involved in long arguments. If you think the suggestion/bug is unreasonable, just thank the reporter for their view and close the issue.
</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w11-v13", show_main_text) }}