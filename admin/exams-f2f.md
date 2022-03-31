
<p class="lead">There is no midterm exam. Information about the final exam is given below.</p>

{% if (current_week | int) < 11 %}
<box type="important">

Instructions below are from the previous semester. Will be updated closer to the exam.
</box>
{% endif %}


1. The final exam will be **as per the normal exam schedule** (you can check exam time from [NUSMods](https://nusmods.com/modules/)), and will count for **{{ marks_exam }}% of the final grade**.
1. The exam will be done **face-to-face, but using LumiNUS quiz**. SCALE is not allowing remote exam this semester except in some special cases.
1. You will ==need to **bring your own laptop**==, which can connect to the NUS wifi network.
1. ==**Recording of your PC screen** is not required.==
1. **Soft copies of notes: only PDF format is allowed.** Other formats (e.g., MS Word, .txt, html) are not allowed. No limitation on what the PDF file contains or the number of PDF files to be used.<br>
  You may use any hard copies or written materials too.
1. **The Browser should only be used to access LumiNUS and the module website{% if not tee3201 %} (including relevant se-education.org pages %%e.g., Java coding standard%%){% endif %}.** ==Accessing other websites is not allowed==.<br>
1. **The quiz will not appear on LumiNUS until a few minutes before we release the password**. Wait until we announce that the quiz is available to see.
1. **If you have a doubt/query about a question**, or want to make an assumption about a question, please write it down in the 'justification' text box. ==Do not try to communicate those with the invigilator during the exam.== We'll take your doubt/query/assumption into account when grading. For example, if many had queries about a specific question, we can conclude that the question is unclear and omit it from grading.
1. **If your computer crashed/restarted** during the exam, try to get it up again and resume the exam. LumiNUS will allow you to resume from where you stopped earlier. However, note that there is a deadline to finish the quiz and you will overrun that deadline if you lose more than 5 minutes due to the computer outage.
1. **Bring your computer fully charged**, although some charging points will be available at the exam venue.

## Format

* The exam will be divided into 2 parts.

### Final exam - part 1

* A LumiNUS quiz containing 16 MCQ questions. All questions are estimated to be equal size/difficulty.
* You only need to answer 15 questions correctly to get full marks. The extra question is there to cushion you against careless mistakes or misinterpreting a question.
* Questions will appear in random order.
* You will not be able to go back to previous questions.<br>
  %%Reasons:<br>
  1\. to minimize opportunities for collusion<br>
  2\. not unreasonable for the materials tested and the proficiency level expected -- i.e., when using this knowledge in a real life SE project discussion, it will be rare for you to go back to revise what you said earlier in the discussion%%
* Duration: **45 minutes** (recommended: allocate 2.5 minutes per question, which gives you a 5 minutes buffer)
* You are required to give a justification/rationale for your answer. ==The question will specify what should be included in the justification. **Answers without the correct justification may not earn full marks.**== However, we'll give full marks up to two correct answers (per 16 questions) with missing/incorrect justifications %%(to cater for cases where you accidentally proceeded to the next question before adding the justification)%%.
* Here is an example question. The answer is `a` and the justification can be `OOP is only one of the choices for an SE project`.
<div class="indented-level2">

<panel haader="A sample question" expanded >

Choose the incorrect statement.

<span class="text-info">[Justification: why is it incorrect?]</span>
- ( ) a. Software engineering projects always use OOP.
- ( ) b. Some software engineering projects can be large and complex.
- ( ) c. Some software engineering projects can go on for many years.
- ( ) d. Software projects can involve people who are not software engineers.

</panel>
<p/>
</div>


### Final exam - part 2

* Similar to part 1 (e.g., 16 questions, same length).


## Exam briefing, mock exam, practice exam paper

* There will be an exam briefing in the penultimate lecture. It will include a minimal mock exam, just to help you understand the structure.
* You will be given a practice exam paper (at least half the size of the full paper) to help you practice timing. That practice paper will be released at least one week before the exam.
