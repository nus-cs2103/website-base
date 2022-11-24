
<p class="lead">There is no midterm exam. Information about the final exam is given below.</p>

{% if (current_week | int) < 11 %}
<box type="important">

Instructions below are from the previous semester. Will be updated closer to the exam.
</box>
{% endif %}


1. The final exam will be **as per the normal exam schedule** (you can check exam time from [NUSMods](https://nusmods.com/modules/)), and will count for **{{ marks_exam }}% of the final grade**.
1. The exam will be done **face-to-face, but using Examplify**. SCALE is not allowing remote exam this semester except in some special cases.<br>
  Please use these resources if you haven't used Examplify in the recent past (the behavior may be different from the version you used last semester):
   * [slides](https://wiki.nus.edu.sg/x/daBJCw) (refer to the slides on _On-Campus exam_)
   * [video](https://wiki.nus.edu.sg/x/tgg_EQ) (refer to the _Examplify Student Briefing_ video)
   * try a few practice exams provided in the above two
   * write to NUS CIT (citbox25@nus.edu.sg) if you run into any technical issues
1. You will ==need to **bring your own laptop**==, which can connect to the NUS wifi network.
   * <span class="text-danger">iPads are not allowed</span> as our exam configuration is not compatible with the iPad Examplify app.
   * Only one device per person is allowed for the exam.
1. ==**Recording of your PC screen** is not required.==
1. **Any soft/hard copies of notes are allowed**, including hand-written notes.
1. **Internet is not allowed**.<br>
   You are recommended to have a soft copy of the textbook, the coding standard, and any other relevant document on your exam device.
1. **Download the exam (both parts) before you come to the exam**. We'll give you the password for opening the exam paper at the starting time of the exam.
1. **If you have a doubt/query about a question**, or want to make an assumption about a question, please write it down in the 'feedback' text box. ==Do not try to communicate those with the invigilator during the exam.== We'll take your doubt/query/assumption into account when grading. For example, if many had queries about a specific question, we can conclude that the question is unclear and omit it from grading.

<include src="exam-doubts-fragment.md" />

9. **Bring your computer fully charged** (and bring the charger too), although some charging points will be available at the exam venue.
   * **FAQ:** My laptop battery is weak. Can I be put in a seat near a charging point?<br>
   **A**: The standard operation procedure for digital exams: Some venues have charging points within reach of every seat. If that's not the case, you will be moved to another location with a charging point when your laptop power level reaches a low level. Pre-allocating you a seat with a charging point is not feasible, as the number of such requests can easily exceed the number of charging points in the venue.
10. **You must start the exam within 5 minutes of receiving the password** or else the quiz will close before your allotted time has run out.

## Format

* The exam will be divided into 2 parts.

### Final exam - part 1

* This exam contains 16 MCQ questions. All questions are estimated to be equal size/difficulty.
* You only need to answer 15 questions correctly to get full marks. The extra question is there to cushion you against careless mistakes or misinterpreting a question.
* Questions will appear in random order.
* **You will not be able to go back to previous questions.**<br>
  %%Reasons:<br>
  1\. to minimize opportunities for collusion<br>
  2\. not unreasonable for the materials tested and the proficiency level expected -- i.e., when using this knowledge in a real life SE project discussion, it will be rare for you to go back to revise what you said earlier in the discussion%%
* Duration: **45 minutes** (recommended: allocate 2.5 minutes per question, which gives you a 5 minutes buffer)
* **Most MCQ question will also have a follow up question.**<br>
  Answering at least 75% of the follow-up questions can earn you full marks for follow up questions.<br>
  **Submitting the answer to a fullow up question is done the same as submitting feedback for a question** (explained above), repeated below for your reference:

<include src="exam-follow-up-questions-fragment.md" />


* Here is an example question. The answer is `a` and the justification can be `OOP is only one of the choices for an SE project`.
<div class="indented-level2">

<panel haader="A sample question" expanded >

Choose the <span class="text-danger">**incorrect**</span> statement.

<span class="text-info">[Justification: Why is it incorrect?]</span>

A. Software engineering projects always use OOP.<br>
B. Some software engineering projects can be large and complex.<br>
C. Some software engineering projects can go on for many years.<br>
D. Software projects can involve people who are not software engineers.

</panel>
<p/>
</div>

* Here is another example question. Note the ==[**SELECT ALL**]== which tells you that this question can have multiple correoct answers and you need to select all of them i.e., it is a checkbox type question<br>
  The answer is `A`, `B`, `C` (and the rationale is `A` and `B`).

<div class="indented-level2">

<panel haader="A sample question" expanded >

==[**SELECT ALL**]== Which are UML diagrams covered in the module?.

<span class="text-info">[Justification: Which two are closely related to each other?]</span>

A. Class diagrams.<br>
B. Object diagrams.<br>
C. Activity diagrams.<br>
D. Gantt charts.

</panel>
<p/>
</div>


### Final exam - part 2

* Similar to part 1 (e.g., 16 questions, same length).


## Exam briefing, mock exam, practice exam paper

* There will be an exam briefing in the penultimate lecture. It will include a minimal mock exam, just to help you understand the structure.
* You will be given a practice exam paper (at least half the size of the full paper) to help you practice timing. That practice paper will be released at least one week before the exam.
