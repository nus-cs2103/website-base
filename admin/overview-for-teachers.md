<frontmatter>
title: CS2103/T Overview (Teacher's POV)
pageNav: 2
</frontmatter>

# ++CS2103/T Overview (Teacher's POV)++

**The goal of the course is to prepare students for SE internships** (note: most students do their first internship at the end of their second year, before taking any other SE courses). That includes teaching students **basic SE concepts** as well as giving them enough **practice in tools, techniques, and practices used in the industry**. This is a CS foundation course, which can also be considered the entry point to the SE focus area, as most other SE courses have this course in their prerequisite chains.

<box type="info" seamless>

**CS2103T vs CS2103:** CS2103T students take CS2101 (Effective Communication for Computing Professionals) at the same time so that they can learn communication skills in the context of the SE project they do in CS2103T. CS2103 is for students who have already taken a different communications course (these are mostly cross-faculty students).<br>
 From our side, we treat both groups of students the same way.
</box>

**Workload:** 4 Units (i.e., workload of 10 hours/week)

**Class size:** (CS2103T: `509` + CS2103: `53` = `562`)

**Topics covered:** [here](../se-book-adapted/index.html).

------------------------{.thick-1 .border-info}

# Key components{.text-info}

Here is the grade breakdown:

<pic eager src="gradeBreakdown.png" />

-----------------------{.dotted .border-info}

## ~~Lectures~~ Weekly Briefings{.text-info}

**CS2103/T is delivered in blended mode.** The primary content delivery mechanism is the online textbook and pre-recorded videos (for example, see [Schedule -> Week 10 -> Topics](../schedule/week10/topics.html)).

**The course doesn't have traditional lectures. We use the lecture slot for a _weekly briefing_ instead.**
The briefing is shorter (about 1 hour), and consists of two parts:

1. A recap (and a deep dive) of the previous week's topics, e.g., reiterating finer points
1. A preview of next week's topics, e.g., their motivation, importance, and place in the big picture

**The briefing is delivered in hybrid mode, and is optional to attend synchronously.** As most students prefer to watch the recording, ==making the session interactive is of low priority==. However, there is an in-briefing quiz students can do during the briefing or while watching the recording.

**To ensure students learn the weekly materials, there is a separate weekly quiz on Canvas.** Students need to submit it before the following lecture. It counts for participation.

-----------------------{.dotted .border-info}

## Tutorials{.text-info}

**Our tutorials are a combination of traditional tutorials and ==a light F2F assessment==.**

**During the tutorial, the tutor poses a series of questions. Students answer using Zoom private chat.** The answers are discussed immediately. Student answers are later extracted from Zoom chat logs. Students earn points as long as they made a good attempt.

**Tutors are given detailed instructions, and slides to use** in the interest of uniformity. I conduct a mock tutorial during the weekly staff meeting to show how to deliver the tutorial. As a quality control measure, tutorials are recorded, and each tutor files a report after each tutorial. As most tutorials are conducted by UG tutors, the class size is kept at around 10 students per tutor.

-----------------------{.dotted .border-info}

## Individual project (iP){.text-info}

**This is a <tooltip content="created from scratch">greenfield</tooltip> project completed iteratively**, meant to build up students' individual competencies before they start the team project. Students add features to the product incrementally while practicing relevant tools such as Java, Git, GitHub, and Gradle.

**The _mastery learning_ approach is used**, i.e., students can keep trying until their work is good enough to earn full marks. The product they build is a chatbot that helps users keep track of tasks.

* The project description starts from [this page](ip-overview.html).<br>
  For a representative view of project tasks for a specific week, see [Week 3 iP tasks](ip-w3.md).
* Final versions of this semester's iPs are on [this page](ip-showcase.html). Some examples are given below:

<tabs active="1">
 <tab header="minimal">

-><pic eager src="https://tys2.github.io/ip/Ui.png"></pic><-
 </tab>
 <tab header="typical">

-><pic eager src="https://ffynch.github.io/ip/Ui.png" width="350"></pic><-
 </tab>
 <tab header="good">

-><pic eager src="https://bedrockfake.github.io/ip/Ui.png" width="800"></pic><-
 </tab>
 <tab header="very good">

-><pic eager src="https://jixiang-t.github.io/ip/Ui.png" width="800"></pic><-
 </tab>
</tabs>

* iP Assessment: As the goal of the iP is to ensure students pass a certain bar of competence before starting the team project, the [iP assessment](ip-grading.html) is done almost on an S/U basis. Those who are unable to pass the bar are given more time and more help until they are able to do so -- resulting in almost all students receiving full marks for this component. **Eventually, more than 99% of the students achieve full marks for the iP (i.e., demonstrate the expected competency level).**

-----------------------{.dotted .border-info}

## Team project (tP){.text-info}

**This is a <tooltip content="starting with a legacy codebase">brownfield</tooltip> iterative project.** Students start with the existing Java desktop [Address Book application](https://se-education.org/addressbook-level3/) and evolve it into a contact management app for a selected target user and use case %%(e.g., for insurance agents to manage contacts of their clients)%%.

In the first half of the semester, students lay the groundwork for the team project, while doing the individual project:<br>
<pic eager src="tpGanttChart-preIterations.png" width="800"></pic>

In the second half of the semester, students build the product in three iterations:<br>
<pic eager src="tpGanttChart-iterations.png" width="800"></pic>

* The project description starts from [this page](tp-overview.html).
* Final versions of the previous semester's tPs are on [this page](https://nus-cs2103-ay2526s1.github.io/website/admin/teamList.html). A few examples are given below:


<tabs>
 <tab header="Example 1">

  -><pic eager src="https://ay2122s2-cs2103t-w14-1.github.io/tp/images/Ui.png"></pic><-
 </tab>
 <tab header="Example 2">

  -><pic eager src="https://ay2122s2-cs2103t-t11-4.github.io/tp/images/Ui.png"></pic><-
 </tab>
 <tab header="Example 3">

  -><pic eager src="https://ay2122s2-cs2103-f11-3.github.io/tp/images/Ui.png"></pic><-
 </tab>
</tabs>

* tP Assessment: We try to make the tP assessment _outcome-based_. For example, the number of bugs found in a team's code influences the grade more than the number of test cases they wrote. More details are given [here](tp-grading.html).


<box type="info" seamless>

The end products of both projects are not meant to be large, as the project duration is short, the learning curve is steep, and the focus is on learning the tools, processes, techniques, etc. rather than adding a lot of features.
</box>

-----------------------{.dotted .border-info}

## Use of AI{.text-info}

This course is probably one of the most affected by the current wave of disruptions of generative AI.

Given that students are already past their introductory programming courses, this course can afford to rely more on AI. In fact, the course now has the responsibility to teach not only foundational skills, but also how to guide AI in SE projects.

In response, we have added the following guidance to our course expectations, **letting students use a level of AI they are comfortable with**.

<panel type="info" header="Course Expectations (extract) → Use of AI" minimized >

<include src="courseExpectations.md#use-of-ai-section" />
</panel>
<p/>

In addition, **we provide fine-grained guidance on how to use AI tools like Codex** in the individual project. [This page]({{ baseUrl }}/admin/ip-w4.html) has some examples (look for purple-colored panels).

-----------------------{.dotted .border-info}

## Participation{.text-info}

[Participation marks](participation.html) are awarded for actively participating in the course activities. To reduce workload stress, students are given full participation marks if they meet a reasonably low bar of participation (e.g., earn at least half the participation points on offer, in at least 10 weeks). Almost all students are expected to earn full marks for this component.

Students can track their own participation level using a participation dashboard.  [Here](https://nus-cs2103-ay2627-s1.github.io/dashboards//contents/participation.html) is the participation dashboard of the current semester -- click on a cell in the **Activities** column to see the details of activities considered.

<box type="info" seamless>

**The use of dashboards brings in an element of _gamification_ to the course**, by framing work as small 'achievements' and making those achievements visible (like a 'leaderboard') to keep students motivated. It is also a way for students to keep track of their own progress and see how it compares to other classmates.

Go [here](https://nus-cs2103-ay2627-s1.github.io/dashboards/) to see all dashboards used by the course.
</box>

---------------------------------{.dotted .border-info}

## Exam{.text-info}

The final exam is designed to scale to a large class (e.g., minimize manual grading).

There are two main components:

1. **A UML diagram drawing task.**

<div class="indented">
<panel type="info" header="Sample question" minimized>

(a) Sketch a class diagram for the code given below. Also incorporate the following information into the diagram:
* An  `Activity` object can consist of other `Activity` objects i.e., sub-activities.
* A  `Watcher` object may not be associated with more than 5 `Activity` objects.
* `UiWidget` class inherits the `ProgressWatcher`.

```java
class Activity{
    private Watcher[] watchers = new Watcher[ProgressWatcher.MAX];
    //...

    void watch(Watcher w){
        //add w to watchers
    }

    Activity getInstance(){
        //...
    }
}
```
```java
interface Watcher{
    void update(int value);
}
```
```java
abstract class ProgressWatcher implements Watcher{
    static int MAX = 10;
}
```
(b) Sketch an object diagram that has two `Activity` objects `a1` and `a2`, both being watched by a `UiWidget` object `u`. Furthermore, `a2` is a sub-activity of `a1`.

----

**Model answer:**

<pic eager src="images/sample-uml-drawing-question-answer.png"></pic><p/>

**Explanation:** The purpose of this type of question is to check whether students can document their code using UML diagrams. Typically, the exam has one question on a UML structure diagram (such as the question above) and another that focuses on a behavior diagram (e.g., a UML sequence diagram).
</panel>
</div>
<p/>


2. **Multiple-choice questions, each paired with a 'short-answer' question.** Some of the questions are based on the UML diagram drawn in (1) above. The exam is conducted using Examplify.

<div class="indented">
<panel type="info" header="Sample question" minimized >

**MCQ question:** Given below are some changes Tom made to his code. Which is not a refactoring?

- ( ) Tom removes braces around an `if` block because there is only one statement in the block.
- ( ) Tom finds the `sort()` function doesn't work when the list is empty. He adds an exception to handle that case.
- ( ) Tom merges two classes into one bigger class.
- ( ) Tom thinks the `add()` function is too long. He applies the SLAP technique to it.
- ( ) Tom finds that a variable name used is misleading. He changes it to a better name.

**Follow-up question:** Why is it not a refactoring?

-----------

**Model Answer**

> - (x) Tom finds the `sort()` function doesn't work when the list is empty. He adds an exception to handle that case.
>
> Reason: This alters the behavior, whereas refactoring should not.

**Explanation:** This question checks whether students can apply their knowledge of refactoring to a given context and distinguish refactoring from other code changes.

</panel>
</div>
<p/>

As the course is heavy on the practice side, it does not contain a heavy/deep theory component. Therefore, the **exam assesses whether students can _fluently_ apply a variety of concepts in a real project context**, by requiring students to answer questions at a rapid pace (e.g., 2 minutes per MCQ + Short answer question pair).

The exam is closed book, but we provide a cheat sheet through Examplify ([example from the previous semester](exam-reference-sheet.html)). In addition, students can bring their own one-page cheat sheet.

----------------------------{.thick-1 .border-danger}

# Challenges{.text-danger}

Although most of our students are academically strong, they lack programming experience outside of school courses. Preparing them to work on an actual SE project is a formidable challenge, especially at a scale of about 500 students per semester.
Following from the main goal of the course (i.e., preparing students for internships), there are two key requirements that make CS2103/T harder to run than a typical first SE course:

1. **The need to train students on the iterative software development process**: While the more common approach is for the first SE course to train students in a _sequential_ (i.e., _waterfall_) process and move to an _iterative_ process in the second SE course, this course needs to train students in the more industry-friendly iterative process from the beginning, as some may go for internships before taking a second SE course.
2. **The need to train students to work in both greenfield and brownfield projects**: As internships can involve both types of projects, we need to train students for both.

---------------------------{.dotted .border-danger}

### Challenge 1: Iterative topic delivery can disorient students.{.text-danger}

When following an iterative process in the project, topic coverage itself needs to be iterative i.e., cover basics of all topics first, and go progressively deeper into all topics (in parallel) as the semester progresses. %%Reason: we cannot spend the first few weeks on the topic of _Requirements_ alone because students need to know about design, implementation, testing, etc. when doing their first iteration of the project%%. However, iterative topic coverage results in each topic being delivered as multiple fragments over many weeks, which can disorient students and make it harder for them to see the 'full picture'. The [course timeline](../schedule/timeline.html) page shows how the course jumps between multiple topics every week.

**Solution: A full-fledged course website to guide students through the course contents.** We built a website authoring tool called [MarkBind](https://markbind.org) that we then used to create the course website. MarkBind is able to present the same content in different ways without duplicating content. Here is an example of how this helps with the disorientation caused by the iterative topic delivery:
 * The topics covered each week are presented as a separate page (e.g., the [Schedule -> Week 7 -> Topics](../schedule/week7/topics.html) page), with additional commentary (in light green boxes) to guide students through the topics.
 * The same content is presented in logical order on the [Textbook page](../se-book-adapted/index.html). Students can use it when studying for exams at the end of the semester or looking up a topic.

---------------------------{.dotted .border-danger}

### Challenge 2: Iterative is hard for beginners.{.text-danger}

Iterative is hard for beginners because there are many things (i.e., design, implementation, testing, etc.) happening at once.

**Solution: Give fine-grained guidance.** Each week, we give detailed guidance on what students should be doing in their project. These tasks are designed to tie in with what they have learned so far. Examples:
* The page [Schedule -> Week 7 -> Project](../schedule/week7/project.html) explains what to do in the iP (i.e., the individual project) and the tP (i.e., the team project) in that week.
* Starting from [this page](ip-overview.html), the next several pages explain how the individual project needs to progress over the following weeks.

---------------------------{.dotted .border-danger}

### Challenge 3: Temptation to fake 'iterative'.{.text-danger}

Given that the iterative process is harder to follow and requires consistent effort throughout the project, there is a temptation for students to 'fake' an iterative process and do everything in the last few weeks using a waterfall process.

**Solution: Monitor project progress closely.** We monitor project progress and provide dashboards that students can also use to self-monitor:

* [The iP progress dashboard](https://nus-cs2103-ay2627-s1.github.io/dashboards/contents/ip-progress.html) shows which individual project tasks each student has done.
* [The iP code dashboard](https://nus-cs2103-ay2627-s1.github.io/ip-dashboard/?search=&sort=groupTitle&sortWithin=title&timeframe=commit&mergegroup=&groupSelect=groupByRepos&breakdown=true&viewRepoTags=true&checkedFileTypes=java~md~fxml~sh~bat~gradle~txt) shows coding activities in the individual project, e.g., the code written by each student and when students commit code.
* [The iP comments dashboard](https://nus-cs2103-ay2627-s1.github.io/dashboards/contents/ip-comments.html) shows code review comments given by students for others' iP code.
* The team project progress is monitored using a similar set of dashboards too ([example](https://nus-cs2103-ay2627-s1.github.io/dashboards/contents/tp-progress.html)).

---------------------------{.dotted .border-danger}
### Challenge 4: Rigorous project grading is hard.{.text-danger}

Given the large class size, evaluating the projects fairly, uniformly, and rigorously is hard.

**Solutions: Leverage peer evaluations and crowdsourcing.** One good example is the [practical exam (PE)](tp-pe.html) that we do at the end of the team project. In the PE, each project deliverable is independently tested by 5-6 other students. The testers earn marks by finding bugs in the product they are testing, and the developers lose marks if others find bugs in their product. This motivates students to test the product and documentation intensively and, more importantly, to avoid bugs in their own product from the start.


---------------------------{.thick-1 .border-success}

# Achievements{.text-success}

The following are some notable achievements of the course.

---------------------------{.dotted .border-success}

### Achievement 1: Concrete evidence of SE competence{.text-success}

At the end of the semester, each student produces and makes publicly available the following concrete evidence of their SE competence.

* A small software product built from scratch, together with a User Guide.
* A contribution to a brownfield project, together with a User Guide ([example](https://ay2526s1-cs2103t-t13-1.github.io/tp/UserGuide.html)) and a Developer Guide ([example](https://ay2526s1-cs2103t-t13-1.github.io/tp/DeveloperGuide.html)).

Their work (e.g., committed code, reviewed pull requests, created issues, and document updates) is available for scrutiny by anyone.

---------------------------{.dotted .border-success}

### Achievement 2: Well-received despite many 'unpopular' choices{.text-success}

This course makes several 'unpopular' choices, some of which are listed below:

1. **Our approach: Lectures give only a preview of the topics** and the motivation for learning them.<br>
   Rationale: To encourage self-learning at own pace.<br>
   Students prefer: Lectures going through the content in detail.

1. **Our approach: Lecture slides are printer-unfriendly**, optimized for lecture delivery only.<br>
   Rationale: To encourage students to use the textbook instead of relying on slides as the sole source of content.<br>
   Students prefer: Slides that can be printed and used as study materials.

1. **Our approach: Tutors are not allowed to give technical help.** We require students to resolve technical issues via the [course forum]({{url_forum}}). Forum use is monitored ([example](https://nus-cs2103-ay2223s1.github.io/dashboards/contents/forum-activities.html)) and rewarded.<br>
   Rationale: To encourage peer support and wean students off relying too heavily on tutors to solve technical problems.

1. **Our approach: Tutors are not allowed to give specific feedback on students' project work.** Instead, we use alternative means to guide students through the project (e.g., discuss a hypothetical project to figure out common mistakes students make in the project).<br>
   Rationale: To encourage students to make their own project decisions and prevent tutors from influencing project outcomes.

1. **Our approach: Many deliverables, every week.** This [Summary of the Course Timeline](../schedule/timeline.html) page shows how many project and admin tasks are due in each week. In addition, most weeks have optional in-lecture and in-video quizzes, not forgetting the tutorial tasks ([example](../schedule/week7/tutorial.html)).<br>
   Rationale: To ensure students learn and apply the topics in a timely manner, rather than try to do everything near the end of the semester.

1. **Our approach: Require students to use an existing codebase** for the team project, and a pre-selected tool stack, and follow a prescribed workflow in the project (e.g., follow a [forking workflow](https://git-mastery.org/lessons/forkingWorkflow/)).<br>
   Rationale: To train students to work with legacy code, and follow workflows used in the industry.<br>
   Students prefer: Full freedom to build whatever product they want using their preferred tool stack and simpler workflows (e.g., everyone commits to the master branch).

1. **Our approach: Get students to test each other's products**, report bugs, and respond to reported bugs.<br>
   Rationale: To achieve a higher rigor in testing the quality of student work.<br>
   Students prefer: Teaching team does all the evaluations.

Despite these unpopular choices, students have given the course reasonable feedback over many semesters. Course ratings have not fallen far below the department norm for courses of this size, and instructor ratings have remained above the department average.

---------------------------{.dotted .border-success}

### Achievement 3: Scaled up without losing rigor{.text-success}

While SE courses are notoriously hard to scale, we have done reasonably well in scaling this course to 500+ students, without a significant drop in rigor of evaluation, and without a significant increase in teaching resources (e.g., tutor hours).
Strategies used:

1. **Heavy use of automation**: The course relies heavily on automation, supported by about 20,000 LoC of Python scripts, e.g., to generate dashboards from various data sources. In addition, the course uses the following EdTech tools, which students built primarily to support this course and which other courses now use as well:
   * [Git-Mastery](https://git-mastery.org/#/cs2103): A resource for students to learn, practice, and self-check Git skills.
   * [MarkBind](https://markbind.org): Used to create the course website
   * [TEAMMATES](https://teammatesv4.appspot.com/): For peer evaluations
   * [RepoSense](https://reposense.org): To generate code dashboards
   * [se-education.org](https://se-education.org): To provide project templates, tech guides, etc.<p/>

1. **Leverage peer input**: Students contribute to guiding and evaluating other students. For example, scripts and peers grade the iP except in a small number of cases (about 5%) that require tutor intervention.

----------------------------{.thick-1}

# Future work

The heavy workload remains a concern, according to the [mid-term survey](mid-semester-survey-results.html).

Providing adequate and personalized help to struggling students is another challenge that becomes harder in a class of this size.
