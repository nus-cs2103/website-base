{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("exams") %}
<div id="main">


<p class="lead">There is no midterm exam. Information about the final exam (which counts for {{ marks_exam }}% of the final grade) is given below.</p>

{% if (current_week | int) < 11 %}
<box type="important">

Instructions below are from the previous semester. Will be updated closer to the exam.
</box>
{% endif %}


<div tags="m--cs2113">

* The exam is open-book.
* We will use Examplify for the final exam this time.
* Examplify is set to block internet access during the exam.
* However, you are allowed to refer to the PDF version of the textbook and your own notes on your laptop.
* Permitted materials: <br>
  PDF of the module textbook, lecture slides (allowed format: PPT/PDF), self-created notes (please convert everything to PDF). <br>
  A printed copy of the module textbook, hand-written notes. <br>
  No other device other than the laptop you are using to take the exam is allowed; however, NUS-approved calculators are allowed.

## Exam structure

The exam duration is 90 minutes.

The final exam has two types of questions:
1. MCQ questions - includes True/False like concept questions and some multiple choice/response questions
2. Short-answer questions

<br>

* All questions will be displayed at once as Examplify doesn't allow creating sections
* Based on the question you are answering, you need to manage your time appropriately
* Weightage of the questions will be displayed to help you with time management


## Exam briefing, mock exam, practice exam paper

* There will be an exam briefing in the penultimate lecture that covers Examplify usage.
* You will be given a practice exam paper (smaller than the full paper) to help you practice timing. That practice paper will be released at least one week before the exam.
</div>

<div tags="m--cs2103 m--tic2002 m--tee3201">

1. **Schedule/venue:** The final exam will be as per the normal exam schedule, which will be sent to you by the Registrar's Office (or you can find via EduRec -> Academics -> Exams -> View exam schedule). You can find the date/time from [NUSMODS](https://nusmods.com/modules/{{ module }}) as well.
1. **Mode: F2F, using Examplify**. You ==need to **bring your own device**== (<span class="text-danger">iPads not allowed</span>), which can connect to the NUS wifi network.<br>
  Please use these resources if you haven't used Examplify in the recent past (the behavior may be different from the version you used last semester):
   * [slides](https://wiki.nus.edu.sg/x/daBJCw) (refer to the slides on _On-Campus exam_)
   * [video](https://wiki.nus.edu.sg/x/tgg_EQ) (refer to the _Examplify Student Briefing_ video)
   * try a few practice exams provided in the above two
   * write to NUS CIT (citbox25@nus.edu.sg) if you run into any technical issues.
   * if you do not have a working laptop for the exam, please contact IT Care itcare@nus.edu.sg directly for a laptop loan (for exam purpose only)
1. ==**Not required to record the screen**.==
1. **The exam is open-book. Soft/hard copies of documents are allowed**, including written notes.
1. **No Internet access** will be allowed during the exam. However, you need to be connected to the WiFi (for Examplify to upload your answers).
   * Examplify will be configured to disable Internet access while you are answering questions on Examplify.
   * Even when Examplify is not blocking the Internet, you are not to access the Internet.
   * Exit all non-essential applications (e.g., Telegram) that may be running in the background and connected to the Internet.
   * <span class="text-danger">You are strongly discouraged from using ~~Do not use~~ Web Browsers</span> to view local files.<br>
     %%Reason: invigilators will not be able to distinguish viewing local files from visiting online websites, and might have to talk to you (while the exam clock is still running) to verify that you are not accessing external sites%%.
1. **Use of other software applications** (e.g., note taking applications) during the exam: you should not use any special-purpose application that can,<br>
   &nbsp;&nbsp;(a) give you an unfair advantage over the other exam takers, or,<br>
   &nbsp;&nbsp;(b) go against the goal of the exam,<br>
   even if your action was not explicitly prohibited by the exam rules.
1. **Download all parts of the exam before you come to the exam** ({% if cs2103 %}parts 1 & 3 from Examplify, part 2 PDF file from Luminus{% else %}i.e., parts 1 & 2{% endif %}). We'll give you the password for opening each part at the exam, at the respective starting time of each part.
1. **If you have a doubt/query about a question**, or want to make an assumption about a question, please write it down in the 'NOTES' text box. ==Do not try to communicate those with the invigilator during the exam.== We'll take your doubt/query/assumption into account when grading. For example, if many had queries about a specific question, we can conclude that the question is unclear and omit it from grading.

<include src="exam-doubts-fragment.md" />


7. **Bring your computer fully charged** (and bring the charger too), although some charging points will be available at the exam venue.
   * **FAQ:** My laptop battery is weak. Can I be put in a seat near a charging point?<br>
     **A**: The standard operation procedure for digital exams: Some venues have charging points within reach of every seat. If that's not the case, you will be moved to another location with a charging point when your laptop power level reaches a low level. Pre-allocating you a seat with a charging point is not feasible, as the number of such requests can easily exceed the number of charging points in the venue.
1. **You must start the exam within 5 minutes of receiving the password** or else the quiz will close before your allotted time has run out.


## Format
<div tags="m--cs2103 m--tic2002 m--tee3201">

* The exam will be divided into {{ 3 if cs2103 else 2 }} parts.
* Although the official duration of the exam is 1.5 hours, note that the actual exam might take up to 2 hours (due to technical issues). So, please don't schedule anything important right after the exam.

### Final exam - part 1

* A quiz containing 16 MCQ questions. All questions are estimated to be equal size/difficulty.
* You only need to answer 15 questions correctly to get full marks. The extra question is there to cushion you against careless mistakes or misinterpreting a question.
* Questions will appear in random order.
* You will not be able to go back to previous questions.<br>
  %%Reasons:<br>
  1\. To minimize opportunities for collusion or over-the-shoulder copying from others.<br>
  2\. Not unreasonable for the materials tested and the proficiency level expected -- i.e., when using this knowledge in a real life SE project discussion, it will be rare for you to go back to revise what you said earlier in the discussion%%
* Duration: **{{ 45 if tic2002 else 35 }} minutes** <span tags="m--cs2103">(recommended: allocate 2 minutes per question, which gives you a 3 minutes buffer)</span>
* Most MCQ question have a short-answer follow up question.
**Use the 'NOTES' feature of Examplify to answer the follow-up question** (explained above), repeated below for your reference:

<include src="exam-follow-up-questions-fragment.md" />

* **To get full marks for follow-up questions, you only need to submit at least 75% of them.**<br>
  %%The bar is set lower than 100% as a cushion against you forgetting to answer a few follow-up questions before moving to the next question.%%
* Here is an example question. The answer is `a` and the answer to the follow-up question can be `OOP is only one of the choices for an SE project`.
<div class="indented-level2">

<panel header="Sample question 1" expanded >

Choose the incorrect statement.

<span class="text-info">[Follow-up question: Why is it incorrect?]</span>
- ( ) a. Software engineering projects always use OOP.
- ( ) b. Some software engineering projects can be large and complex.
- ( ) c. Some software engineering projects can go on for many years.
- ( ) d. Software projects can involve people who are not software engineers.
- ( ) e. Software engineering projects can deliver the end product incrementally.

</panel>
<p/>
</div>

* Here is another example question. Note the ==[**SELECT ALL**]== which tells you that this question can have multiple correoct answers and you need to select all of them i.e., it is a checkbox type question<br>
The answer is `C`, `D` (answer to teh follow-up question: `A` and `B`).

<div class="indented-level2">

<panel header="Sample question 2" expanded >

==[**SELECT ALL**]== Which of these are UML diagrams depicting behavior (as opposed to structure)?.

<span class="text-info">[Follow-up question: Which two are closely related to each other?]</span>

A. Class diagrams.<br>
B. Object diagrams.<br>
C. Activity diagrams.<br>
D. Sequence diagrams.<br>
E. Gantt charts.

</panel>
<p/>
</div>

<div tags="m--cs2103">

### Final exam - part 2

* You will be asked to draw some UML diagrams, **to be hand-drawn on paper** (not on a tablet).<br>
  You may use pencils if you wish.
* Duration: 20 minutes
* The questions will be in an encrypted PDF file that will be given to you in advance. The password will only be given at the start of this section.
* **Bring the following when you come to the exam:**
  * **1-2 sheets of A4 size paper**, for drawing diagrams.
  * Recommended: Something with a hard flat surface (e.g., a hardcover book) to put underneath the papers when drawing the diagrams. This is in case the arm rest of the exam venue chairs doesn't have enough space for both your laptop and drawing work.
* At the _end_ of the exam (i.e., after all three parts are over), you need to submit the diagrams.
* These diagrams will not be graded directly. Instead, you will use them when answering part 3 of the exam.<br>
  However, we may use the diagrams to give _some_ consolation marks should you score very low in the corresponding MCQ questions.
</div>

### Final exam - part {{ 3 if cs2103 else 2 }}

* Similar to part 1 (e.g., 16 questions, same length).{% if cs2103 %}
* Some questions will refer to the UML diagrams that you drew in part 2.
* <span class="text-danger">After the part 3 password has been released, you are not allowed to update the UML diagrams, _until_ you start the part 3.</span><br>
  %%Reason: to prevent students delaying the start of part 3 to gain extra drawing time.%%
* You _may_ modify your UML diagrams _after_ you have started part 3 on Examplify.<br>
  %%Reminder: diagrams are not graded.%%
* You may refer the PDF file used in part 2 during this part too.
{% endif %}

</div>

## Exam briefing, mock exam, practice exam paper

* There will be an exam briefing in the penultimate lecture. It will include a minimal mock exam, just to help you understand the structure.
* You will be given a practice exam paper (at least half the size of the full paper) to help you practice timing. That practice paper will be released at least one week before the exam.
* Your score and answers for the mock/practice exams can be retrieved by visiting [https://examsoft.com](https://apac.examsoft.com/GKWeb/login/NUS).

</div>

</div>

{% endcall %}
