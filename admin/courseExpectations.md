{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("courseExpectations") %}
<div id="main">

<p class="lead">Here are some important expectations of the course from you.</p>

<div tags="m--cs2103">

## Prior Knowledge: Java and OOP

This course requires you to write Java code almost every week, starting from the very first week. If your Java skills are rusty, do brush up your Java programming skills.

In particular, you may want to **have a look at the new Java features** such as _streams_, _lambdas_, _Optionals_, that may not have been covered in previous Java courses.
</div>

## Workload

As {{ marks_ca }}% of this course is based on CA (see <trigger trigger="click" for="modal:expectations-gradeBreakdown">grade breakdown</trigger>), it can appear to be _heavy_. However, **it is not expected that you will spend more time on this course than its <tooltip content="e.g., if this course is core for you, it should not take more time than other core courses at the same level in your program">peer courses</tooltip>**.
* Note that the **course contains more things than a typical students can do**, in order to provide enough things for even the strongest students to learn as much as they wish to.
* This means it is ==perfectly OK if you don't have time to learn everything the course offers==. Control your workload based on time you spend for the course in a week e.g., 1-1.5 days per week.
* We have provided a _topic levels_ (explained below) to guide you when prioritizing which things to do.

<modal large header="Grade breakdown" id="modal:expectations-gradeBreakdown">
  <pic eager src="gradeBreakdown.png" no-validation />
</modal>

<div id="topicLevels">

#### Topic Levels

<div class="indented">

<p class="lead"><md>We use a topic levels system to indicate the progression of course components. **Start with things that are rated level-1 and progress to topics at higher levels.** Things rated level-4 are optional.</md></p>

**Levels for lesson topics** (and textbook sections):

* **Level-1 topics** {{ one_star }} are essential to keep up with the course. We recommend you to ==learn these topics if you want to pass the course== (i.e., up to a **C** grade).
* **Level-2 topics** {{ two_stars }} can get you up to a **B+**.
* **Level-3 topics** {{ three_stars }} can get you up to an **A**.
* **Level-4 topics** {{ four_stars }} can push you beyond the limits of the course, and help you get into a level above those who merely limit themselves to the topics of the course. They ==are not <popover content="_examinable_ here means _can affect the grade_ during evaluation of various components, not necessarily limited to the final exam (if any)">examinable</popover>==.

<span tags="m--cs2103 m--tic2002">

* Topics marked with two {{ icon_prereq }} icons e.g., {{ prereq_one_star }},{{ prereq_two_stars }},{{ prereq_three_stars }} are relevant topics you are expected to have learned in prerequisite courses. They are given for reference, but ==are examinable==. The number of {{ star }} indicates the progression of prerequisite topics, similar to the topic levels system above i.e., level-1 prerequisite topics are the most basic and the most important. level-4 prerequisite topics can be ignored without affecting GPA.
</span>

**Topic levels for other things** e.g., admin info sections:

* The course uses a similar topic levels system to indicate the importance of other info in this website. i.e., information rated as level-1 are the most essential. ==Info rated level-4 are non-essential and can be ignored== without affecting your ability to follow the course.

</div>
<div tags="m--cs2103">

#### Rewards for exceeding expectations

This course deliberately avoids giving extra credit for exceeding the expected bars, in order to keep the workload manageable (of course, doing more will have their own rewards in terms of learning).
</div>
</div>

</div>

{% endcall %}
