{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import show_faq with context %}

{% call show_admin_page("courseExpectations") %}
<div id="main">

<p class="lead">Here are some important things the course expects of you.</p>

<div tags="m--cs2103">

## Prior Knowledge: Java and OOP

This course requires you to write Java code almost every week, starting from the very first week. If your Java skills are rusty, please brush up on them.

</div>
<div id="use-of-ai">

## Use of AI

This course aims to get you started on using SE-related AI tools well. We want you to learn how to use those AI tools and use them in a way that enhances (not compromises) learning of basic SE skills.

When faced with a coding-related task (e.g., adding a feature), the level of AI use can vary as follows.

* No AI use. Hand-code everything. Use AI as a 'smart search engine' to ask general questions.{texts="['AI-1)', 'AI-2)', 'AI-3)', 'AI-4)', 'AI-5)', 'AI-6)']"}
* Hand-code first as if there is no AI. Ask AI to review. Refine based on AI's feedback.
* Hand-code minimal version, just a proof-of-concept. Get AI to strengthen it to a full-fledged version e.g., handle edge cases, add tests.
* Think of how you would do the task manually. Get AI to do it. Compare the solution you 'imagined' with the one AI produced.
* Get AI to do the task. Review it yourself fully, including the code, tests, behavior etc.
* Get AI to do the task, fully, including the review. Only review the outcome (e.g., the feature behavior).

Higher levels saves more time but can reduce learning.

Which level to use? Depends on how much you already know, and how much you want to learn.

{{ show_faq("useAiCode") }}

</div>

## Workload

As {{ marks_ca }}% of this course is based on CA (see <trigger trigger="click" for="modal:expectations-gradeBreakdown">grade breakdown</trigger>), it can appear to be _heavy_. However, **it is not expected that you will spend more time on this course than its <tooltip content="e.g., if this course is core for you, it should not take more time than other core courses at the same level in your program">peer courses</tooltip>**.
* Note that the **course contains more things than a typical student can do**, so that even the strongest students have enough opportunities to learn as much as they wish to.
* This means it is ==perfectly OK if you don't have time to learn everything the course offers==. Control your workload based on the time you spend on the course in a week, e.g., 1-1.5 days per week.
* We have provided a _topic levels_ system (explained below) to guide you when prioritizing what to do.

<modal large header="Grade breakdown" id="modal:expectations-gradeBreakdown">
  <pic eager src="gradeBreakdown.png" no-validation />
</modal>

<div id="topicLevels">

#### Topic Levels

<div class="indented">

<p class="lead"><md>We use a topic levels system to indicate the progression of course components. **Start with things that are rated level-1 and progress to topics at higher levels.** Things rated level-4 are optional.</md></p>

**Levels for lesson topics** (and textbook sections):

* **Level-1 topics** {{ one_star }} are essential to keep up with the course. We recommend that you ==learn these topics if you want to pass the course== (i.e., up to a **C** grade).
* **Level-2 topics** {{ two_stars }} can get you up to a **B+**.
* **Level-3 topics** {{ three_stars }} can get you up to an **A**.
* **Level-4 topics** {{ four_stars }} can push you beyond the limits of the course and help you reach a level above those who limit themselves to the course topics. They ==are not <popover content="_examinable_ here means _can affect the grade_ during evaluation of various components, not necessarily limited to the final exam (if any)">examinable</popover>==.

<span tags="m--cs2103 m--tic2002">

* Topics marked with two {{ icon_prereq }} icons e.g., {{ prereq_one_star }},{{ prereq_two_stars }},{{ prereq_three_stars }} are relevant topics you are expected to have learned in prerequisite courses. They are given for reference, but ==are examinable==. The number of {{ star }} indicates the progression of prerequisite topics, similar to the topic levels system above, i.e., level-1 prerequisite topics are the most basic and the most important. Level-4 prerequisite topics can be ignored without affecting GPA.
</span>

**Topic levels for other things**, e.g., admin info sections:

* The course uses a similar topic levels system to indicate the importance of other info in this website. i.e., information rated as level-1 is the most essential. ==Info rated level-4 is optional and can be ignored== without affecting your ability to follow the course.

</div>
<div tags="m--cs2103">

#### Rewards for exceeding expectations

This course deliberately avoids giving extra credit for exceeding expectations, in order to keep the workload manageable (of course, doing more will have its own rewards in terms of learning).
</div>
</div>

</div>

{% endcall %}
