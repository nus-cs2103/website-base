{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/topics.njk" import panopto with context %}

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
  PDF of the course textbook, lecture slides (allowed format: PPT/PDF), self-created notes (please convert everything to PDF). <br>
  A printed copy of the course textbook, handwritten notes. <br>
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

<div tags="m--cs2103">
<div id="exam-briefing-video">

{{ panopto("2ab962b5-554e-41be-9df3-b14f00fd2cb8", desc="[Course Briefing Video] Final Exam (12 minutes)", start_week="13") }}
</div>

## Exam admin info to note

1. **Schedule/venue:** The final exam will be as per the normal exam schedule, which will be sent to you by the Registrar's Office (or you can find via EduRec -> Academics -> Exams -> View exam schedule). You can find the date/time from [NUSMODS](https://nusmods.com/modules/{{ course }}) as well.
1. **Scope:**
   * All topics in the textbook, excluding level 4 topics (i.e., optional topics), are examinable. For your convenience, you can view the examinable portion of the textbook in [this printable view of the textbook](../se-book-adapted/print.html) (same as the PDF version of the textbook provided to you).
   * In addition, you are expected to be aware of SE-related things (i.e., tools, techniques, concepts) encountered while dong the iP and the tP %%e.g., Was testing technique X used in the tP?%%.<br>
     That is, you are expected to strengthen your SE _knowledge_ (not just hands-on skills) as you do the course projects -- in particular, to be able to connect theory to practice.
1. **Mode: F2F, using Examplify**. You ==need to **bring your own device**== (<span class="text-danger">iPads not recommended</span>), which can connect to the NUS Wi-Fi network.<br>
  Please use these resources if you haven't used Examplify in the recent past (the behavior may be different from the version you used last semester):
   * [NUS Guides on Examplify](https://nus.atlassian.net/wiki/spaces/DAstudent/overview)
   * try a few practice exams provided in the above two
   * write to NUS CIT (citbox25@nus.edu.sg) if you run into any technical issues.
   * if you do not have a working laptop for the exam, please contact IT Care itcare@nus.edu.sg directly for a laptop loan (for exam purpose only)
1. ==**Examplify will use the fully locked-down**== mode during the exam. You will not be able to access Internet or any other applications/files in the computer.
1. **The exam is open-book. Any written/printed documents are allowed, but hard copies only**.<br>
   A PDF _Exam Reference_ file containing the full textbook, UML reference sheet, and the coding standard will be available within Examplify. We'll give you a copy of that file in advance %%(so that you can know what exactly is in that file)%%.<br>
   Yes, Examplify allows you to search in that PDF file.
1. **Not required to record the screen**.
1. **Download all parts of the exam before you come to the exam** (i.e., parts 1, 2{% if cs2103 %}, 3{% endif %}). We'll give you the password for opening each part at the exam, at the respective starting time of each part.<br>
  You will be notified when they are ready for download (typically, around 24 hours before the exam start time).
1. **If you have a doubt/query about a question**, or want to make an assumption about a question, please write it down in the 'NOTES' text box. ==Do not try to communicate those with the invigilator during the exam.== %%(reason: at an exam of this scale, it is not practical to clarify such doubts on-the-spot on a timely manner)%%. We'll take your doubt/query/assumption into account when grading. For example, if many had queries about a specific question, we can conclude that the question is unclear and omit it from grading.

<include src="exam-doubts-fragment.md" />


9. **Bring your computer fully charged**, although some charging points will be available at the exam venue (so, bring the charger too).
   * **FAQ:** My laptop battery is weak. Can I be put in a seat near a charging point?<br>
     **A**: The standard operation procedure for digital exams: Some venues have charging points within reach of every seat. If that's not the case, you will be moved to another location with a charging point when your laptop power level reaches a low level. Pre-allocating you a seat with a charging point is not feasible, as the number of such requests can easily exceed the number of charging points in the venue.
10. **You must start the exam within 5 minutes of receiving the password**.


## Structure/format
<div tags="m--cs2103 m--tic2002 m--tee3201">

* The exam will be divided into {{ 3 if cs2103 else 2 }} parts.
* Although the official duration of the exam is 1.5 hours, note that the actual exam might take up to 2 hours (due to technical issues). So, please don't schedule anything important right after the exam.

### Final exam - part 1

* A quiz containing 16 MCQ questions. All questions are estimated to be equal size/difficulty.
* You only need to answer 15 questions correctly to get full marks. The extra question is there to cushion you against careless mistakes or misinterpreting a question.
* Questions will appear in random order.
* You will not be able to go back to previous questions.<br>
  %%Reasons:<br>
  1\. To minimize opportunities for collusion or over-the-shoulder copying from others (the risk of the latter is higher in this type of exam due to the upright exam device screens being easily visible to other exam takers).<br>
  2\. Not unreasonable for the materials tested, nature of the questions, and the proficiency level expected -- i.e., when using this knowledge in a real life SE project discussion, it will be rare for you to go back to revise what you said earlier in the discussion%%
* Duration: **{{ 45 if tic2002 else 35 }} minutes** <span tags="m--cs2103">(recommended: allocate 2 minutes per question, which gives you a 3 minutes buffer)</span>
* Most MCQ question have a short-answer follow-up question.
* Here is an example question. The answer is `a` and the answer to the follow-up question can be `OOP is only one of the choices for an SE project`.
<div class="indented-level2">

<panel header="Sample question 1" expanded >

Choose the incorrect statement.

- ( ) a. Software engineering projects always use OOP.
- ( ) b. Some software engineering projects can be large and complex.
- ( ) c. Some software engineering projects can go on for many years.
- ( ) d. Software projects can involve people who are not software engineers.
- ( ) e. Software engineering projects can deliver the end product incrementally.

Why is it incorrect? ______

</panel>
<p/>
</div>

* Here is another example question. Note the ==[**SELECT ALL**]== at the start of the question text, which tells you that this question can have multiple correct answers, and you need to select all of them i.e., it is a checkbox type question<br>
The answer is `C`, `D`.

<div class="indented-level2">

<panel header="Sample question 2" expanded >

==[**SELECT ALL**]== Which of these are UML diagrams depicting behavior (as opposed to structure)?.

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
* The questions will be in Examplify.
* **Bring 1-2 sheets of A4 size papers when you come to the exam:**
* These diagrams will not be graded directly. Instead, you will use them when answering part 3 of the exam.<br>
  However, we may use the diagrams to give _some_ consolation marks should you score very low in the corresponding MCQ questions.<br>
  For that purpose, the papers will be collected at the end of the full exam (i.e., after part 3 is over).
</div>

### Final exam - part {{ 3 if cs2103 else 2 }}

* Similar to part 1 (e.g., 16 questions, same length).{% if cs2103 %}
* Some questions will refer to the UML diagrams that you drew in part 2.
* <span class="text-danger">After the part 3 password has been released, you are not allowed to update the UML diagrams, _until_ you start the part 3.</span><br>
  %%Reason: to prevent students delaying the start of part 3 to gain extra drawing time.%%
* You _may_ modify your UML diagrams _after_ you have started part 3 on Examplify.<br>
  %%Reminder: diagrams are not graded.%%
* The _Exam Reference PDF_ file in this part will also include a copy of part 2 questions, in case you want to refer to them again during part 2 %%e.g., to check your diagram against the code given in the question%%.
{% endif %}

</div>

## Exam preparation resources

{% set handouts_link = "[Canvas/files/handouts](" + url_files +"/folder/handouts)" %}

<box type="info" seamless>

The following exam resources will be **available from the start of week 13**.
</box>

<include src="exams.md#exam-briefing-video" />


* **A mock exam** (consisting of just a few questions), via Examplify.
  You can use it to get familiar with the quiz format that will be used for the final exam.
  Password: `Hello123`<br>
  Model answers are in {{ handouts_link }}.
* **A practice exam** of same format/length/difficulty as the actual exam will be available at least one week before the exam.<br>
  You can use it to practice your timing/pace. Multiple attempts are allowed.
    * Recommended:
        * Watch the exam briefing video and finish studying the topics before
          you attempt the practice exam, to get its full benefit.<br>
        * Do the mock exam (to get used to the software and question structure) before the practice exam.
    * Where to find it: on Examplify. Password: `Hello123`
    * Model answers are available on {{ handouts_link }}.
* **Some extra practice questions** for exam part 2 are in
  {{ handouts_link }} -- look for the file `Additional practice questions for part 2.pdf`
* **All weekly quizzes** will be reopened on [Canvas Quizzes]({{ url_canvas_home }}/quizzes).
  You can retake them to self-test your knowledge (note: retaking them will not affect participation marks).
* **Recordings of all tutorial Zoom sessions** should be available in a file named `Recordings.docx` inside
  your tutorial group's MS Team (in the 'Files' section). Remind your tutor to update that file if recording
  links are missing.
* **Recordings of all weekly briefings** are available on the [Canvas home page]({{ url_canvas_home }}).
* **The _Topics Overview_ video** given below explains how course topics fit into a big picture, and as a bonus, touches on some exam-like questions as well.

{{ panopto(desc="[Course briefing video] **Topics overview** aka the 'big picture' (19 mins)", "e1bf94be-36e3-4ab1-8261-b14f00fd2cc9", start_week="13") }}

* **PDF files useful for the exam** (given in {{ handouts_link }}):
  * Exam Reference PDF
  * Topics infographic (shows how the various topics fit into the big picture)

</div>

</div>

{% endcall %}
