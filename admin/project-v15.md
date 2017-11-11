<tip-box> 

* :exclamation: **Penalty for late submission:** ==-1 mark for each hour delayed.== Even a 1-second delay is penalized, irrespective of the reason. 
  * For submissions done via IVLE, the submission time is the timestamp shown by IVLE.
  * When determining the late submission penalty, **we take the latest submission** even if the same exact file was submitted earlier. Do not submit the same file multiple times if you want to avoid unnecessary late submission penalties.
* The whole team is penalized for problems in team submissions. Only the respective student is penalized for problems in individual submissions. 
* :exclamation: Please **follow submission instructions closely**. ==Any non-compliance will be penalized==. e.g. wrong file name, team member photos not suitable, etc.
* For pdf submissions, ensure the file is usable and hyperlinks in the file are correct. Problems in documents are considered bugs too %%&nbsp;e.g. broken links, outdated diagrams/instructions etc.%%.
* **Do not update the repo during the 7 days after the deadline.** Get our permission first if you need to update the repo during that one-week _freeze_ period. You can continue to evolve your repo after that. 

**Summary of submissions**:

Item | Team/Individual | Method
---- | --------------- | ------
Jar file | :busts_in_silhouette::busts_in_silhouette: | IVLE
User Guide | :busts_in_silhouette::busts_in_silhouette: | IVLE
Developer Guide | :busts_in_silhouette::busts_in_silhouette: | IVLE
Sample Data | :busts_in_silhouette::busts_in_silhouette: | IVLE
Test Script | :busts_in_silhouette::busts_in_silhouette: | IVLE
Project Portfolio Page | :bust_in_silhouette: | IVLE
`README.adoc`, `Ui.png` | :busts_in_silhouette::busts_in_silhouette: | GitHub
`AboutUs.adoc` | :busts_in_silhouette::busts_in_silhouette: | GitHub
Collated files | :bust_in_silhouette: | GitHub

</tip-box>


### v1.5 Product

This is as a ‘production release’. It should be at least ‘near production quality’.

==Add these two new files== to the repo (these will be used by our testers when testing your final submission):

* `{project root}\src\test\data\ManualTesting\[team][Project Name]SampleData.xml` :  %%e.g. [T09-B1][ContactsPlus]SampleData.xml%%
    Sample data that can be loaded to your app. Should contain 20+ items.
* `{project root}\src\test\data\ManualTesting\[team][Project Name]TestScript.adoc` :  %%e.g. [T09-B1][ContactsPlus]TestScript.adoc%%
  A document explaining the steps to perform manual testing (i.e. manual scripted testing), starting with how to load the sample data.  
  Should cover all functionality of the product. Should be grouped by functionality.  
  Should specify the command to type and the expected result (screenshots not required).  
  Limit the test cases to about 20 minutes worth of testing.

**Submission**:

* **Source code**: Push the code to GitHub and tag with the version number. Source code (==including collated .md files==; please ensure the collated `.md` files are up to date; any updates to collated code files after the deadline comes with an automatic penalty) Note that the quality of the code in these ==collated code files accounts for a significant component of your final score==, graded individually.
* **Executable**: upload the jar file to IVLE. File name: `[team][product name].jar` %%e.g. [T09-B1][ContactsPlus].jar%%
* **Test data/instructions**: Upload following files to IVLE.
  * Sample data file. File name  `[team][Project Name]SampleData.xml` %%e.g. [T09-B1][ContactsPlus]SampleData.xml%%
  * Testing instructions. File name  `[team][Project Name]TestScript.pdf` %%e.g. [T09-B1][ContactsPlus]TestScript.pdf%%
    

**Deadline**: Week 13 Monday 23.59.

**Grading**: 

<include src="project-assessment.md" name="%%Admin &raquo; Project: Assessment%%" dynamic />

### v1.5 Documentation

**Submission**:

* Update User Guide, Developer Guide, README, and AboutUs pages on GitHub.
 

* Convert the following documents to pdf (AB4 dev guide has some instructions on converting project docs to pdf) and upload to IVLE.

Document | Name format 
---------|-------------
User guide | `[TEAM_ID][Project Name]UserGuide.pdf`<br>  %%e.g.[T09-B1][Contacts Plus]UserGuide.pdf%%
Developer guide | `[TEAM_ID][Project Name]DeveloperGuide.pdf`<br> %%e.g. [T09-B1][Contacts Plus]DeveloperGuide.pdf%%
Portfolio | `[TEAM_ID][Your Name]Portfolio.pdf`<br> %%e.g.[T09-B1][John Doe]Portfolio.pdf%%

**Deadline**: Same as v1.5 product.

**Grading**: 

<include src="project-assessment.md" name="%%Admin &raquo; Project: Assessment%%" dynamic />

### v1.5 Demo

<img src="{{baseUrl}}/admin/images/v05demo.png" style="width: 250px">

* **Venue:** Same as the tutorial venue unless informed otherwise.
* **Duration:** Strictly no more than 3 minutes per person (i.e. a total of 12 minutes for a 4-person team). Exceeding this limit will be penalized.
* **Schedule:** Your demo timing is same as your tutorial time in week 13.  
    Starting times: `Team B1: 00 minutes, B2: 15 minutes, B3: 30 minutes, B4: 45 minutes`  
    At least some team members need to arrive 15 minutes ahead of the allocated time to set up your computer.  
    There is an ==automatic penalty if you are not ready to start on time.==.
* **Target audience**: Assume you are giving a demo to a higher-level manager of your company, to brief him/her on the current capabilities of the product.  
* **Scope**: 
  * Organize the demo to present a cohesive picture of the product as a whole, similar to the v1.5rc demo.
  * Remember to explain the profile of the target user early in the demo.
  * The scenarios you demonstrate should be chosen judiciously so that you cover the full range of your product's functionality. Give more time to stronger features (i.e. cover mundane/basic features fast). It is recommended you showcase how the product improves the user’s life rather than simply describe each feature.
  * No need to cover design/implementation details as the manager is not interested in those details.
* **Dress code** : The level of formality is up to you, but it is recommended that the whole team dress at the same level.
* **Structure:**  
    Demo the product using the same executable you submitted, on your own laptop, using the TV.  
    Every team member should take part in the demo. However, it's ok for one member to do all the typing.
* **Optimizing the time:**  
    Try to make the maximum use of the short demo time in the following ways,
  * Spend as much time as possible on demonstrating the actual product. Not recommended to use slides (if you do, use them sparingly) or videos or lengthy narrations.  
   Avoid skits, re-enactments, dramatizations etc. This is not a sales pitch or an informercial. While you need to show how a user use the product to get value, but you don’t need to act like an imaginary user. For example, 
   [Instead of this]`Jim get’s a call from boss. "Ring ring", "hello", "oh hi Jim, can we postpone the meeting?" "Sure". Jim hang up and curses the boss under his breath. Now he starts typing ..etc.`  
    [do this] `If Jim needs to postpone the meeting, he can type …`  
    It’s not that dramatization is bad or we don’t like it. We simply don’t have enough time for it.  
    Note that CS2101 demo requirements may differ. Different context → Different requirements.  
  * Rehearse the steps well and ensure you can do a smooth demo. ==Demos that are clearly under-prepared will be penalized.==
  * Don’t waste time repeating things the target audience already knows. e.g. no need to say things like "We are students from NUS, SoC". 
  * No need to spend time describing features that existed in original AB4 but you can mention if you did any changes to those features.
  * Bring sufficient amount of sample data and know how to load them to the system. You should not plan to type all the sample data during the demo itself. On the other hand, trying to demo a product using just 1-2 sample data creates a bad impression too.
  * Plan the demo to be in sync with the impression you want to create. For example, if you are trying to convince that the product is easy to use, show the easiest way to perform a task before you show the full command with all the bells and whistles.
  * Limit the demo to CLI inputs only. There is no point explaining GUI inputs because they don't earn marks.

**Grading**: 

<include src="project-assessment.md" name="%%Admin &raquo; Project: Assessment%%" dynamic />

<div id=v15-practicalExam>

### v1.5 Practical Exam

(Previously called _Testathon_)

<tip-box type="important"> 

**Graded ==(accounting for about 10 marks in total)==. Attendance is compulsory**. 

</tip-box>

**Objectives:** 
* Evaluate your,
  * manual testing skills
  * product evaluation skills
  * effort estimation skills
* Peer-evaluate your
  * product design :busts_in_silhouette::busts_in_silhouette:
  * implementation effort :bust_in_silhouette:
  * documentation quality :bust_in_silhouette:

**Time/venue:** week 13 lecture, lecture venue

<include src="project-testing.md#testingPreparations" />

**During:** 

<tip-box> 

:exclamation: this session is conducted under conditions similar to that of a final exam except limited use of the computer is allowed.
* Sit in the [assigned row](https://docs.google.com/spreadsheets/d/e/2PACX-1vTSnp6t_MzmNDS2Jg5GPWkHoJmX0ISL_XBz86Z2n_CxvEkwHw4yZCWxaDZbRFb6PBotFQRPZXfreJwI/pubhtml?gid=0&single=true). When you select a seat to sit in the assigned row, choose the empty seat closest to the middle of the seat segment (i.e. fill rows starting from the middle) so that those who come later than you don't have to distrub you to get to empty seats in the middle.
* Not allowed:
  * communicating with others (except with teaching team members present)
  * use any other software/websites than those strictly required for the testing 
  * running background IM/chat/notification services
  * use of phones

</tip-box>

1. **Take note of your team to test and your _Tester ID_**. Both will be given to you by the teaching team. 
1. **Download from IVLE all files** submitted by the team %%&nbsp;(i.e. jar file, user guide, developer guide, sample data, test script, project portfolio pages)%% ==into an empty folder==.
1. **[40 minutes] Test the product and report bugs** 
   * Launch the jar file. Test it. 
   * You can use the provided _test script_ and _user guide_ in your testing. 
   * The test script can provide you some guidance but if you follow the test script strictly, you are unlikely to find many bugs. You can deviate from the script to probe areas that are more likely to have bugs.
   * You can do _acceptance_ testing as well as _system_ testing.
   * Report bugs in the [practical exam issue tracker](https://github.com/nus-cs2103-AY1718S1/pe/issues), ==not in the team's repo==. 
     * Issue title format: `[Tester ID] Issue description` %%&nbsp;e.g. `[26] Empty name crashes app`%%
     * Do not use team ID in bug reports %%&nbsp;Reason: to prevent others copying your bug reports%%
   * Report bugs only. Do not post suggestions. These are considered bugs:
     * Behavior differs from the user guide (or testing instructions)
     * A legitimate user behavior is not handled %%&nbsp;e.g. incorrect commands, extra parameters%%
     * Behavior is not specified and differs from normal expectations %%&nbsp;e.g. error message does not match the error%%
   * Write good quality bug reports; :exclamation: **poor quality or incorrect bug reports will be penalized**.
     * Use a descriptive title
     * Give a good description of the bug with steps to reproduce and screenshots
   * :mag: Note that we plan to **anonymize bug reports** before revealing it to the receiving team. 

1. **[30 minutes] Evaluate the following aspects.** Note down your evaluation in a hard copy (as a backup). Submit via TEAMMATES.  
  
   * **A. Cohesiveness of product features** [:busts_in_silhouette::busts_in_silhouette:]: Do the features fit together and match the target user (and the target problem being addressed)?
     * `low`: Target user/problem not clear from the user guide OR features don't seem to match target user for the most part.
     * `medium`: Some features are relevant to the target user but some are not.
     * `high`: One of these
       * Almost all features are relevant to the target user but the target user is very general
       * Almost all features are relevant to the target user but the features are not very high value to the target user 
     * `excellent`: Target user clearly defined (not too general) and almost all new features are of high-value to the target user. i.e. the product is very attractive to the target user.
  
   * **B. Quality of user docs** [:bust_in_silhouette:]: Evaluate based on the parts of the user guide written by the person, as reproduced in the project portfolio.  ==Evaluate from an end-user perspective.== 
     * `low`: Hard to understand, often inaccurate or missing important information
     * `medium`:
     * `high`: Mostly easy to follow. Only a few areas for improvements.
     * `excellent`: Easy to follow and accurate. Just enough information, visuals, examples etc. (not too much).
     * `unable to judge`: not enough content to make a judgement

   * **C. Amount of work** [:bust_in_silhouette:]:  Evaluate the amount of work on a scale of 0 to 30
     * Consider [this PR (`history` command)](https://github.com/se-edu/addressbook-level4/pull/440/files) as 5 units of effort which means [this PR (`undo/redo` command)](https://github.com/se-edu/addressbook-level4/pull/610/files) is about 15 points of effort. Given that 30 points matches an effort twice as that needed for the `undo/redo` feature, we do not expect a vast majority of students to be have efforts lower than 20.
     * Count all implementation/testing/documentation work mentioned in that person's portfolio page.
     * If the features was adapted from another team, count the effort required for adapting it, rather than the effort needed for writing it from scratch. 
     * :exclamation: Do not give a high value to be nice. If your estimate is wildly inaccurate, it is a sign that you are unable to estimate the effort required to implement a feature in a project that you are supposed to know well at this point. ==You will lose marks if that is the case.==
  
   * **D. Depth of features** [:bust_in_silhouette:]: Evaluate ==the strongest feature== done by the developer for difficulty, depth, and completeness. Note: examples given below assumes AB4 did not have commands`edit` `undo` `redo`
     * `low` : an easy feature %%&nbsp;e.g. make the existing _find_ command case insensitive%% 
     * `medium` : moderately difficult feature, barely acceptable implementation %%&nbsp;e.g. an _edit_ command that requires the user to type _all_ fields, even the ones that are not being edited%% 
     * `high`: one of the below
       * A moderately difficult feature but fully implemented %%&nbsp;e.g. an _edit_ command that allows editing any field%%
       * A difficult feature with a reasonable implementation but some aspects are not covered %%&nbsp;undo/redo command that only allows a single undo/redo%%
     * `excellent`: A difficult feature, all reasonable aspects are fully implemented %%&nbsp;undo/redo command that allows multiple undo/redo%%
     * `outstanding`: A difficult feature, implemented as good as it can be under the circumstances. %%&nbsp;undo/redo command that even allows undoing non-mutating commands such as _select_, allows selectively undo specific commands in the history, etc.%%
  
   * **E. Quality of developer docs** [:bust_in_silhouette:]: Evaluate based on the developer docs cited/reproduced in the respective project portfolio page. ==Evaluate from the perspective of a new developer trying to understand how the features are implemented.== 
     * `low`: One of these
       * Very small amount of content (i.e., less than 1 page). 
       * Hardly any use to the reader (i.e., content doesn't make much sense or redundant). 
       * Uses ad-hoc diagrams where UML diagrams could have been used instead.
     * `medium`: _Some_ diagrams, _some_ descriptions, but does not help the reader that much.
     * `high`: Enough diagrams and enough descriptions (about 2 pages worth) but explanations are not always easy to follow.
     * `excellent`: Easy to follow. Just enough information (not too much). Minimum repetition of content/diagrams. Good use of diagrams to complement text descriptions.
     * `unable to judge`: not enough content to make a judgement.

**Grading:** Your performance in the practical exam will be considered for your final grade (under the _QA_ category and under _Implementation_ category, about 10 marks in total). 

* You will lose marks if you missed too many bugs in the products you tested or your evaluation/estimates are significantly off from the evaluator consensus. %%&nbsp;Explanation: we penalize if your inputs don't seem be be based on a sincere effort to test/evaluate%%
* The bugs found in your product by others will affect your v1.5 marks. In some cases we'll ask for your input before deciding whether a bug should be penalized %%&nbsp;i.e. give you a chance to reject false-positive bug reports%%
  
</div>