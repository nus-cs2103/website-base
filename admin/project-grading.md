{% macro show_main_text() %}
<div id="main">

Note that project grading is ==not competitive (not bell curved)==. {{ module }}T projects will be assessed separately from {{ module }} projects. This is to account for the perceived difference in workload. Given below is the marking scheme.

**Total**: 45 marks ({{ icon_individual }} 35 individual marks + {{ icon_team }} 10 team marks)

See the sections below for details of how we assess each aspect.

-----------------------------------------------------------------------------------------------------------------------

#### 1. Project Grading: Product Design %%[{{ icon_team }} 5 marks]%%

**Evaluates:** how well your features fit together to form a cohesive product (not how many features or how big the features are) and how well does it match the target user

**Evaluated by:**
* tutors (based on product demo and user guide)
* peers from other teams (based on peer testing and user guide)

{{ icon_info }} For reference, here are some grading instructions that will be given to peers/tutors grading this aspect:

<blockquote>
<div id="projectGrading-featureFit-instructions">

Evaluate the product design ==based on how the product V2.0 (not V1.4) is described in the User Guide==.
- [ ] `unable to judge`: You are unable to judge this aspect for some reason e.g., UG is not available or does not have enough information.

**Target user**:
- [ ] `target user specified and appropriate`: The target user is clearly specified, ==prefers typing over other modes of input==, and not too general (should be narrowed to a specific user group with certain characteristics).
- [ ] `value specified and matching`: The value offered by the product is clearly specified and matches the target user.

**Value to the target user**:
- [ ] `value: low`: The value to target user is low. App is not worth using.
- [ ] `value: medium`: Some small group of target users might find the app worth using.
- [ ] `value: high`: One of the below:
  * Most of the target users are likely to find the app worth using.
  * It feels like a fast typist can be more productive with the app, compared to an equivalent GUI app without a CLI.

**Feature-fit**:
  - [ ] `feature-fit: low`: Features don't seem to fit together.
  - [ ] `feature-fit: medium`: Some features fit together but some don't.
  - [ ] `feature-fit: high`: All features fit together.

**Other**:
- [ ] `polished`: The product looks well-designed, ==good enough to be a real product== (i.e., A/A+ effort)
</div>
</blockquote>

-----------------------------------------------------------------------------------------------------------------------

#### 2. Project Grading: Implementation %%[{{ icon_individual }} 10 marks]%%

**<big>2A. Code quality</big>**

**Evaluates:** the quality of the code you have written yourself

**Based on:** the parts of the code you claim as written by you

**Evaluation method:**: manual inspection by tutors + automated-analysis by a script

{{ icon_info }} For reference, here are some factors considered when grading this aspect:

<span id="projectGrading-codeQuality-criteria">

* At least some evidence of these (see [here]({{baseUrl}}/se-book-adapted/chapters/errorHandling.html) for more info)
  * logging
  * exceptions
  * assertions
  * defensive coding

* No [coding standard]({{java_coding_standard}}) violations %%e.g. all boolean variables/methods sounds like booleans%%. Checkstyle can prevent only _some_ coding standard violations; others need to be checked manually.

* [SLAP]({{baseUrl}}/se-book-adapted/chapters/codeQuality.html#slap-hard) is applied at a reasonable level. Long methods or deeply-nested code are symptoms of low-SLAP.

* No noticeable code duplications %%i.e. if there multiple blocks of code that vary only in minor ways, try to extract out similarities into one place%%, especially in test code.

* Evidence of applying [code quality guidelines covered in the module](../book/codeQuality/).

</span>


**<big>2B. Feature Quality</big>**

**Evaluates:** how deep is your biggest feature, how complete is the feature, how well it solves the target user needs, etc.

**Evaluation method:**
* by peers from own team and other teams (based on peer testing session, PPP, RepoSense data) -- more weight for team members from own team than those from other teams
* by tutors (based on demo, <tooltip content="Project Portfolio Page">PPP</tooltip>, RepoSense data)

{{ icon_info }} For reference, here are some grading instructions that will be given to peers/tutors grading this aspect:

<blockquote>
<div id="projectGrading-featureQuality-instructions">

Evaluate ==the biggest feature done by the student== for difficulty, completeness, and testability. Note: examples given below assume that AB3 did not have the commands `edit`, `undo`, and `redo`.

**Difficulty**:
- [ ] `Feature/ difficulty: unable to judge`: You are unable to judge this aspect for some reason.
- [ ] `Feature/ difficulty: low`: Examples:
  * Make the existing _find_ command case insensitive.
  * CRUD for a simple entity type just like Person that is not connected to any other entity type.
- [ ] `Feature/ difficulty: medium`: Examples:
  * A moderately difficult new command that is not similar to existing commands.
  * A new entity type moderately different from Person and lightly connected to other entity types..
- [ ] `Feature/ difficulty: high`: Examples:
  * a) A high-level of natural language support b) A deep integration with another product c) An enhancement that makes the product good enough to take to the market d) A new entity type very different from Person and deeply connected to many other entity types

**Completeness**:
- [ ] `Feature/ completeness: unable to judge`: You are unable to judge this aspect for some reason.
- [ ] `Feature/ completeness: low`: A partial implementation of the feature. Barely useful.
- [ ] `Feature/ completeness: medium`: The feature has enough functionality to be useful for some of the users.
- [ ] `Feature/ completeness: high`: The feature has all functionality to be useful to almost all users AND Some optimization for keyboard users e.g., easy-to-type syntax.

**Other**:
- [ ] `Feature/ not hard to test`: The feature was not too hard to test manually.
- [ ] `Feature/ polished`: The feature looks _polished_ (as if done by a professional programmer), A/A+ effort.

</div>
<div id="projectGrading-effort-instructions">

Evaluate the amount of work (i.e., ==all work described in the PPP==, not just the biggest feature), on a scale of 0 to 30.
* Consider [this PR (`history` command)](https://github.com/se-edu/addressbook-level4/pull/440/files) as 5 units of effort which means [this PR (`undo/redo` command)](https://github.com/se-edu/addressbook-level4/pull/610/files) is about 15 points of effort. Given that 30 points matches an effort twice as that needed for the `undo/redo` feature (which was given as an example of an `A` grade project), we expect most students to be have efforts lower than 20.
* Count all implementation/testing/documentation work as mentioned in that person's PPP. Also look at the actual code written by the person.
* {{ icon_important_big_red }} Do not give a high value just _to be nice_. ==Your responses will be used to evaluate your effort estimation skills.==
</div>
</blockquote>

-----------------------------------------------------------------------------------------------------------------------

#### 3. Project Grading: QA %%[{{ icon_individual }} 10 marks]%%

<big>**3A. System/Acceptance Testing:**</big>

**Evaluates:** How well you can system-test/acceptance-test a product

**Based on:**
1. bugs you found in the [Practical Exam]({{baseUrl}}/admin/project-deliverables.html#deliverable-practical-exam)
1. our own manual testing (when necessary)

**Evaluated by:** teaching team (in the capacity of _moderators_ %%e.g., to verify if it is reasonable for you to reject a bug reported by others%%)

<big>**3B. Developer Testing:**</big>

**Evaluates:** How well you tested your own feature

**Based on:**
1. bugs in your work found by others during the PE
1. your test code %%(note <trigger trigger="click" for="modal:projectGradingQA-testingExpectations">our expectations for automated testing</trigger>)%%

**Evaluated by:** tutors (in the capacity of _moderators_ %%e.g., to verify if it is reasonable for the team to downgrade the severity of a bug you reported%%)

<modal large title="Our expectations for automated testing in the project" id="modal:projectGradingQA-testingExpectations">
  <include src="project-scope.md#testing-expectations"/>
</modal>

<box>

<div id="pe-grading-notes">

##### Notes on how marks are calculated based on PE product testing

* Bugs rejected by the dev team, if the rejection is approved by the teaching team, will not be affect marks of the tester or the developer.
* The penalty/credit for a bug varies based on,
  * The severity of the bug: `severity.High` > `severity.Medium` > `severity.Low`
  * The type of the bug:  `type.FunctionalityBug` > `type.DocumentationBug` > `type.FeatureFlaw` > `type.DocTypo`
* The penalty for a bug is divided equally among assignees.
* The developers are not penalized for the duplicate bug reports they received but the testers earn credit for the duplicate bug reports they submitted as long as the duplicates are not submitted by the same tester.
* <tooltip content="i.e., the same bug reported by many testers">_Obvious_ bugs</tooltip> earn less credit for the tester and slightly more penalty for the developer.
* If the team you tested has a low bug count i.e., total bugs found by all testers is low, we will fall back on other means %%(e.g., performance in PE dry run)%% to calculate your marks for system/acceptance testing.
* Your marks for developer testing depends on the _bug density_ rather than total bug count. Here's an example:
  * `n` bugs found in your feature; it is a difficult feature consisting of lot of code → 4/5 marks
  * `n` bugs found in your feature; it is a small feature with a small amount of code → 1/5 marks
* You don't need to find all bugs in the product to get full marks. For example, finding half of the bugs of that product or 4 bugs, whichever the lower, could earn you full marks.
* Excessive incorrect downgrading/rejecting/<tooltip content="marking as duplicates">duplicate-flagging</tooltip>, if deemed an unethical attempt to _game the system_, may be penalized.
</div>
</box>

-----------------------------------------------------------------------------------------------------------------------

#### 4. Project Grading: Documentation %%[{{ icon_individual }} 10 marks]%%

**Evaluates:** the quality of the sections you wrote for the user guide and the developer guide

**Based on:** the relevant sections of your PPP.

**Evaluated by:** tutors, peers from own team and other teams

{{ icon_info }} For reference, here are some grading instructions that will be given to peers/tutors grading this aspect:

<blockquote>
<div id="projectGrading-userGuide-instructions">

Evaluate the quality of user documentation **based on the parts of the user guide written by the person,** as reproduced in the project portfolio.  ==Evaluate from an end-user perspective.==
- [ ] `UG/ unable to judge`: Less than 1 page worth of UG content written by the student or cannot find PPP
- [ ] `UG/ good use of visuals`: Uses visuals e.g., screenshots.
- [ ] `UG/ good use of examples`: Uses examples e.g., sample inputs/outputs.
- [ ] `UG/ just enough information`: Not too much information. All important information is given.
- [ ] `UG/ easy to understand`: The information is easy to understand for the target audience.
- [ ] `UG/ polished`: The document looks neat, well-formatted, and professional.

</div>
<div id="projectGrading-devGuide-instructions">

Evaluate the quality of developer documentation **based on the developer docs cited/reproduced in the respective project portfolio page.** ==Evaluate from the perspective of a new developer trying to understand how the features are implemented.==
- [ ] `DG/ unable to judge`: Less than 0.5 pages worth of content OR other problems in the document %%e.g. looks like included wrong content%%.
- [ ] `DG/ too little`: 0.5 - 1 page of documentation
- Diagrams:
  - [ ] `DG/ types of UML diagrams: 1`: Only one type of diagram used (types: Class Diagrams, Object Diagrams, Sequence Diagrams, Activity Diagrams, Use Case Diagrams)
  - [ ] `DG/ types of UML diagrams: 2`: Two types of diagrams used
  - [ ] `DG/ types of UML diagrams: 3+`: Three or more types of diagrams used
  - [ ] `DG/ UML diagrams suitable`: The diagrams used for the right purpose
  - [ ] `DG/ UML notation correct`: No more than one minor error in the UML notation
  - [ ] `DG/ diagrams not repetitive`: No evidence of repeating the same diagram with minor differences
  - [ ] `DG/ diagrams not too complicated`: Diagrams don't cram too much information into them
  - [ ] `DG/ diagrams integrates with text`: Diagrams are well integrated into the textual explanations
- [ ] `DG/ easy to understand`: The document is easy to understand/follow
- [ ] `DG/ just enough information`: Not too much information. All important information is given.
- [ ] `DG/ polished`: The document looks neat, well-formatted, and professional.

</div>
</blockquote>

-----------------------------------------------------------------------------------------------------------------------

#### 5. Project Grading: Project Management %%[{{ icon_team }} 5 + {{ icon_individual }} 5 = 10 marks]%%

<div id="project-management-grading"> 

<big>**5A. Process:**</big>

**Evaluates:** How well you did in project management related aspects of the project, as an individual and as a team

**Based on:** tutor/bot observations of project milestones and GitHub data
 
Milestones ==need to be reached the midnight before of the tutorial== for it to be counted as achieved. ==To get a good grade for this aspect, achieve at least 60% of the recommended milestone progress.==
  
Other criteria:
* Good use of GitHub milestones
* Good use of GitHub release mechanism
* Good version control, based on the repo
* Reasonable attempt to use the forking workflow
* Good task definition, assignment and tracking, based on the issue tracker
* Good use of buffers %%(opposite: everything at the last minute)%%
* Project done iteratively and incrementally %%(opposite: doing most of the work in one big burst)%% 

<big>**5B. Team-tasks:**</big>

**Evaluates:** How much you contributed to team-tasks

**Based on:** peer evaluations, tutor observations

To earn full marks, you should have done a fair share of the team tasks. You can earn bonus marks by doing more than your fair share.

{{ embed_topic("project-scope.md#example-team-tasks", "Admin " + icon_embedding + " Project Scope → Examples of team-tasks", "projectGrading-exmapleTeamTasks", "3") }}

</div>

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-grading", show_main_text) }}
