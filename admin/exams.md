{% macro show_main_text() %}
<div id="main">

There is no midterm.

The final exam has two parts: 
* Part 1: MCQ questions (1 hour, 20 marks) 
* Part 2: Essay questions (1 hour, 20 marks)

Both papers will be given to you at the start but you need to **answer Part 1 first** (i.e. MCQ paper). It will be **collected 1 hour after the exam start time** (even if arrived late for the exam). You are free to start part 2 early if you finish Part 1 early.

## Final Exam: Part 1 (MCQ)

Each MCQ question gives you a statement to evaluate. 

<tip-box> 

{{ icon_example }} An example statement

>Testing is a Q&A activity

</tip-box>


Unless stated otherwise, the meaning of answer options are<br>
**A**: Agree. If the question has multiple statements, ++agree with all of them++.<br>
**B**: Disagree. If the question has multiple statements, ++disagree with at least one of them++<br>
**C**, **D**, **E**: Not used

Number of questions: 100

<div class="full-mode">

Note that you have **slightly more than ½ minute for each question**, which means you need to go through the questions fairly quickly.
</div>

Given the fast pace required by the paper, to be fair to all students, **you will not be allowed to clarify doubts about questions** (in Part 1) by talking to invigilators. 
* If a question is not clear, you can circle the question number in the question paper and write your doubt in the question paper, near that question.
* If your doubt is justified %%(e.g. there is a typo in the question)%% or if many students found the question to be unclear, the examiner may decide to omit that question from grading.

**Questions in Part 1 are confidential.** You are not allowed to reveal Part 1 content to anyone after the exam. All pages of the assessment paper are to be returned at the end of the exam.

<div class="full-mode">

You will be given OCR forms %%(i.e., bubble sheets)%% to indicate your answers for Part 1. As each OCR form can accommodate only 50 answers, you will be given 2 OCR forms. **Indicate your student number in both OCR forms**.
</div>

To save space, we use the following notation in MCQ question.
 **[++x++ | y | ++z++] means ‘x and z, but not y’**

<tip-box> 

{{ icon_example }} SE is [boring | ++useful++ | ++fun++] means _SE is not boring_ AND _SE is useful_ AND _SE is fun_.

{{ icon_example }} Consider the following statement:

* IDEs can help with [++writing++ | debugging | ++testing++] code.

The correct response for it is `Disagree` because IDEs can help with all three of the given options, not just writing and testing.

</tip-box>

Some questions will use ++underlines++ or ==highlighting== to draw your attention to a specific part of the question. That is because those parts are highly relevant to the answer and we don’t want you to miss the relevance of that part.

<tip-box> 

{{ icon_example }} Consider the statement below:
  
> Technique ABC ++can++ be used to generate more test cases. 

The word ++can++ is underlined because the decision you need to make is whether the ABC _can or cannot_ be used to generate more test cases; the decision is not whether ABC can be used to generate _more or better_ test cases.

</tip-box>

Markers such as the one given below appears at left margin of the paper to **indicate where the question corresponds to a new column in the OCR form**. E.g. questions 11, 21, 31, etc. (a column has 10 questions). Such markers can help you to detect if you missed a question in the previous 10 questions. You can safely ignore those markers if you are not interested in making use of that additional hint.

<img src="{{baseUrl}}/admin/images/columnMarker.png" /><br>

Some questions have tags e.g., the question below has a tag  **`JAVA`**. These **tags provide additional context about the question**. In the example below, the tag indicates that the code given in the question is Java code.

<img src="{{baseUrl}}/admin/images/contextTag.png" /><br>

**The exam paper is open-book**: you may bring any printed or written materials to the exam in hard copy format.
However, given the fast pace required by Part 1, you will not have time left to refer notes during that part of the exam. 

:bulb: **Mark the OCR form as you go**, rather than planning to transfer your answers to the OCR form near the end. %%&nbsp;Reason: Given there are 100 questions, it will be hard to estimate how much time you need to mass-transfer all answers to OCR forms.%%

:bulb: **Write the answer in the exam paper as well** when marking it in the OCR form. %%&nbsp;Reason: It will reduce the chance of missing a question. Furthermore, in case you missed a question, it will help you correct the OCR form quickly.%%

:bulb: We have tried to **avoid deliberately misleading/tricky questions**. If a question seems to take a very long time to figure out, you are probably over-thinking it.

<box type="success">

You will be given a practice exam paper to familiarize yourself with this slightly unusual exam format.
</box>


## Final Exam: Part 2 (Essay)

Unlike in part 1, **you can ask invigilators for clarifications** if you found a question to be unclear in part 2.

Yes, **you may use pencils** when answering part 2.

</div>


{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("exams", show_main_text) }}