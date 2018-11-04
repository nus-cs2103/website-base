{% macro show_main_text() %}
<div id="main">

Here is a list of main deliverables of the project; their details are given in the subsequent sections.
* Product
  * [Executable](#deliverable-executable)
  * [Source code](#deliverable-source-code)
* Documentation
  * [User Guide](#deliverable-user-guide-ug)
  * [Developer Guide](#deliverable-developer-guide-dg)
  * [Product Website](#deliverable-product-website)
  * [Project Portfolio Page](#deliverable-project-portfolio-page-ppp)
* [Product Demo](#deliverable-demo)
* [Practical Exam Dry Run](#deliverable-practical-exam-dry-run)
* [Practical Exam](#deliverable-practical-exam)
  * Peer testing results
  * Peer evaluation


### Deliverable: Executable
<span id="project-deliverables-executable">

* The product should be delivered as an executable jar file.
* Ideally, the product delivered at v1.4 should be a <tooltip content=" i.e., it can be used by end-users">_releasable_</tooltip> product. However, in the interest of lowering your workload, we do not penalize if the product is <tooltip content="i.e., the product is not usable by end-users because some essential features are missing">not releasable</tooltip>, ==as long as the product is <tooltip content="i.e., the features it has can be tested from an end-user perspective">_acceptance testable_</tooltip>==.
</span>

### Deliverable: Source code
<span id="project-deliverables-sourcecode">

* The source code should match the executable, and should include the revision history of the source code, as a Git repo.
</span>


### Deliverable: User Guide (UG)
<span id="project-deliverables-ug">

* The User Guide (UG) of the product should match the proposed v2.0 of the product and in sync with the current version of the product.
* Features not implemented yet should be clearly marked as `Coming in v2.0`
* Ensure the UG matches the product precisely, as it will be used by peer testers (and ==any inaccuracy in the content will be considered bugs==).
</span>


### Deliverable: Developer Guide (DG)
<span id="project-deliverables-dg">

* The Developer Guide (DG) of the product should match the proposed v2.0 of the product and should be in sync with the current version of the product.
* :exclamation: **The appendix named _Instructions for Manual Testing_** of the Developer Guide should include testing instructions to **cover all your major and minor enhancements**. There is no need to add testing instructions for existing features if you did not touch them.<br>
  :bulb: What to include in the appendix _Instructions for Manual Testing_? This appendix is meant to give some guidance to the tester to chart a path through the features, and provide some important test inputs the tester can copy-paste into the app. There is no need to give a long list of test cases including all possible variations. It is upto the tester to come up with those variations. However, if the instructions are inaccurate or deliberately misses/mis-states information to make testing harder %%&nbsp;i.e. annoys the tester%%, the tester can report it as a bug %%&nbsp;(because flaws in developer docs are considered as bugs)%%.
* Ensure the DG matches the product precisely, as it will be used by peer evaluators (and ==any inaccuracy in the content will be considered bugs==).
    
</span>


### Deliverable: Product Website
<span id="project-deliverables-website">

* Include an updated version of the online UG and DG that match v1.4 executable
* README : ==Ensure the `Ui.png` matches the current product==
* AboutUs : Ensure the following:
  * Use a suitable profile photo
<div id="profile-photo" class="indented-level2">

* The purpose of the profile photo is for the teaching team to identify you. Therefore, you should choose a recent individual photo showing your face clearly (i.e., not too small) -- somewhat similar to a passport photo. Some examples can be seen in the 'Teaching team' page. Given below are some examples of good and bad profile photos.<br>
  <img src="{{baseUrl}}/admin/images/profilephotos.png" style="width: 365.33px">

* If you are uncomfortable posting your photo due to security reasons, you can post a lower resolution image so that it is hard for someone to misuse that image for fraudulent purposes. If you are concerned about privacy, you can request permission to omit your photo from the page by writing to prof.

</div>

  * Contains a ==link to each person's Project Portfolio page== 
  * Team member ==names match full names used by IVLE==
  
    
</span>

### Deliverable: Project Portfolio Page (PPP)
<span id="project-deliverables-ppp">

At the end of the project each student is required to submit a _Project Portfolio Page_.

* **Objective:** 
  * For you to use %%&nbsp;(e.g. in your resume)%% as a well-documented data point of your SE experience 
  * For us to use as a data point to evaluate your,
    * contributions to the project
    * your documentation skills

* **Sections to include:**
  * **Overview**: A short overview of your product to provide some context to the reader.
  * **Summary of Contributions**:
    * **Code contributed**: Give a link to your code on [Project Code Dashboard](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/{{ module | lower }}-dashboard), which should be `https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/{{ module | lower }}-dashboard/#=undefined&search=YourGithubUserName` (==replace `YourGithubUserName` with your actual username==).
    * **Main feature implemented:** A summary of the main feature (the so called _major enhancement_) you implemented
    * **Other contributions:**
      * Other _minor_ enhancements you did which are not related to your _main_ feature
      * Contributions to project management %%e.g., setting up project tools, managing releases, managing issue tracker etc.%%
      * Evidence of helping others %%e.g. responses you posted in our forum, bugs you reported in other team's products%%,
      * Evidence of technical leadership %%e.g. sharing useful information in the forum%%

  * **Contributions to the User Guide**: Reproduce the parts in the User Guide that you wrote. This can include features you implemented as well as features you propose to implement.<br>
    %%The purpose of allowing you to include _proposed_ features is to provide you more flexibility to show your documentation skills. e.g. you can bring in a proposed feature just to give you an opportunity to use a UML diagram type not used by the actual features.%%
  * **Contributions to the Developer Guide**: Reproduce the parts in the Developer Guide that you wrote. Ensure there is enough content to evaluate your technical documentation skills and UML modelling skills. You can include descriptions of your design/implementations, possible alternatives, pros and cons of alternatives, etc.

  * If you plan to use the PPP in your Resume, you can also include your SE work outside of the module (will not be graded)

* **Format**:
  * File name: `docs/team/GitHubUserName.adoc` e.g., `docs/team/JamesTan2001.adoc`
  * {{ icon_example }} Follow the [example in the AddressBook-Level4](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/addressbook-level4/team/johndoe.html), but ignore the following two lines in it.<br>
      >* **Minor enhancement:** added a history command that allows the user to navigate to previous commands using up/down keys.
      >* **Code contributed:** [[Functional code]()] [[Test code]()] _{give links to collated code files}_

  * :bulb: You can use the [Asciidoc's `include` feature](http://asciidoctor.org/docs/asciidoc-syntax-quick-reference/#include-files) to include sections from the developer guide or the user guide in your PPP. Follow the example in the [sample](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/addressbook-level4/team/johndoe.html).

  * =={{ icon_important_big_red }} It is assumed that all contents in the PPP were written primarily by you.== If any section is written by someone else %%&nbsp;e.g. someone else wrote described the feature in the User Guide but you implemented the feature%%, clearly state that the section was written by someone else %%&nbsp;(e.g. `Start of Extract [from: User Guide] written by Jane Doe`)%%. %%&nbsp;Reason: Your writing skills will be evaluated based on the PPP%%

  * Page limit: If you have more content than the limit given below, shorten (or omit some content) so that you do not exceed the page limit. Having too much content in the PPP will be viewed unfavorably during grading. Note: the ==page limits given below are _after_ converting to PDF format==. The actual amount of content you require is actually less than what these numbers suggest because the HTML → PDF conversion adds a lot of spacing around content.
    Content | Limit
    ------- | -----
    Overview + Summary of contributions | 0.5-1
    Contributions to the User Guide | 1-3
    Contributions to the Developer Guide | 3-6
    Total | 5-10

</span>

### Deliverable: Demo
<span id="project-deliverables-demo">

* **Duration:** Strictly `(teamSize x 4) + 2` minutes %%&nbsp;e.g. 22 minutes for a 5-person team.%% Exceeding this limit will be penalized. The extra two minutes is for the first speaker to give an overview of the product.

* **Target audience**: Assume you are giving a demo to a higher-level manager of your company, to brief him/her on the current capabilities of the product. This is the first time they are seeing the new product you developed but they are familiar with the AddressBook-level4 (AB4) product.

* **Scope**: 
  * **Each person should demo the enhancements they added**. However, it's ok for one member to do all the typing.
  * Subjected to the constraint mentioned in the previous point, as far as possible, organize the demo to present a cohesive picture of the product as a whole, presented in a logical order. %%&nbsp;Remember to explain the profile of the target user profile and value proposition early in the demo.%%
  * It is recommended you showcase how the feature improves the user’s life rather than simply describe each feature.
  * No need to cover design/implementation details as the manager is not interested in those details.
  * Mention features you inherited from AB4 only if they are needed to explain your new features. %%&nbsp;Reason: existing features will not earn you marks, and the audience is already familiar with AB4 features.%%

* **Structure:**  
  * Demo the product using the same executable you submitted, on your own laptop, using the TV.  
  * It can be **a _sitting down_ demo**: You'll be demonstrating the features using the TV while sitting down. But you may stand around the TV if you prefer that way.
  * It will be an uninterrupted demo: The audience members will not interrupt you during the demo. That means you should finish within the given time.
  * The demo should use a sufficient amount of <tooltip content="`Mr aaa` is not a realistic person name">_realistic_</tooltip> demo data. %%&nbsp;e.g at least 20 contacts%%. Trying to demo a product using just 1-2 sample data creates a bad impression.
  * **Dress code** : The level of formality is up to you, but it is recommended that the whole team dress at the same level.
    
* **Optimizing the time:** 
  * Spend as much time as possible on demonstrating the actual product. Not recommended to use slides (if you do, use them sparingly) or videos or lengthy narrations.  
   Avoid skits, re-enactments, dramatizations etc. This is not a sales pitch or an informercial. While you need to show how a user use the product to get value, but you don’t need to act like an imaginary user. For example, [Instead of this] `Jim get’s a call from boss. "Ring ring", "hello", "oh hi Jim, can we postpone the meeting?" "Sure". Jim hang up and curses the boss under his breath. Now he starts typing ..etc.` [do this] `If Jim needs to postpone the meeting, he can type …`
    It’s not that dramatization is bad or we don’t like it. We simply don’t have enough time for it.  
    Note that CS2101 demo requirements may differ. Different context → Different requirements.  
  * Rehearse the steps well and ensure you can do a smooth demo. Poor quality demos can affect your grade.
  * Don’t waste time repeating things the target audience already knows. e.g. no need to say things like "We are students from NUS, SoC". 
  * Plan the demo to be in sync with the impression you want to create. For example, if you are trying to convince that the product is easy to use, show the easiest way to perform a task before you show the full command with all the bells and whistles.
  * Limit the demo to CLI inputs only. Do not explain GUI inputs because they don't earn marks.

</span>

### Deliverable: Practical Exam (Dry Run)

<span id="project-deliverables-practicalexam-dry-run">

**What**: The v1.3 is subjected to a round of peer _acceptance/system testing_, also called the _Practical Exam Dry Run_ as this round of testing will be similar to the graded <trigger trigger="click" for="modal:projectDeliverablesPeDryRun-pe">Practical Exam that will be done at v1.4</trigger>.

**When, where**: uses a 30 minute slot at the start of week 11 lecture

<modal large title="Admin {{ icon_embedding }} Project → Deliverables → Practical Exam" id="modal:projectDeliverablesPeDryRun-pe">
  <include src="project-deliverables.md#project-deliverables-practicalexam"/>
</modal>

{{ icon_important_big_red }} **Grading**: Taking part in the PE dry run is strongly encouraged as it ==can affect your grade in the following ways==.
* If the product you are allocated to test in the Practical Exam (at v1.4) had a very low bug count, we will consider your performance in PE dry run as well when grading the PE.
* PE dry run will help you practice for the actual PE.
* Taking part in the PE dry run will earn you participation points.
* There is ==no penalty for bugs reported== in your product. Every bug you find is a win-win for you and the team whose product you are testing.

**Objectives**:
* **To train you** to do manual testing, bug reporting, bug <tooltip content="assigning of priority order">triaging,</tooltip> bug fixing, communicating with users/testers/developers, evaluating products etc.
* **To help you improve your product** before the final submission.

<include src="project-testing.mbdf#testingPreparations" />

**During the session**:
1. **Take note of your team to test**. Distributed via IVLE gradebook and via email.
1. Download the latest jar file from the team's GitHub page. ==Copy it to an empty folder==.
1. Confirm you are testing the allocated product by comparing the product UI with the UI screenshot sent via email.

<div id="project-deliverables-pe-testing-intructions">
<box>

##### Testing instructions for PE and PE Dry Run

* **What to test**:
  * PE Dry Run (at **v1.3**):
    * Test the product ==based on the User Guide== (the UG is most likely accessible using the `help` command).
    * Do ==_system_ testing first== %%i.e., does the product work as specified by the documentation?%%. If there is time left, you can ==do _acceptance_ testing as well== %%i.e., does the product solve the problem it claims to solve?%%.
  * PE (at **v1.4**):
    * Test ==based on the Developer Guide== (Appendix named _Instructions for Manual Testing_) ==and the User Guide==. The testing instructions in the Developer Guide can provide you some guidance but if you follow those instructions strictly, you are unlikely to find many bugs. You can deviate from the instructions to probe areas that are more likely to have bugs.
    * Do ==_system testing only_== %%i.e., verify actual behavior against documented behavior%%. Do not do _acceptance testing_.

* **What not to test**:
  * Omit features that are driven by GUI inputs (e.g. buttons, menus, etc.) %%Reason: Only CLI-driven features can earn credit, as per given project constraints.%% Some features might have both a GUI-driven and CLI-driven ways to invoke them, in which case test only the CLI-driven way of invoking it.
  * Omit feature that existed in AB-4.

* **These are considered _bugs_**:
  * Behavior differs from the User Guide
  * A legitimate user behavior is not handled %%e.g. incorrect commands, extra parameters%%
  * Behavior is not specified and differs from normal expectations %%e.g. error message does not match the error%%
  * Problems in the User Guide e.g., missing/incorrect info

* **Where to report bugs**: Post bug in the following issue trackers (==not in the team's repo==):
  * PE Dry Run (at **v1.3**): [nus-{{ module | lower }}-{{ semester }}/**pe-dry-run**]({{module_org}}/pe-dry-run/issues).
  * PE (at **v1.4**): [nus-{{ module | lower }}-{{ semester }}/**pe**]({{module_org}}/pe/issues).

* **Bug report format**:
  * {{ icon_important_big_red }} Post bugs as you find them %%(i.e., do not wait to post all bugs at the end)%% because the issue tracker will close exactly at the end of the allocated time.
  * ==Do not use team ID in bug reports==. %%Reason: to prevent others copying your bug reports%%
  * Each bug should be a separate issue.
  * Write good quality bug reports; ==poor quality or incorrect bug reports will not earn credit==.
  * Use a descriptive title.
  * Give a good description of the bug with ==steps to reproduce and screenshots==.
  * Assign a severity to the bug report. Bug report without a priority label are considered `severity.Low` (lower severity bugs earn lower credit):

<div class="indented-level4">
<include src="appendixE-gitHub.md#bug-severity" />
</div>

* **About posting _suggestions_:**
  * PE Dry Run (at **v1.3**): You can also post suggestions on how to improve the product. :bulb: Be diplomatic when reporting bugs or suggesting improvements. For example, instead of criticising the current behavior, simply suggest alternatives to consider.
  * PE (at **v1.4**): Do not post suggestions.

* **If the product doesn't work at all:** If the product fails catastrophically %%e.g., cannot even launch%%, you can test the _fallback_ team allocated to you. But in this case ==you must inform us immediately after the session== so that we can send your bug reports to the correct team.

</box>
</div>

<modal large title="Admin {{ icon_embedding }} Project →" id="modal:v1.3-ppp">
  <include src="project-deliverables.md#project-deliverables-ppp"/>
</modal>

**After the session**:
* We'll transfer the relevant bug reports to your repo over the weekend. Once you have received the bug reports for your product, it is up to you to decide whether you will act on reported issues before the final submission v1.4. For some issues, the correct decision could be to reject or postpone to a version beyond v1.4.
* You can post in the issue thread to communicate with the tester %%e.g. to ask for more info%%, etc. However, the tester is not obliged to respond.
  * :bulb: Do not argue with the issue reporter to try to convince that person that your way is correct/better. If at all, you can gently explain the rationale for the current behavior but do not waste time getting involved in long arguments. If you think the suggestion/bug is unreasonable, just thank the reporter for their view and close the issue.

</span>

### Deliverable: Practical Exam

<span id="project-deliverables-practicalexam">

**Objectives:**
* Evaluate your manual testing skills, product evaluation skills, effort estimation skills
* Peer-evaluate your product design %%{{ icon_team }}%%, implementation effort %%{{ icon_individual }}%%, documentation quality %%{{ icon_individual }}%%

**When, where**: Week 13 lecture

{{ icon_important_big_red }} **Grading**:
* Your performance in the practical exam will be considered for your final grade (under the _QA_ category and under _Implementation_ category, about 10 marks in total).
* You will be graded based on your effectiveness as a tester (e.g., the percentage of the bugs you found, the nature of the bugs you found) and how far off your evaluation/estimates are from the evaluator consensus. %%Explanation: we understand that you have limited expertise in this area; hence, we penalize only if your inputs don't seem to be based on a sincere effort to test/evaluate.%%
* The bugs found in your product by others will affect your v1.4 marks. You will be given a chance to reject false-positive bug reports.

<include src="project-testing.mbdf#testingPreparations" />

**During:** 

1. **Take note of your team to test**. It will be given to you by the teaching team (distributed via IVLE gradebook).
1. **Download from IVLE all files** submitted by the team %%(i.e. jar file, User Guide, Developer Guide, and Project Portfolio Pages)%% ==into an empty folder==.
1. **[~40 minutes] Test the product and report bugs** as described below:

<div class="indented-level2">
  <include src="project-deliverables.md#project-deliverables-pe-testing-intructions" />
</div>

1. **[~50 minutes] Evaluate the following aspects.** Note down your evaluation in a hard copy (as a backup). Submit via TEAMMATES.
  
   * **A. Cohesiveness of product features** [{{ icon_team }}]: Do the features fit together and match the stated target user and the value proposition?
     * `unable to judge`: You are unable to judge this aspect for some reason.
     * `low`: One of these
       * target user is too general %%&nbsp;i.e. wider than AB4%%
       * target user and/or value proposition not clear from the user guide
       * features don't seem to fit together for the most part
     * `medium`: Some features fit together but some don't.
     * `high`: All features fit together but the features are not very high value to the target user.
     * `excellent`: The target user is clearly defined (not too general) and almost all new features are of high-value to the target user. i.e. the product is very attractive to the target user.

   * **B. Quality of user docs** [{{ icon_individual }}]: Evaluate based on the parts of the user guide written by the person, as reproduced in the project portfolio.  ==Evaluate from an end-user perspective.== 
     * `unable to judge`: Less than 1 page worth of UG content written by the student.
     * `low`: Hard to understand, often inaccurate or missing important information.
     * `medium`: Needs some effort to understand; some information is missing.
     * `high`: Mostly easy to follow. Only a few areas need improvements.
     * `excellent`: Easy to follow and accurate. Just enough information, visuals, examples etc. (not too much either).

   * **C. Quality of developer docs** [{{ icon_individual }}]: Evaluate based on the developer docs cited/reproduced in the respective project portfolio page. ==Evaluate from the perspective of a new developer trying to understand how the features are implemented.==
     * `unable to judge`: One of these
       * no content at all.
       * less than 0.5 pages worth of content.
       * other problems in the document %%&nbsp;e.g. looks like included wrong content%%.
     * `low`: One of these
       * Very small amount of content (i.e., 0.5 - 1 page).
       * Hardly any use to the reader (i.e., content doesn't make much sense or redundant).
       * Uses ad-hoc diagrams where UML diagrams could have been used instead.
       * Multiple notation errors in UML diagrams.
     * `medium`: _Some_ diagrams, _some_ descriptions, but does not help the reader that much %%&nbsp;e.g. overly complicated diagrams%%.
     * `high`: Enough diagrams (at lest two kinds of UML diagrams used) and enough descriptions (about 2 pages worth) but explanations are not always easy to follow.
     * `excellent`: Easy to follow. Just enough information (not too much). Minimum repetition of content/diagrams. Good use of diagrams to complement text descriptions. Easy to understand diagrams with just enough details rather than very complicated diagrams that are hard to understand.

   * **D. Depth of feature** [{{ icon_individual }}]: Evaluate the feature done by the student for difficulty, depth, and completeness. Note: examples given below assume that AB4 did not have the commands `edit`, `undo`, and `redo`.
     * `unable to judge`: You are unable to judge this aspect for some reason.
     * `low` : An easy feature %%&nbsp;e.g. make the existing _find_ command case insensitive%%.
     * `medium` : Moderately difficult feature, barely acceptable implementation %%&nbsp;e.g. an _edit_ command that requires the user to type _all_ fields, even the ones that are not being edited%%.
     * `high`: One of the below
       * A moderately difficult feature but fully implemented %%&nbsp;e.g. an _edit_ command that allows editing any field%%.
       * A difficult feature with a reasonable implementation but some aspects are not covered %%&nbsp;undo/redo command that only allows a single undo/redo%%.
     * `excellent`: A difficult feature, all reasonable aspects are fully implemented %%&nbsp;undo/redo command that allows multiple undo/redo%%.

   * **E. Amount of work** [{{ icon_individual }}]:  Evaluate the amount of work, on a scale of 0 to 30.
     * Consider [this PR (`history` command)](https://github.com/se-edu/addressbook-level4/pull/440/files) as 5 units of effort which means [this PR (`undo/redo` command)](https://github.com/se-edu/addressbook-level4/pull/610/files) is about 15 points of effort. Given that 30 points matches an effort twice as that needed for the `undo/redo` feature (which was given as an example of an `A` grade project), we expect most students to be have efforts lower than 20.
     * Consider ==the _main feature_ only==. Exclude GUI inputs, but consider GUI outputs of the feature. Count all implementation/testing/documentation work as mentioned in that person's portfolio page. Also look at the actual code written by the person. We understand that it is not possible to know exactly which part of the code is for the main feature; make a best guess judgement call based on the available info.
     * {{ icon_important_big_red }} Do not give a high value just _to be nice_. If your estimate is wildly inaccurate, it means you are unable to estimate the effort required to implement a feature in a project that you are supposed to know well at this point. ==You will lose marks if that is the case.==

**Bug Review Period**:

There will be a review period for you to respond to the [bug reports]({{module_org}}/pe-results/issues) you received.

Duration: The review period will start around 1 day after the PE (exact time to be announced) and will last until the following **Wednesday midnight**. 

Bug reviewing is recommended to be done as a team as some of the decisions need team consensus.

<tip-box> 

**Instructions for Reviewing Bug Reports**

* **First, don't freak out if there are lot of bug reports.** Many can be duplicates and some can be _false positives_. In any case, we anticipate that all of these products will have some bugs and our penalty for bugs is not harsh. Furthermore, it depends on the severity of the bug. Some bug may not even be penalized.

* **Do not edit the subject or the description. Do not close bug reports.** Your response (if any) should be added as a comment.

* **If the bug is reported multiple times**, mark all copies EXCEPT one as duplicates using the `duplicate` tag (if the duplicates have different severity levels, you should ==keep the one with the highest severity==). In addition, use [this technique](https://help.github.com/articles/about-duplicate-issues-and-pull-requests/) to indicate which issue they are duplicates of.  Duplicates can be omitted from processing steps given below.

* **If a bug seems to be for a different product** (i.e. wrongly assigned to your team), let us know (email prof).

* **Decide if it is a real bug and apply ONLY one of these labels**.

<div class="indented">
<box>

Response Labels:
* `response.Accepted`: You accept it as a bug.
* `response.Rejected`: What tester treated as a bug is in fact the expected behavior. {{ icon_important_big_red }} The penalty for rejecting a bug using an unjustifiable explanation is higher than the penalty if the same bug was accepted. You can reject bugs that you inherited from AB4.
* `response.CannotReproduce`: You are unable to reproduce the behavior reported in the bug after multiple tries.
* `response.IssueUnclear`: The issue description is not clear.

</box>
</div>

* If applicable, **decide the type of bug**. Bugs without `type-` are considered `type-FunctionalityBug` by default (which are liable to a heavier penalty):

<div class="indented">
<box>

Bug Type Labels:
* `type-FunctionalityBug` : the bug is a flaw in how the product works.
* `type-DocumentationBug` : the bug is in the documentation.

</box>
</div>

* **If you disagree with the original severity assigned to the bug**, you may change it to the correct level, in which case add a comment justifying the change. All such changes will be double-checked by the teaching team and unreasonable lowering of severity will be penalized extra.:

<div class="indented">
  <include src="appendixE-gitHub.md#bug-severity" />
</div>

* **Decide who should fix the bug**. Use the `Assignees` field to assign the issue to that person(s). There is no need to actually fix the bug though. It's simply an indication/acceptance of responsibility. **If there is no assignee, we will distribute the penalty for that bug (if any) among all team members.**

* **Add an explanatory comment** explaining your choice of labels and assignees.

</tip-box>

</span>

### Notes for Those Using AB-2 or AB-3 for the Project
<span id="notes-for-ab23">

There is no explicit penalty for switching to a lower level AB. All projects are evaluated based on the same yardstick irrespective of on which AB it is based. As an AB is given to you as a 'free' head-start, a lower level AB gives you a shorter head-start, which means your final product is likely to be less functional than those from teams using AB-4 unless you progress faster than them. Nevertheless, you should switch to AB2/3 if you feel you can learn more from the project that way, as our goal is to maximize learning, not features.<br>
  If your team wants to stay with AB-4 but you want to switch to a lower level AB, let the us know so that we can work something out for you.

If you have opted to use AB-2 or AB-3 instead of AB-4 as the basis of your product, please note the following points:
* Set up [auto-publishing of documentation similar to AB-4](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/addressbook-level4/UsingTravis.html#enabling-auto-publishing-of-documentation)
* Add Project Portfolio Pages (PPP) for members, similar to the example provided in AB-4
* You can convert UG, DG, and PPP into pdf files using [instructions provided in AB-4 DG](https://nus-{{ module | lower }}-{{ semester | lower }}.github.io/addressbook-level4/DeveloperGuide.html#converting-documentation-to-pdf-format)
* Create an _About Us_ page similar to AB-4 and update it as described in <trigger trigger="click" for="modal:deliverables-midv11">mid-v1.1 progress guide</trigger>

<modal large title="Admin {{ icon_embedding }} Project: mid-v1.1" id="modal:deliverables-midv11">
  <include src="project-w06-mid-v11.md#body"/>
</modal>

</span>

</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-deliverables", show_main_text) }}
