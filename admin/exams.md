{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("exams") %}
<div id="main">


## Final Exam

<box type="important">

Instructions below are from the previous semester. Will be updated closer to the exam.
</box>


* The final exam will be as per the normal exam schedule, and will count for {{ marks_exam }}% of the final grade.
* The exam will be done online. Tools used: LumiNUS, Zoom, Microsoft Teams.

### Early preparations

* **Set up Zoom**: Follow the [Zoom exam instructions provided by NUS](https://wiki.nus.edu.sg/display/THES/Proctoring+with+Zoom) (note the requirement for ==SSO login==).
  * **Update the name of your Zoom profile to match the exact name on your student card, ==including whether the family name is give first or last==** (reason: we need to manually locate your name in the attendance list, which is sorted by your name in LumiNUS). You will not be admitted to the Zoom meeting if you do not comply with the requirement.
  * **Note the requirements for camera placement**: Your Zoom video feed need to capture your upper body and the work area, including the computer screen (==as explained in [this example](https://www.youtube.com/watch?v=BoeXRLfpYv4)==). That means **the built-in camera of your computer is not suitable** for this purpose. Use either a separate web cam (attached to your Computer) or use Zoom through your smart phone. If neither of those options are available to you, let the prof know ASAP (deadline: April 24).

<div class="indented-level2">

<box type="important">

You will not be allowed into the Zoom meeting unless your Zoom name complies with the above requirement.<br>
Your exam submission will not be accepted if your Zoom video feed does not comply with the above requirement.
</box>
<box type="warning">

As per NUS requirements, your Zoom video feed is recorded by us and will be shared with NUS administration. If you do not consent to that, please let us know ASAP (deadline: April 24) so that we can put you in touch with the NUS administration to sort it out.
</box>
</div>

* **Set up MS-Teams**: Follow the [_Microsoft Teams_ instructions provided by NUS](https://wiki.nus.edu.sg/display/THES/Before+exams+-+Install+and+log+in+to+Microsoft+Teams). We'll be using MS-Teams as a backup in case of Zoom fails.


### 30 minutes before the exam

* Aim to join the Zoom waiting room around 12.30pm.
* Ensure your computer and the phone (if applicable) are charged and within reach of a power supply.
* In your computer, close all other apps and browser tabs other than the ones permitted to be use for the exam. Remember to exit other background apps that starts automatically such as telegram.
* Launch MS-Teams, login to it, and close the app without exiting (which makes it run in the background).
* Login to LumiNUS. The password to open the quiz will be broadcast via Zoom (audio announcement plus chat message) by the invigilator later.
* If you are using Zoom from your phone, remember to disable the auto-sleep/lock feature so that the phone doesn't go to sleep in the middle of the exam.
* Launch Zoom, login, ensure profile name and camera complies with our requirements, and join the meeting. Wait for the invigilator to take you into the meeting.
* **Do not use more than one Zoom device at a time.**
  * If it is inconvenient to use the Zoom device for PM'ing the invigilator %%(e.g., if you are using Zoom through a smart phone mounted on a stand)%%, use MS-Teams (via your computer) to PM the invigilator.
  * **Exception: if you use a phone as your primary Zoom device but it not convenient to use it for audio** %%(e.g., its speaker volume not high enough)%%,<br>
    1. Get our permission to use the PC as a second Zoom device.
    1. Install Zoom in the PC.
    1. Use the PC for audio/chat only (i.e., switch off the video) and the phone for video only.
    1. Name your Zoom profile name in the PC as `[PC] Your Name as in Student Card` e.g., `[PC] John Doe`
* Once you are inside the Zoom meeting, wait patiently until all students have been admitted and the exam is ready to start. **This wait could be as long as 30-45 minutes.**
* Note that ==the quiz will not appear on LumiNUS until a few minutes before we release the password==.

### During the exam

* **Keep both the video and speaker switched-on (but microphone muted)** in your Zoom during the entire exam.
* Do not use MS-Teams during the exam unless the invigilator uses to contact you, you need to contact the invigilator, or you need to contact CIT for tech help.
* **Stay in the video frame for the entire exam duration**, except during the toilet break.
* **Do not to use virtual backgrounds in Zoom**. Do not use pre-recorded videos as your video feed.
* As the exam is open-book, you can refer to any printed/written materials or use the computer to read any PDF/word documents that are in your computer. You may also access the online version of the textbook in the module website but ==strongly encouraged to use the PDF or printed version of the textbook instead==.<br>
  **Do not visit any other websites, use any other apps, or online search engines during the exam.**
* **Remain in the video frame until the invigilator ends the exam**, even after you have submitted the quiz. Do not use the computer or other communication devices (not even Kindle) during that period (suggestion: have something in hard-copy form to ready to read during this time e.g., printed lecture notes of another module).
* **Do not communicate with any person other than the invigilator** during the exam, as per normal exam rules.
* **When the invigilator asks you to do a _face check_**, turn your face towards the camera, move closer to the camera, remove face mask (if any), and hold the pose until the invigilator tells you to go back to your working position.

### Troubleshooting exam problems

* **If you have a doubt/query about a question**, or want to make an assumption about a question, please write it down in the 'justification' text box. ==Do not try to communicate those with the invigilator during the exam.== We'll take your doubt/query/assumption into account when grading. For example, if many had queries about a specific question, we can conclude that the question is unclear and omit it from grading.
* **If you encounter a serious problem** that prevents you from proceeding with the exam (e.g., the password to open the quiz doesn't work), contact the invigilator using Zoom chat or MS-Teams.
* **If your computer crashed/restarted** during the exam, try to get it up again and resume the exam. LumiNUS will allow you to resume from where you stopped earlier. However, note that there is a deadline to finish the quiz and you will overrun that deadline if you lose more than 5 minutes due to the computer outage.


### Format

* The exam will be given as quizzes in LumiNUS.<br>
  For the ease of administration, the exam is split into two equal size quizzes: part 1, part 2.<br>
* Each quiz,
  * consists of 15 MCQ questions (plus one easy _bonus question_ and a dummy question to collect comments)
  * is to be done in 30+5 minutes (if you spend around 2 minutes per question, you'll have a 5 minutes buffer)
* All 30 normal questions have the same the weight and each question is expected to take a similar amount of time.
* The questions will be presented in random order.
* You are not allowed to go back to previous questions.
* You are required to give a justification for your answer. The question will specify what should be included in the justification.<br>
  ==**Answers without the correct justification will not earn full marks.**== However, we'll give full marks up to two correct answers (per 15 questions) that do not have justifications %%(to cater for cases where you accidentally proceeded to the next question before adding the justification)%%.
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

<div class="full-mode">

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
