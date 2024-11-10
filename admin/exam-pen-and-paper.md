There is no midterm. The info given below are for the final exam.

{% if (current_week | int) < 11 %}
<box type="important">

Instructions below are from the previous semester. Will be updated closer to the exam.
</box>
{% endif %}

**Mode:** F2F pen-and-paper mode (not digital)

**Weightage:** {{ marks_exam }}% of the final grade

**Schedule/venue:** The final exam will be as per the normal exam schedule, which will be sent to you by the Registrar's Office (or you can find via EduRec -> Academics -> Exams -> View exam schedule). You can find the date/time from [NUSMODS](https://nusmods.com/modules/{{ course }}).

**Structure:**

* The exam has two parts:
  * Part 1: MCQ questions (1 hour, 30 marks)
  * Part 2: Essay questions (1 hour, 30 marks)
* Both papers will be given to you at the start, but you need to **answer Part 1 first** (i.e. MCQ paper). It will be **collected 1 hour after the exam start time** (even if you arrived late for the exam). You are free to start part 2 early if you finish Part 1 early.

{{ icon_info }} **The exam is open-book**: you may bring any printed or written materials to the exam in hard copy format. But no devices are allowed.

{{ icon_important_big_red }} **Questions papers are confidential.** You are not allowed to reveal their content to anyone after the exam. All pages of the exam paper are to be returned at the end of the exam.

<box type="success" seamless>

You will be given a practice exam paper at least one week before the final exam.<br>
You can also use past weekly Canvas quizzes to self-test your knowledge (they have been reopened, and set to show the answer immediately).<br>
However, past exam papers will not be made available.
</box>

### Final Exam: Part 1 (MCQ)

**Number of questions: 50**

Each MCQ question gives you one or more statement to evaluate.<br>
Unless stated otherwise, the meaning of answer options are<br>
`A`: Agree. If the question has multiple statements, !!agree with all of them!!.<br>
`B`: Disagree. If the question has multiple statements, !!disagree with at least one of them!!<br>

<box>

{{ icon_example }} Here is an example:

>**Q23:** {{ "Python" if tee3201 else "Java" }} can be used to write OOP code.

The answer should be `A` %%(i.e., Agree)%%.
</box>
<box>

{{ icon_example }} Here is another example:

>**Q24:** Testing is a QA activity. It is done by testers only.

As the first statement is true but the second is not, the answer should be `B` %%(i.e., Disagree)%%.
</box>

A small number of questions will provide custom options to choose from.

<box>

{{ icon_example }} Here is one more example that has specific options to choose from, rather than the default Agree/Disagree.

>**Q25:** The course project was done using the _____ paradigm.<br>
>[A] Procedural&nbsp;&nbsp;&nbsp;[B] Functional&nbsp;&nbsp;&nbsp; [C] OOP

Answer: `C`
</box>

You will be given OCR forms %%(i.e., bubble sheets)%% to indicate your answers for Part 1.

**You have slightly more than 1 minute for each question**, which means you need to go through the questions fairly quickly. You might not have a lot of time left to refer notes frequently during this part of the exam (i.e., you need to be fairly familiar with the content, needing to refer to notes only occasionally).<br>
 That said, based on our past observations, almost all students are able to finish this part of the exam withing the given time fairly comfortably.

{{ icon_tip }} **Mark the OCR form as you go**, rather than planning to transfer your answers to the OCR form near the end. %%Reason: Given there are 50 questions, it will be hard to estimate how much time you need to mass-transfer all answers to OCR forms.%%

{{ icon_tip }} **Write the answer in the exam paper as well** when marking it in the OCR form. %%Reason: It will reduce the chance of missing a question. Furthermore, in case you missed a question, it will help you correct the OCR form quickly.%%

{{ icon_tip }} **We have tried to avoid deliberately misleading/tricky questions**. If a question seems to take a very long time to figure out, you are probably over-thinking it.

<box type="important" light>

**Invigilators will not answer queries about the questions in the exam paper part 1** (but _will_ answer queries related to exam administration). Reason: Given the fast pace required by this part of the exam, it may be difficult to reach exam takers quickly enough, or to ensure all students receive the same level of access to the invigilator during the exam.
* If you have a doubt/query about a question, or would like to make an assumption about a question, or would like to report a potential error in the exam paper, **write down your doubt/query/assumption in the space provided for it at the end of the exam paper**.
* Those doubts/queries/assumptions (if justified) will be taken into account when grading.
</box>

## Final Exam: Part 2 (Essay)

* Some examples of the nature of questions you can expect:
  * Draw UML diagrams to match the given code/description
  * Specify requirements for a given project using various formats covered in the course
  * {% if tic2002 %}Review a given piece of Java code to identify areas to improve (e.g., detect coding standard violations){% else %}Design test cases to test a given function.
* **Yes, you may use pencils** when answering part 2.{% endif %}
* If you have any queries during this part of the exam, you may ask the invigilator for clarifications.
