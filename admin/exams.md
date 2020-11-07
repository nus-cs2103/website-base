{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("exams") %}
<div id="main">


<p class="lead">There is no midterm exam. Information about the final exam is given below.</p>

* The final exam will be as per the normal exam schedule, and will count for {{ marks_exam }}% of the final grade.
* The exam will be done online.
* ==**We will be following the [SoC's E-Exam SOP](https://mysoc.nus.edu.sg/academic/e-exam-sop-for-students/)**==, combined with the deviations/refinements given in the section below. Please read the SOP carefully and ensure you follow all instructions.

## SOP deviations/refinements

1. **Tools: LumiNUS, Zoom, Microsoft Teams (MST), PDF scanner**, PDF reader.
1. ==**Recording of your PC screen** is not required.==
1. **Only one computer screen** is allowed.
1. **Not allowed to take printouts during the exam.**
1. **Soft copies of notes: only PDF format is allowed.** Other formats (e.g., MS Word, .txt, html) are not allowed.
1. **The Browser should only be used to access LumiNUS.** Accessing other websites (including the module website) is not allowed.
1. **Use Microsoft Teams (not Zoom) private messages to communicate with the prof**. Use Zoom PM only if you don't get a response via MST.
1. **The quiz will not appear on LumiNUS until a few minutes before we release the password**. Wait until we announce that the quiz is available to see.
1. **When the invigilator asks you to do an _identity check_**, turn your face towards the camera, move closer to the camera, remove face mask (if any), and hold the pose until the invigilator tells you to go back to your working position.

1. **If you have a doubt/query about a question**, or want to make an assumption about a question, please write it down in the 'justification' text box. ==Do not try to communicate those with the invigilator during the exam.== We'll take your doubt/query/assumption into account when grading. For example, if many had queries about a specific question, we can conclude that the question is unclear and omit it from grading.

1. **If you encounter a serious problem** that prevents you from proceeding with the exam (e.g., the password to open the quiz doesn't work), PM the invigilator using MS Teams (failing that, use Zoom chat).

1. **If your computer crashed/restarted** during the exam, try to get it up again and resume the exam. LumiNUS will allow you to resume from where you stopped earlier. However, note that there is a deadline to finish the quiz and you will overrun that deadline if you lose more than 5 minutes due to the computer outage.


## Format

* The exam will be divided into {{ 3 if cs2103 else 2 }} parts.

### Final exam - part 1

* A LumiNUS quiz containing 16 MCQ questions. All questions are estimated to be equal size/difficulty.
* You only need to answer 15 questions correctly to get full marks. The extra question is there to cushion you against careless mistakes or misinterpreting a question.
* Questions will appear in random order.
* You will not be able to go back to previous questions.<br>
  %%Reasons:<br>
  1\. to minimize opportunities for collusion<br>
  2\. not unreasonable for the materials tested and the proficiency level expected -- i.e., when using this knowledge in a real life SE project discussion, it will be rare for you to go back to revise what you said earlier in the discussion%%
* Duration: 35 minutes (recommended: allocate 2 minutes per question, which gives you a 3 minutes buffer)
* You are required to give a justification for your answer. ==The question will specify what should be included in the justification. **Answers without the correct justification may not earn full marks.**== However, we'll give full marks up to two correct answers (per 16 questions) that do not have justifications %%(to cater for cases where you accidentally proceeded to the next question before adding the justification)%%.
* Here is an example question. The answer is `a` and the justification can be `OOP is only one of the choices for an SE project`.
<div class="indented-level2">

<panel haader="A sample question" expanded >

Choose the incorrect statement.

<span class="text-info">[Justification: why is it incorrect?]</span>
- ( ) a. Software engineering projects always use OOP.
- ( ) b. Some software engineering projects can be large and complex.
- ( ) c. Some software engineering projects can go on for many years.

</panel>
<p/>
</div>

* {{ icon_tip }} Almost all questions will ask you to choose the INCORRECT statement and justify why it is incorrect.

* There will be a 5-minutes toilet break after this part

<div tags="m--cs2103">

### Final exam - part 2

* You will be asked to draw some UML diagrams, **to be hand-drawn on paper** (not on a tablet).
* Duration: 20 minutes
* The questions will be in an encrypted PDF file that will be given to you in advance. The password will only be given at the start of this section.
* At the end of the exam, you will be asked to show your diagrams to the camera, and then upload a scanned copy to LumiNUS.
* These diagrams will not be graded directly. Instead, you will use them when answering part 3 of the exam.<br>
  However, we will use the diagrams to give some marks should you score low in the corresponding MCQ questions.
</div>

### Final exam - part {{ 3 if cs2103 else 2 }}

* Similar to part 1.{% if cs2103 %}
* Some questions will refer to the UML diagrams that you drew in part 2.{% endif %}

## Exam briefing, mock exam, practice exam paper

* There will be an exam briefing in the penultimate lecture. It will include a minimal mock exam, just to help you understand the structure.
* You will be given a practice exam paper (half the size of the full paper) to help you practice timing. That practice paper will be released at least one week before the exam.

</div>

<!--
There is no midterm.

The final exam has two parts:
* Part 1: MCQ questions (1 hour, {{ marks_mcq }} marks)
* Part 2: Essay questions (1 hour, {{ marks_essay }} marks)

Both papers will be given to you at the start but you need to **answer Part 1 first** (i.e. MCQ paper). It will be **collected 1 hour after the exam start time** (even if arrived late for the exam). You are free to start part 2 early if you finish Part 1 early.

<box type="important">

Given the fast pace required by the paper, the large class size, and the need to collect part 1 answer scripts in the middle of the exam, to be fair to all students, **invigilators will not answer queries about the questions in the exam paper** (but _will_ answer queries related to exam administration).
* If you have a doubt/query about a question ,or would like to make an assumption about a question, or would like to report a potential error in the exam paper, write down your doubt/query/assumption in the space provided for it at the end of the exam paper.
* Those doubts/queries/assumptions (if justified) will be taken into account when grading.
</box>


## Final Exam: Part 1 (MCQ)

Each MCQ question gives you a statement to evaluate.

<box>

{{ icon_example }} An example statement

>Testing is a Q&A activity

</box>


Unless stated otherwise, the meaning of answer options are<br>
**A**: Agree. If the question has multiple statements, ++agree with all of them++.<br>
**B**: Disagree. If the question has multiple statements, ++disagree with at least one of them++<br>
**C**, **D**, **E**: Not used

Number of questions: {{ mcq_count }}

<div tags="m--cs2103">

Note that you have **slightly more than ½ minute for each question**, which means you need to go through the questions fairly quickly.
</div>

**Questions in Part 1 are confidential.** You are not allowed to reveal Part 1 content to anyone after the exam. All pages of the exam paper are to be returned at the end of the exam.

<div class="full-mode">

You will be given OCR forms %%(i.e., bubble sheets)%% to indicate your answers for Part 1. As each OCR form can accommodate only 50 answers, you will be given 2 OCR forms. **Indicate your student number in both OCR forms**.
</div>

To save space, we use the following notation in MCQ question.
 **[++x++ | y | ++z++] means ‘x and z, but not y’**

<box>

{{ icon_example }} SE is [boring | ++useful++ | ++fun++] means _SE is not boring_ AND _SE is useful_ AND _SE is fun_.

{{ icon_example }} Consider the following statement:

* IDEs can help with [++writing++ | debugging | ++testing++] code.

The correct response for it is `Disagree` because IDEs can help with all three of the given options, not just writing and testing.

</box>

Some questions will use ==highlighting== to draw your attention to a specific part of the question. That is because those parts are highly relevant to the answer and we don’t want you to miss the relevance of that part.

<box>

{{ icon_example }} Consider the statement below:

> Technique ABC ==can== be used to generate more test cases.

The word ==can== is highlighted because the decision you need to make is whether the ABC _can or cannot_ be used to generate more test cases; the decision is not whether ABC can be used to generate _more or better_ test cases.

</box>

Markers such as the one given below appears at left margin of the paper to **indicate where the question corresponds to a new column in the OCR form**. E.g. questions 11, 21, 31, etc. (a column has 10 questions). Such markers can help you to detect if you missed a question in the previous 10 questions. You can safely ignore those markers if you are not interested in making use of that additional hint.

<img src="{{baseUrl}}/admin/images/columnMarker.png" /><br>

Some questions have tags e.g., the question below has a tag  **`JAVA`**. These **tags provide additional context about the question**. In the example below, the tag indicates that the code given in the question is Java code.

<img src="{{baseUrl}}/admin/images/contextTag.png" /><br>

**The exam paper is open-book**: you may bring any printed or written materials to the exam in hard copy format.
However, given the fast pace required by Part 1, you will not have time left to refer notes during that part of the exam.

{{ icon_tip }} **Mark the OCR form as you go**, rather than planning to transfer your answers to the OCR form near the end. %%Reason: Given there are 100 questions, it will be hard to estimate how much time you need to mass-transfer all answers to OCR forms.%%

{{ icon_tip }} **Write the answer in the exam paper as well** when marking it in the OCR form. %%Reason: It will reduce the chance of missing a question. Furthermore, in case you missed a question, it will help you correct the OCR form quickly.%%

{{ icon_tip }} We have tried to **avoid deliberately misleading/tricky questions**. If a question seems to take a very long time to figure out, you are probably over-thinking it.

<box type="success">

You will be given a practice exam paper to familiarize yourself with this slightly unusual exam format.
</box>


## Final Exam: Part 2 (Essay)

Yes, **you may use pencils** when answering part 2.



-->

{% endcall %}
