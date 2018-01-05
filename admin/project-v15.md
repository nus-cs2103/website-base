<tip-box> 

* :exclamation: **Penalty for late submission:** ==-1 mark for each hour delayed, up to 3 hours.== Even a 1-second delay is penalized, irrespective of the reason. Penalty for delays beyond 3 hours are determined on a case by case basis. 
  * For submissions done via IVLE, the submission time is the timestamp shown by IVLE.
  * When determining the late submission penalty, **we take the latest submission** even if the same exact file was submitted earlier. Do not submit the same file multiple times if you want to avoid unnecessary late submission penalties.
* The whole team is penalized for problems in team submissions. Only the respective student is penalized for problems in individual submissions. 
* :exclamation: Please **follow submission instructions closely**. ==Any non-compliance will be penalized==. e.g. wrong file name, team member photos not suitable, etc.
* For pdf submissions, ensure the file is usable and hyperlinks in the file are correct. Problems in documents are considered bugs too %%&nbsp;e.g. broken links, outdated diagrams/instructions etc.%%.
* **Do not update the repo during the 14 days after the deadline.** Get our permission first if you need to update the repo during that one-week _freeze_ period. You can continue to evolve your repo after that. 

**Summary of submissions**:

Team/Individual Item | Name format | Upload to
-------------------- | ----------- | ---------
:busts_in_silhouette: Source code |  tag as `v1.5` | GitHub
:busts_in_silhouette: Jar file |  `[team][product name].jar`<br>%%e.g. [T09-B1][ContactsPlus].jar%% | IVLE
:busts_in_silhouette: User Guide | `[TEAM_ID][Project Name]UserGuide.pdf`<br>  %%e.g.[T09-B1][Contacts Plus]UserGuide.pdf%% | IVLE
:busts_in_silhouette: Developer Guide | `[TEAM_ID][Project Name]DeveloperGuide.pdf`<br> %%e.g. [T09-B1][Contacts Plus]DeveloperGuide.pdf%% | IVLE
:busts_in_silhouette: `README.adoc`, `Ui.png`, `AboutUs.adoc` | | GitHub
:bust_in_silhouette: Project Portfolio Page | `[TEAM_ID][Your Name]Portfolio.pdf`<br> %%e.g.[T09-B1][John Doe]Portfolio.pdf%% | IVLE
:bust_in_silhouette: Collated files | | GitHub

</tip-box>


### v1.5 Product

This is as a ‘production release’. It should be at least ‘near production quality’.

**Submission**:

* **Source code**: Push the code to GitHub and tag with the version number. Source code (==including collated .md files==; please ensure the collated `.md` files are up to date; any updates to collated code files after the deadline comes with an automatic penalty) Note that the quality of the code in these ==collated code files accounts for a significant component of your final score==, graded individually.
* **Executable**: See summary of submissions above 
    

**Deadline**: Week 13 Monday 23.59.

**Grading**: 

<include src="project-assessment.md" name="%%Admin » Project: Assessment%%" dynamic />

### v1.5 Documentation

**Submission**:

First, update following pages on GitHub: 
* User Guide, Developer Guide: Ensure these two docs match the product precisely, as these docs will be used by peer testers (and ==any inaccuracy in the content will be reported/penalized as bugs==).
  * :exclamation: in particular, **update the appendix named _Instructions for Manual Testing_** of the Developer Guide to include testing instructions to **cover all your major and minor enhancements**. There is no need to add testing instructions for existing features if you did not touch them.<br>
    :bulb: What to include in the appendix _Instructions for Manual Testing_? This appendix is meant to give some guidance to the tester to chart a path through the features, and provided some important test inputs the tester can copy-paste into the app. There is no need to give a long list of test cases including all possible variations. It is upto the tester to come up with those variations. However, if the instructions are inaccurate or deliberately misses/mis-states information to make testing harder %%&nbsp;i.e. annoys the tester%%, the tester can report it as a bug %%&nbsp;(because flaws in developer docs are considered as bugs)%%.
* README : ==Ensure the `Ui.png` matches the current product==
* AboutUs : Ensure the following:
  * Contains a ==link to each person's Project Portfolio page== 
  * Team member ==names match full names used by IVLE==
* Project Portfolio Pages of each member

Next, convert the following documents to pdf (AB4 dev guide has some instructions on converting project docs to pdf) and upload to IVLE. See _summary of submissions_ above for the file name format for each. 
* User Guide
* Developer Guide
* Project Portfolio Pages

**Deadline**: Same as v1.5 product.

**Grading**: 

<include src="project-assessment.md" name="%%Admin » Project: Assessment%%" dynamic />


### v1.5 Demo

<img src="{{baseUrl}}/admin/images/v05demo.png" style="width: 250px">

* **Venue:** Same as the tutorial venue unless informed otherwise.
* **Schedule:** Your demo timing is same as your tutorial time in week 13.  
    Starting times: `Team B1: 00 minutes, B2: 15 minutes, B3: 30 minutes, B4: 45 minutes`<br>
    At least some team members need to arrive 15 minutes ahead of the allocated time to set up your computer.<br> 
    There is an ==automatic penalty if you are not ready to start on time.==<br>
    Wait outside the venue until you are called in.
    
<div id="v15-demo-instructions">

* **Duration:** Strictly `(teamSize x 3) + 1` minutes %%&nbsp;e.g. 13 minutes for a 4-person team.%% Exceeding this limit will be penalized. The extra minute is for the first speaker to give an overview of the product.

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
  * It will be uninterrupted demo: The audience members will not interrupt you during the demo. That means you should finish within the given time.
  * The app should be populated with a significant amount of realistic data at the start. %%&nbsp;e.g at least 20 contacts%%.
  * **Dress code** : The level of formality is up to you, but it is recommended that the whole team dress at the same level.
    
* **Optimizing the time:** 
  * Spend as much time as possible on demonstrating the actual product. Not recommended to use slides (if you do, use them sparingly) or videos or lengthy narrations.  
   Avoid skits, re-enactments, dramatizations etc. This is not a sales pitch or an informercial. While you need to show how a user use the product to get value, but you don’t need to act like an imaginary user. For example, [Instead of this]`Jim get’s a call from boss. "Ring ring", "hello", "oh hi Jim, can we postpone the meeting?" "Sure". Jim hang up and curses the boss under his breath. Now he starts typing ..etc.` [do this] `If Jim needs to postpone the meeting, he can type …`  
    It’s not that dramatization is bad or we don’t like it. We simply don’t have enough time for it.  
    Note that CS2101 demo requirements may differ. Different context → Different requirements.  
  * Rehearse the steps well and ensure you can do a smooth demo. ==Demos that are clearly under-prepared will be penalized.==
  * Don’t waste time repeating things the target audience already knows. e.g. no need to say things like "We are students from NUS, SoC". 
  * Bring sufficient amount of sample data and know how to load them to the system. You should not plan to type all the sample data during the demo itself. On the other hand, trying to demo a product using just 1-2 sample data creates a bad impression too.
  * Plan the demo to be in sync with the impression you want to create. For example, if you are trying to convince that the product is easy to use, show the easiest way to perform a task before you show the full command with all the bells and whistles.
  * Limit the demo to CLI inputs only. There is no point explaining GUI inputs because they don't earn marks.

</div>

**Grading**: 

<include src="project-assessment.md" name="%%Admin » Project: Assessment%%" dynamic />

<div id=v15-practicalExam>

### v1.5 Practical Exam

<tip-box type="important"> 

**Compulsory. Graded ==(accounting for about 10 marks in total)==**. 

</tip-box>

**Objectives:** 
* Evaluate your,
  * manual testing skills
  * product evaluation skills
  * effort estimation skills
* Peer-evaluate your
  * product design :busts_in_silhouette:
  * implementation effort :bust_in_silhouette:
  * documentation quality :bust_in_silhouette:

**Time/venue:** week 13 lecture slot, but not in the lecture venue (you can do it anywhere)

<include src="project-testing.md#testingPreparations" />

**During:** 

1. **Take note of your team to test and your _Tester ID_**. Both will be given to you by the teaching team (distributed via IVLE gradebook). 
1. **Download from IVLE all files** submitted by the team %%&nbsp;(i.e. jar file, User Guide, Developer Guide, and Project Portfolio Pages)%% ==into an empty folder==.
1. **[~40 minutes] Test the product and report bugs** 
   * Launch the jar file. Test it. 
   * You can use Developer Guide (Appendix named _Instructions for Manual Testing_) and the User Guide in your testing. 
   * No need to test features that are driven by GUI inputs (e.g. buttons, menus, etc.) %%&nbsp;Reason: Only CLI-driven features can earn credit, as per given project constraints.%% Some features might have both a GUI-driven and CLI-driven ways to invoke them, in which case test only the CLI-driven way of invoking it.
   * The testing instructions in the Developer Guide can provide you some guidance but if you follow those instructions strictly, you are unlikely to find many bugs. You can deviate from the instructions to probe areas that are more likely to have bugs.
   * You can do _acceptance_ testing as well as _system_ testing.
   * Omit feature that existed in AB4. Instead, test features the team has added. 
   * Report bugs in the [practical exam issue tracker](https://github.com/nus-cs2103-AY1718S2/pe/issues), ==not in the team's repo==. 
     * Issue title format: `[Tester ID] Issue description` %%&nbsp;e.g. `[26] Empty name crashes app`%%
     * Do not use team ID in bug reports %%&nbsp;Reason: to prevent others copying your bug reports%%
   * Report bugs only. Do not post suggestions. These are considered bugs:
     * Behavior differs from the User Guide (or Developer Guide)
     * A legitimate user behavior is not handled %%&nbsp;e.g. incorrect commands, extra parameters%%
     * Behavior is not specified and differs from normal expectations %%&nbsp;e.g. error message does not match the error%%
   * Write good quality bug reports; :exclamation: **poor quality or incorrect bug reports will be penalized**.
     * Use a descriptive title
     * Give a good description of the bug with steps to reproduce and screenshots
     * :mag: Note that we will **anonymize bug reports** before revealing it to the receiving team. 
   * Assign a severity to the bug report:

<include src="appendixE-gitHub.md#bug-severity" />


1. **[~40 minutes] Evaluate the following aspects.** Note down your evaluation in a hard copy (as a backup). Submit via TEAMMATES.  
  
   * **A. Cohesiveness of product features** [:busts_in_silhouette:]: Do the major features fit together and match the stated target user and the value proposition?
     * `low`: One of these
       * target user is too general %%&nbsp;i.e. not narrower than AB4%%
       * target user and value proposition is not clear from the user guide OR
       * features don't seem to match for the most part
     * `medium`: Some features match but some don't
     * `high`: all features match but the features are not very high value to the target user 
     * `excellent`: the product is very attractive to the target user. i.e. and almost all new features are of high-value to the target user.
     * `unable to judge`: you are unable to judge this aspect for some reason
  
   * **B. Quality of user docs** [:bust_in_silhouette:]: Evaluate based on the parts of the user guide written by the person, as reproduced in the project portfolio.  ==Evaluate from an end-user perspective.== 
     * `low`: Hard to understand, often inaccurate or missing important information
     * `medium`:
     * `high`: Mostly easy to follow. Only a few areas for improvements.
     * `excellent`: Easy to follow and accurate. Just enough information, visuals, examples etc. (not too much either).
     * `unable to judge`: less than 1 page worth of UG content written by the student

   * **C. Amount of work** [:bust_in_silhouette:]:  Evaluate the amount of work on a scale of 0 to 30
     * Consider [this PR (`history` command)](https://github.com/se-edu/addressbook-level4/pull/440/files) as 5 units of effort which means [this PR (`undo/redo` command)](https://github.com/se-edu/addressbook-level4/pull/610/files) is about 15 points of effort. Given that 30 points matches an effort twice as that needed for the `undo/redo` feature (which was given as an example of an `A` grade project), we expect most students to be have efforts lower than 20.
     * Count all implementation/testing/documentation work as mentioned in that person's portfolio page.
     * :exclamation: Do not give a high value just _to be nice_. If your estimate is wildly inaccurate, it means you are unable to estimate the effort required to implement a feature in a project that you are supposed to know well at this point. ==You will lose marks if that is the case.==
     * When estimating effort, ignore features that are driven by GUI inputs.
  
   * **D. Depth of feature (major feature)** [:bust_in_silhouette:]: Evaluate ==the major feature== done by the student for difficulty, depth, and completeness. Note: examples given below assumes AB4 did not have commands`edit` `undo` `redo` 
     * `low` : an easy feature %%&nbsp;e.g. make the existing _find_ command case insensitive%% 
     * `medium` : moderately difficult feature, barely acceptable implementation %%&nbsp;e.g. an _edit_ command that requires the user to type _all_ fields, even the ones that are not being edited%% 
     * `high`: one of the below
       * A moderately difficult feature but fully implemented %%&nbsp;e.g. an _edit_ command that allows editing any field%%
       * A difficult feature with a reasonable implementation but some aspects are not covered %%&nbsp;undo/redo command that only allows a single undo/redo%%
     * `excellent`: A difficult feature, all reasonable aspects are fully implemented %%&nbsp;undo/redo command that allows multiple undo/redo%%
     * `outstanding`: A difficult feature, implemented as good as it can be under the circumstances. %%&nbsp;undo/redo command that even allows undoing non-mutating commands such as _select_, allows selectively undo specific commands in the history, etc.%%
     * `unable to judge`: you are unable to judge this aspect for some reason
  
   * **E. Quality of developer docs** [:bust_in_silhouette:]: Evaluate based on the developer docs cited/reproduced in the respective project portfolio page. ==Evaluate from the perspective of a new developer trying to understand how the features are implemented.== 
     * `low`: One of these
       * Very small amount of content (i.e., 0.5 - 1 page)
       * Hardly any use to the reader (i.e., content doesn't make much sense or redundant) 
       * Uses ad-hoc diagrams where UML diagrams could have been used instead
       * Multiple notation errors in UML diagrams
     * `medium`: _Some_ diagrams, _some_ descriptions, but does not help the reader that much %%&nbsp;e.g. overly complicated diagrams%%
     * `high`: Enough diagrams (at lest two kinds of UML diagrams used) and enough descriptions (about 2 pages worth) but explanations are not always easy to follow.
     * `excellent`: Easy to follow. Just enough information (not too much). Minimum repetition of content/diagrams. Good use of diagrams to complement text descriptions. Easy to understand diagrams with just enough details rather than very complicated diagrams that are hard to understand.
     * `unable to judge`: One of these
       * no content at all
       * less than 0.5 pages worth of content
       * other problems in the document %%&nbsp;e.g. looks like included wrong content%%

**Bug Review Period**:

There will be a review period for you to respond to the [bug reports](https://github.com/nus-cs2103-AY1718S2/pe-results/issues) you received.

Duration: The review period will start around 1 day after the PE (exact time to be announced) and will last until the following **Wednesday midnight**. 

Bug reviewing is recommended to be done as a team as some of the decisions need team consensus.

<tip-box> 

**Instructions for Reviewing Bug Reports**

* **First, don't freak out if there are lot of bug reports.** Many can be duplicates and some can be _false positives_. In any case, we anticipate that all of these products will have some bugs and our penalty for bugs is not harsh. Furthermore, it depends on the severity of the bug. Some bug may not even be penalized.

* **Do not edit the subject or the description. Do not close bug reports.** Your response (if any) should be added as a comment.

* **If the bug is reported multiple times**, mark all copies EXCEPT one as duplicates using the `duplicate` tag. In addition, use [this technique](https://help.github.com/articles/about-duplicate-issues-and-pull-requests/) to indicate which issue they are duplicates of. Duplicates can be omitted from processing steps given below.

* **If a bug seems to be for a different product** (i.e. wrongly assigned to your team), let us know (email prof).

* **Decide if it is a real bug and apply ONLY one of these labels**.

<tip-box> 

Response Labels:
* `response.Accepted` : You accept it as a bug. 
* `response.Rejected` : What tester thought as a bug is in fact expected behavior. :exclamation: The penalty for rejecting a bug using an unjustifiable explanation is higher than the penalty if the same bug was accepted. You can also reject bugs that you inherited from AB4.
* `response.CannotReproduce` : You are unable to reproduce the behavior reported in the bug after multiple tries. 
* `response.IssueUnclear` : The issue description is not clear.

</tip-box>

* If applicable, **decide the type of bug**:

<tip-box> 

Bug Type Labels:
* `type-FunctionalityBug` : the bug is a flaw in how the product works
* `type-DocumentationBug` : the bug is in the documentation

</tip-box>

* **Suggest a severity for the bug**:

<include src="appendixE-gitHub.md#bug-severity" />


* **Decide who should fix the bug**. Use the `Assignees` field to assign the issue to that person(s). There is no need to actually fix the bug though. It's simply an indication/acceptance of responsibility. **If there is no assignee and we are unable to determine a suitable assignee ourselves, we'll have no choice but to distribute the penalty for that bug (if any) among all team members.**

* **Add an explanatory comment** explaining your choice of labels and assignees.

</tip-box>

**Grading:** 

* Your performance in the practical exam will be considered for your final grade (under the _QA_ category and under _Implementation_ category, about 10 marks in total). 
* You will lose marks if you missed too many bugs in the product you tested or your evaluation/estimates are significantly off from the evaluator consensus. %%&nbsp;Explanation: we penalize if your inputs don't seem be be based on a sincere effort to test/evaluate.%%
* The bugs found in your product by others will affect your v1.5 marks. You will be given a chance to reject false-positive bug reports.