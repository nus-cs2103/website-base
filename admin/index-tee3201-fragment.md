<frontmatter>
title: "Admin Info"
header: header.md
footer: footer.md
head: adminHead.md
pageNav: 2
</frontmatter>

<div class="website-content" id="main">

# **TEE3201 Software Engineering**

<!-- .......................................................................................... --> {{ line_dotted }}

# Module overview
<div class="indented" id="module-info">

<img src="{{baseUrl}}/images/growingPlant.png" width="700">

_TEE3201 Software Engineering_ contains roughly a **50-50 balance of theory and practice** of SE. It covers the knowledge/skills necessary to do small software projects.
</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Using this module website

<div class="indented" id="website-info">
<include src="usingThisWebsite.md#main" />
</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Instructors
<div class="indented">

#### Lecturer
<div class="container">
  <div class="row">
    <div class="col-3">

<br>

![Damith]({{ baseUrl }}/admin/images/damith.png)
    </div>
    <div class="col">

**Damith Chatura RAJAPAKSE**<br>
Associate Professor, NUS School of Computing<br>
PhD, Software Engineering, NUS, 2002-2006<br>
BSc, Computer Science & Engineering, University of Moratuwa, 1996-2001<br>
%%:fas-envelope:%% <span id="prof-email">`damith`[at]`comp.nus.edu.sg`</span><br>
%%:fas-map-marker-alt:%% COM2-02-57<br>
%%:fas-phone-square:%% 651 64359<br>
%%:fas-home:%% https://www.comp.nus.edu.sg/~damithch
    </div>
  </div>
  <div class="row">

  </div>
</div>

#### Tutors:
* **Chan Weizhong**:&nbsp;&nbsp; %%:fas-envelope:%% <span id="ta-email">`chan.weizhong`[at]`u.nus.edu`</span>

</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Lectures + Tutorials
<div class="indented" id="lectures-info">

%%:far-clock:%% Tuesdays 1800-2130<br>
%%:fas-map-marker-alt:%% Venue: online (optional E3-06-08)<br>

**A TEE3201 lecture + tutorial time is divided into three parts**, as follows:

* 1800-1830: No formal lecture. This is a time for you to talk to the prof and clarify doubts about the previous week's topics. Use Microsoft Teams if you need to consult the prof during this time.
* 1830-1900: Do exercises related to previous week topics. Consult prof (via MS Teams) if you encounter problems.
* 1900-2000: Short Zoom lecture, introducing topics for the current week. After that, watch the pre-recorded videos and the textbook sections provided.
* 2000-2130: You can stay back and do exercises for the current week. Consult prof/TA (using MS Teams) for help as needed.<br>
{{ icon_tip }} ==If you prefer face-to-face interactions during this portion==, I can come to meet you f2f in the lecture venue (please let me know in advance).


**{{ icon_slides }} Lecture slides will be uploaded to LumiNUS after the lecture**, usually by midnight of the same day. **Lecture slides are not suitable to be used as reference materials** as they have been <tooltip content="i.e., heavy use of graphics and animations">optimized for lecture delivery</tooltip> instead.


</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Textbook

**Software Engineering Textbook**:

A customized **online text book** is used for this module. Topic coverage may not follow the exact topic sequence in the book. There are several ways for you to access the text book.
* Full version is [here]({{baseUrl}}/se-book-adapted/index.html): The relevant sections are embedded under the corresponding week in the [schedule page]({{baseUrl}}/schedule/index.html).
* {{ icon_print }} Printable version is [here]({{baseUrl}}/se-book-adapted/print.html). ==You are encouraged to use the online full version when possible== (instead of the printable version or the PDF version), as it has more content %%videos, exercises, etc.%%

**Programming Textbook**:

[An additional **guide on programming basics**]({{baseUrl}}/programming/index.html) is provided for you to get started or programming. The topics in that textbook are to help you do the programming part of the project; they are not examinable in the final exam. Furthermore, we try to use external resources as much as possible in our guide so that you can continue your learning using those resources beyond the scope of this module.

<!-- .......................................................................................... --> {{ line_dotted }}

# Programming Language

This module uses Python programming language to teach you programming basics required for software engineering. However, Python is not examinable.

**Install [Python (the latest 3.x version)](https://www.python.org/downloads/)** in your computer.

<!-- .......................................................................................... --> {{ line_dotted }}

# Programming Exercises
<span id="exercises-info">

In some weeks, there will be some programming exercises for you to submit (on Coursemology). You should do the exercises as you learn the topics.

<box type="warning">

**Learn the topic first before trying the exercises**. While these are exercises provided to self-test your knowledge, the more important thing is to read and understand the topic content. Furthermore, not all topics are tested by exercises.
</box>
</span>

# Project

<div  id="project-info">

* The project is to be done **individually**.
* The project based on a [generic project called Monty](../programming/chapters/monty.html).
* In the project, you will build a small chatbot, **using Python**.
* The project is to be done in small increments. You will be given a schedule of what increments to be done in each week.
* Some project increments will be common to all students, while some will vary from student to student (to be announced near to the date). That means your final product will be unique in terms of total features, but some features will be common to other students in the class.
* Constraints:
  1. You should not use relational/SQL databases e.g., MySQL
  1. The software should work in a Windows computer that has Python 3. If your software needs other software to be installed (e.g., third-party libraries), please get prof's permission first.
</div>

<panel header="### Weekly Project Increments">
{% for i in range(1, 14) %}

#### <span class="badge badge-dark">Week {{ i }}:</span>
<include src="../schedule/week{{ i }}/admin-tee3201.mbdf#week{{ i }}-project" />
<hr>
{%-endfor %}
</panel>
<p/>

<div id="final-submission-info">

### Week 13: Final Submission

**Submission Deadline**: Sunday of week 13 ({{ date_w13_start | date("YYYY-MM-DD", 6) }}). ==Submissions later than the deadline are liable to a late submission penalty==, to be fair to those who submitted on time. But given that you are part time students, the late submission penalty will be small (e.g., `-1` per day).
* **The deadline for seeking feedback on the project report draft**: ==week 13 lecture ({{ date_w13_start | date("YYYY-MM-DD", 1) }})==.
  * Preferred mode of feedback: ~~in-person (reason: it is hard to give written feedback on diagrams)~~ via email.
  * Such feedback will be limited to high-level comments only (reason: the report is graded), and given only once per student.

**Deliverables**:
1. **Code** of the working program: zip (not rar) the code.
   * Submission: Upload to LumiNUS/files folder named **`final-project-submissions/code`**
   * File name: `{Your Name}.zip` e.g., `Jun Hao.zip`
1. **Documentation**: a single .docx (preferred) or a pdf file that follows the template given (template file will be available in LumiNUS).
   * Submission: Upload to LumiNUS/files folder named **`final-project-submissions/report`**
   * File name: `{Your Name}.docx/pdf`  e.g., `Jun Hao.docx`
1. **Demo video**:
   * Record a demo video showcasing the features of your product.
   * Use the exact version of the code you submitted (i.e., the demo should match the submitted code exactly).
   * Recommended length 7 minutes, max length 10 minutes.
   * Audio narration is optional if the demo can be understood without the audio.
   * Ensure the video is in a format that can be played by any computer.
   * Submission: Upload to LumiNUS/files folder named **`final-project-submissions/demo`**
   * File name: `{Your Name}.mp4`  e.g., `Jun Hao.mp4`

</div>

<!-- .......................................................................................... --> {{ line_dotted }}

# Policies

<span id="deadlines-info">

### Deadlines
* Deadline for weekly tasks:
  * **If a specific deadline is given**, adhere to that.
  * **If no specific deadline is given**, 
    * Soft deadline: try to complete tasks allocated to a week before the following lecture.
    * Hard deadline: In case you fail to meet the soft deadline, there will be no penalty if a task is done within one week after the soft deadline.
</span>

<span id="plagiarism-info">

### Plagiarism
* You may view/discuss others' work or get help from others. However, <span class="text-danger"> ==the work you submit should be your own==. In case of similar submissions, marks will be divided among those submissions</span> e.g., if your submission scored 8/10 and there is another submission that is similar to your work (beyond coincidental similarity), each submission will get 4 marks.
</span>

<!-- .......................................................................................... --> {{ line_dotted }}

# Tools
<div class="indented">
<div id="coursemology-info">

### Coursemology

* We'll be using [Coursemology](http://coursemology.org/) for coding exercises (compulsory).
* You'll receive the invitation link near to the first lecture.
* More info about assignment submission will be given in the first week's lecture.


</div>
<div id="intellij-info">

### PyCharm

* PyCharm is the recommended Python editor. While using PyCharm is optional, there will be no help/instructions given for other editors.

* In the initial weeks, `repl.it` online editor is good enough for writing Python code. As your project code gets bigger in later weeks, you can consider installing [PyCharm](https://www.jetbrains.com/pycharm/download) on your computer. You may use the Community Edition (free) or the Professional Edition (free for students).
</div>
</div>
<!-- .......................................................................................... --> {{ line_dotted }}


# Getting Help
<span id="help-info">

If you face difficulties/doubts while learning the weekly topics, doing weekly exercises/tasks, here are the ways to get help, in the order of preference (most preferred on the top).
1. **Post in [MS Teams ==channel for the class==]({{ url_ms_teams_class }})**, rather than send a private message to the prof/TA. That way, either the prof or the TA can answer and the rest of the class can benefit from the answer.<br>
   If the question is not relevant to the rest of the class, prof/TA will contact you privately (via MS Teams) for follow up.
2. **Email `tee3201@comp.nus.edu.sg`**. These emails will be answered by the prof or forwarded to the TA for follow up.
3. **Send a private message** to the prof (search for `Damith Chatura Rajapakse`) or to the TA (search for `Chan Weizhong`) via MS Teams.
4. Email the prof at <include src="index-{{ module | lower }}.mbdf#prof-email" inline trim/> or the TA at <include src="index-{{ module | lower }}.mbdf#ta-email" inline trim/>
5. You may also post in the [LumiNUS forum]({{ url_forum }}) or [Coursemology forum]({{ url_coursemology_classroom }}/forums).

</span>
<!-- .......................................................................................... --> {{ line_dotted }}

<span id="assessment-info">

# Assessment

* **10%: Participation** -- To get full marks, submit weekly programming exercises and weekly project increments <trigger trigger="click" for="modal:adminInfo-deadlineInfo">on time</trigger>. In a week that has a quiz, they will be counted for participation as well.
* **30%: Project**
  * 10%: Documentation
  * 20%: Functionality, code
* **60%: Final Exam**
 

<modal large header="The Policy on Deadlines" id="modal:adminInfo-deadlineInfo">
  <include src="index-{{ module | lower }}.mbdf#deadlines-info"/>
</modal>

</span>

<!-- .......................................................................................... --> {{ line_dotted }}


# Exam

<div class="indented">

<include src="exams-f2f.md" />

</div>

</div>
