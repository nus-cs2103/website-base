<frontmatter>
title: "Admin Info"
pageNav: 2
</frontmatter>

{% from "common/macros.njk" import get_date with context %}
{% from "common/topics.njk" import panopto with context %}

<div class="website-content">

# **{{ course }} {{ course_name }}**

{{ line_dotted }}<!-- ................................................................................... -->

# Course overview
<div class="indented" id="course-info">

<pic src="{{baseUrl}}/images/growingPlant.png" width="700"></pic>

_TIC2002 Introduction to Software Engineering_ contains roughly a **50-50 balance of theory and practice** of SE. It covers the knowledge/skills necessary to do small software projects, and as such, it is **a first step towards preparing you to work in bigger SE projects**, which will be done in later courses.

<box type="tip" seamless>

**This course is optimized for SCALE students**{.text-success} so that you can _learn at your own pace_ even if you are not a full-time student: the need to attend lectures/tutorials at fixed times is low, deadlines are more flexible than usual, and the on-campus presence is optional.

e.g., **Instead of traditional instructor-led tutorials**, the course provides quizzes and other activities that you can do at your own time to self-test your knowledge. The instructor can be consulted if you need help with any of them.

</box>
</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Using this course website

<div class="indented" id="website-info">
<include src="usingThisWebsite.md#main" />
</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Instructors

<div class="indented">

<div class="container">
  <div class="row">
    <div class="col-3">

<img src="{{ baseUrl }}/admin/images/damith.png" width="175" class="rounded mt-1">
    </div>
    <div class="col">

<include src="instructor-damith-fragment.md" />
    </div>
  </div>
</div>

#### Tutors:

* **Richard Dominick**:&nbsp;&nbsp; %%:fas-envelope:%% <span id="ta-email">`dominick`[at]`u.nus.edu`</span>

</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Lectures + Tutorials
<div class="indented" id="lectures-info">

%%:far-clock:%% Tuesdays 6.30-9.30pm<br>
%%:fas-map-marker-alt:%% COM1-0207<br>

**A TIC2002 lecture + tutorial time is divided into three parts**, as follows:

* **[6.30-7.00pm] Pre-lecture consultations:**
  * You can use this time to get prof's help if you encountered problems while doing the previous week's tasks.
  * This session will be online. Communications with the prof is to be done using Microsoft Teams app.
    * If the question is is potentially relevant to others in the class, post your question in the chat room of the `TIC2002-{{ period }}` ([link]({{ url_ms_teams_class }})) MS Team.
    * Otherwise search for prof's name (`Damith Chatura RAJAPAKSE`) in MS Teams and send a private chat message.
* **[7.00-8.00pm] Lecture briefing**:
  * Will be done in Hybrid mode (i.e., you can attend F2F, or join via Zoom, or watch the recording later).
* **[8.00-9.30pm] Post-lecture consultations**:
  * This portion will start as soon as the previous portion  (i.e., the _lecture briefing_) ends.
  * During this time,
    * go through the week's lecture topics in the course website
    * do suggested activities/exercises in there (if any)
    * if you encounter any problems while doing the above or have a question, contact the prof/TA using MS-Teams or F2F.

**Lecture slides are not suitable to be used as reference materials** as they have been <tooltip content="i.e., heavy use of graphics and animations">optimized for lecture delivery</tooltip> instead. Use the textbook (not slides) as your main reference. Slides can be uploaded to Canvas if requested, _after_ the lecture.<br>

</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Textbook
<div class="indented">

<include src="textbooks.md#main" />

</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Programming language
<div class="indented" id="java">

This course uses Java. It assumes you are familiar with C++ basics and provides lessons to help you transition from C++ to Java.

{{ icon_important_big_red }} Install [JDK 11](https://www.oracle.com/technetwork/java/javase/downloads/jdk11-downloads-5066655.html) on your computer. Using other versions of Java is highly discouraged.

</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Programming exercises
<div id="exercises-info" class="indented">

In some weeks, there will be some programming exercises for you to submit (on Coursemology). You should do the exercises as you learn the topics.


<box type="warning" seamless>

==**Focus on learning the topic rather than finishing the exercises.**== While these are exercises provided to self-test your knowledge, the more important thing is to read and understand the topic content. Furthermore, not all topics are tested by exercises.
</box>

{{ icon_important_big_red }} Programming exercises are graded for participation.
</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Project
<div class="indented">

<div  id="project-info">

* The project is to be done **individually**.
* The project based on a [generic project called Duke](../se-book-adapted/projectDuke/index.html).
* In the project, you will build a small chatbot, using Java.
* The project is to be done in small increments. You will be given a schedule of what increments to be done in each week.
* Some weekly increments will be common to all students, while some will vary from student to student. That means your final product will be unique in terms of total features, but some features will be common to other students in the class.

</div>

Weekly project increments are given in the panels below:
<div class="indented">
{% for i in range(3, 14) %}
<panel header="**Week {{ i }}**">
<include src="../schedule/week{{ i }}/admin-tic2002-fragment.md#project" />
</panel>
{% endfor %}
</div>
<p/>
<div id="final-submission-info">

### Week 13: Final submission

**Deadline**: <span class="text-danger">{{ get_date(date_w13_start, 6, format=format_normal) }}</span> (Sunday of week 13)

* An extra week can be given (upon request) for a small late submission penalty of `-2` marks.
* Submissions later than the hard deadline are liable to a late submission penalty, to be fair to those who submitted on time. But given you are part-time students, late submission penalty will be more lenient than otherwise (e.g., `-1 per day`) and will be on a case-by-case basis.


****Deliverables****:

<box type="important" seamless>

Please upload items 2, 3, 4 as three separate files, using the three Canvas assignments provided. ==Do not put them into a single zip file==.
</box>

1. **Source code** of the working program: push to your GitHub repo.
1. **Product**:<br>
    i\. Create a JAR file for the final version of the code.<br>
    ii\. Copy it to an empty folder outside of your project folder, and test it (reason: to ensure the JAR file does not depend on a specific folder location for it to work).<br>
    iii\. Submit to Canvas, name: `{YourName}.jar` e.g., `JunHao.jar`
1. **Project report**: a single .docx (preferred) or a pdf file that ==follows the template file given== (available in Canvas/Files/Handouts).
   * Submission: Upload to Canvas. The file name should be your name e.g., `JunHao.docx`
   * [Optional] Feedback for an early draft of the project report:  Optionally, you can get prof's feedback on an early draft of the project report if you email a draft of the report to the prof <span class="text-danger">no later than {{ get_date(date_w13_start, 2, format=format_normal) }}</span> (Wednesday of week 13). Note that feedback on project report draft will be high-level feedback only (reason: the report is graded).
1. **Demo video**:
   * Record a demo video showcasing the features of your product.<br>
     You can use any screen recording software for this. One simple way is to start a Zoom meeting and record the meeting while screen-sharing your demo.
   * Use the exact version of the code you submitted (i.e., the demo should match the submitted code exactly).
   * Recommended length 7 minutes, max length 10 minutes.
   * Audio narration is optional if the demo can be understood without the audio.
   * Ensure the video is in a format that can be played by any computer.
   * Submission: Name the file with your name (to match the jar and the report file) and upload to Canvas.
1. **Code Reuse Declaration**:
   * Submit this survey (on Canvas) to declare your level of code reuse in the project.
   * This is compulsory. You <span class="text-danger">must submit this even if you did not reuse</span> any code.
</div>
</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Policies

<div id="deadlines-info">

### Deadlines
* Deadline for weekly tasks:
  * **If a specific deadline is given**, adhere to that.
  * **If no specific deadline is given**, try to complete tasks allocated to a week by Tuesday 6.30pm of the following week (i.e., before the next lecture). In case you fail to meet that deadline, you should still do those tasks as soon as possible. There will be no penalty if a task is done within a _grace period_ of one week after the deadline.

<div id="plagiarism-policy">

### Plagiarism

* You are allowed (and even encouraged) to discuss course tasks with others and help (and learn-from) each other. However, the submitted work should be largely your own.
* If you reuse/adapt code from elsewhere (e.g., from an online site such as stackoverflow), you must cite the source in the code. e.g.,
   ```java{.no-line-numbers}
   //Solution below adapted from https://stackoverflow.com/a/16252290
   {Your implementation of the reused solution here ...}
   ```

<include src="policies-fragment.md#cite-reuse-immediately" />

<include src="policies-fragment.md#using-tool-generated-code" />
</div>
</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Tools
<div class="indented">

### Zoom

Install Zoom in your computer. Installation and login instructions are [here](https://wiki.nus.edu.sg/pages/viewpage.action?spaceKey=THES&title=Proctoring+with+Zoom) (requires login).<br>
When using Zoom, remember to login using the `SSO` option and use your NUSNET account.

### Microsoft Teams (MST)

Install MST in your computer. Installation and login instructions are [here](https://wiki.nus.edu.sg/pages/viewpage.action?spaceKey=THES&title=Before+exams+-+Install+and+log+in+to+Microsoft+Teams) (requires login).<br>
When using MST, remember to login using your NUSNET account.

The MST team used for the class is `TIC2002-{{ period }}` ([link]({{ url_ms_teams_class }})).

<div id="git-info">

### Git, SourceTree

We'll be using Git as our revision control tool (compulsory).

{{ icon_important_big_red }} If you are not familiar with Git already, install [SourceTree](https://www.sourcetreeapp.com/) (a GUI for Git, but also contains Git) on your computer.

{{ icon_tip }} If you encounter issues connecting Sourcetree with your GitHub account, refer to these [Sourcetree Tips](https://se-education.org/guides/tutorials/sourcetree.html).
</div>
<div id="github-info">

### GitHub

We'll be using GitHub for code hosting (compulsory).

{{ icon_important_big_red }} Create a free GitHub account if you don't have one already.
</div>
<div id="coursemology-info">

### Coursemology

We'll be using Coursemology for coding exercises (compulsory).
* You'll receive the invitation link near to the first lecture.
* More info about assignment submission will be given in the first week's lecture.

</div>
<div id="intellij-info">

### Intellij IDEA

We'll be using Intellij IDE for programming. While using Intellij is not compulsory, there will be no help/instructions given for other IDEs.

{{ icon_info }} Install [Intellij](https://www.jetbrains.com/idea/) on your computer. You may use the Community Edition (free) or the Ultimate Edition (free for students).
</div>
</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Assessment
<div class="indented">

****[{{ 100 - (marks_exam | int) }}%] CA****
* **{{ marks_participation }}%: Participation** -- Each week has activities that can earn you participation points.<br>
  For you to be considered as _participated_ in a particular week, you need to earn at least half of available participation points in that week (e.g., if the eligible activities in a week offer a total of `5` points, you should earn at least `3` points).<br>
  To earn full {{ marks_participation }}% marks allocated for participation, you should have _participated_ (based on the above criterion) in at least 10 (out of 13) weeks.<br>
  You can track your participation points through the [Participation Dashboard]({{ url_participation_dashboard }}).<br>
  Given below are the typical activities that can earn you participation points:
  * **Weekly quizzes**:
    * When awarding participation points for quizzes, we look for two conditions:
      * Condition 1: submitted **_early_** i.e., before the next lecture
      * Condition 2: answered **_correctly_** i.e., least 70% of the answers are correct %%(reason: to discourage random answers)%%
    * You earn:
      * 3 points if you satisfy both conditions.
      * 2 points if only one of the conditions is satisfied.
      * 1 point if submitted but both conditions are not satisfied.
  * **Weekly programming exercises**: You can earn `3` points if you complete at least 80% of the exercises allocated for that week.
  * **Other admin activities**: Other admin activities such as submitting a survey can earn you `2` points, unless the activity specify a different number of points.
* **[{{ marks_ip }}%] Project**
  * **[{{ marks_ip_implementation }}%]** Features, code
  * **[{{ marks_ip_documentation }}%]** Documentation

****[{{ marks_exam }}%] Final Exam****

</div>

{{ line_dotted }}<!-- ................................................................................... -->

# Getting help

<span id="help-info">

If you face difficulties/doubts while learning the weekly topics, doing weekly exercises/tasks, here are the options to seek help:
1. **[Preferred] Post in [MS Teams ==channel for the class==]({{ url_ms_teams_class }})**:
   * If there is any chance that the question can be relevant to other classmates, post in the `General` channel.
   * Otherwise, post in the `YOUR_NAME - Help Channel` private channel we have created for each of you.
1. **Email `tic2002@comp.nus.edu.sg`**. These emails will be answered by the prof or forwarded to the TA for follow up.
1. You may also post in the [Canvas forum]({{ url_forum }}) or [Coursemology forum]({{ url_coursemology_classroom }}/forums).

</span>

{{ line_dotted }}<!-- ................................................................................... -->

# Exam
<div class="indented">

<include src="exams-f2f.md" />

</div>


</div>
