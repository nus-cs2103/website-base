{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import show_faq with context %}

{% call show_admin_page("courseOverview") %}
<div id="main">

<!-- =============================================================================== -->
<div tags="m--cs2103">
<p class="lead text-secondary">++A balanced, iterative, and brownfield introduction to Software Engineering...++</p>

<pic eager src="{{baseUrl}}/images/growingPlant.png" width="700"></pic>

<p class="lead"><md>{{ course_pair }} is an introductory Software Engineering course. It has **a 50-50 balance of basic SE theory knowledge and practical skills** that you need to gain before industry internships or <tooltip content="e.g., CS3203, CS3216/7, CS3281&2, etc.">higher-level project courses</tooltip>. The course follows an <tooltip content="going through SE topics several times while increasing depth, as opposed to going through topics sequentially">**iterative approach**</tooltip> to covering topics. It is also one of the rare SE courses that includes a <tooltip content="i.e., working in an existing project">**brownfield** project</tooltip>, in addition to a <tooltip content="i.e., a project that is started from scratch">**greenfield** project</tooltip>.</md></p>


* **On the theory side,** this course is supported by a customized online textbook [_Software Engineering for Self-Directed Learners_](../se-book-adapted/index.html), integrated into this course website.

* **The practice side,** you will first ramp up your technical skills by doing a small individual project (greenfield) in which you will develop a personal assistant chatbot called [Duke](../se-book-adapted/projectDuke/index.html). Then, you will move to a team project (brownfield) in which you will take over an existing project [AddressBook-Level3 (AB3)](https://se-edu.github.io/addressbook-level3/) -- a relatively small yet non-trivial (6 <tooltip content="LoC = Lines of Code">KLoC</tooltip>) generic product -- and enhance it into a better product or evolve it in a direction that you choose.

<div id="meaning-of-iterative-topics">

<box>

****What does mean to 'follow an iterative approach in covering topics'?****

**It means, we cover a little bit of <tooltip content="i.e., requirements, design, testing, project management, ...">all SE aspects</tooltip> at first and then iteratively go deeper into them later**, revisiting each aspect many times over the course of the semester. In contrast, a _sequential_ approach would have covered one SE aspect before moving to the next (e.g., teach the _requirements_ aspect completely before moving to the _design_ aspect).<br>

**In each week, we cover topics that are most relevant to the project tasks** that you are expected to do around that time.

**This way of 'jumping around' topics feels chaotic but consider the benefits**:
* It allows you to start doing SE projects early, and do it iteratively too. That is, you can start with a small project from the very start and make it bigger progressively, learning from earlier mistakes, and getting multiple chances to improve on previous attempts.
* Important SE aspects such as testing can be practiced from the very beginning. If we followed a sequential approach, you can only learn it near the end of the semester.
* It lowers the risk of missing out some SE aspects altogether. For example, suppose your schedule got heavier in the second half of the semester, and you could barely keep up with the course during that half. You still go away with the basic knowledge of _all_ SE aspects rather than knowing some aspects deeply while missing some other aspects altogether.

**To help you cope with the non-sequential progression of topics,** this course website contains two versions of the topics.

1. In the [Schedule page](../schedule/index.html), you'll find the topics organized into the order we cover them in each week.
1. In the [Textbook page](../se-book-adapted/index.html), you'll find the topics in their natural sequential order. This format is suitable for exam reference.
</box>

</div>

Given below is a summary of what the course covers and does not cover.

Topic | {{ icon_tick_green }} Covered | {{ icon_x_red }} Not covered
------|---------|------------
Java | Used heavily, but not taught | syntax %%(reason: expected prerequisite knowledge)%%
OOP | Used in a non-trivial project, <tooltip content="e.g., Single Responsibility Principle, Open-Closed Principle">intermediate OOP principles</tooltip> | basics %%(reason: expected prerequisite knowledge)%%
SE tools/practices | <tooltip content="e.g., revision control, continuous integration, practices, test automation, code reviews, pull requests">those typically used in a mature, high-rigor SE project</tooltip> | those specific to start-ups</md></td>
Modeling | <tooltip content="e.g., class diagrams, sequence diagrams, activity diagrams">Some UML notations</tooltip> (sufficient to be able to describe SE artifacts using models, such as seen in [this Developer Guide of AB3](https://se-edu.github.io/addressbook-level3/DeveloperGuide.html#design)) | intensive <tooltip content="creating detailed UML models before starting to code">upfront design modeling</tooltip>
Requirements | <tooltip content="e.g., user stories, use cases">Some lightweight techniques</tooltip> to gather and document project requirements | rapid prototyping, heavy UI design, designing a product from scratch
Documentation | Documentation targeting end users ([example](https://se-edu.github.io/addressbook-level3/UserGuide.html)) as well as those targeting developers ([example](https://se-edu.github.io/addressbook-level3/DeveloperGuide.html)) | Marketing materials
Project Management | Iterative delivery of a product, working collaboratively with team members, on-site as well as remotely | Setting up project infrastructure from scratch
Testing | <tooltip content="e.g., automated unit/integration/system testing">basic developer testing</tooltip> and <tooltip content="e.g., acceptance testing">user testing</tooltip> | <tooltip content="e.g., security testing, performance testing, usability testing">testing for non-functional aspects</tooltip>
Applications domains | Cross-platform desktop applications | Web programming, Mobile programming, Database programming

<br>
{{ show_faq("tVsNonT") }}
</div>
<!-- =============================================================================== -->
<div tags="m--cs2113">

<p class="lead text-secondary">++An iterative introduction to Software Engineering...++</p>

<pic eager src="{{baseUrl}}/images/growingPlant.png" width="700"></pic>

<p class="lead"><md>{{ course_pair }} is an introductory Software Engineering course covering **a balance of basic SE theory and practical skills** needed to work in a project that has a software component. The course follows an <tooltip content="going through SE topics several times while increasing depth, as opposed to going through topics sequentially">**iterative approach**</tooltip> to covering topics. The course also introduces you to the Java programming language, the OOP paradigm, and some basic UML models.</md></p>

* **The theory side** of this course is supported by a customized online textbook [_Software Engineering for Self-Directed Learners_](../se-book-adapted/index.html), integrated into this course website.

* **On the practice side**, you will first ramp up your technical skills by doing a small individual project in which you will develop a personal assistant chatbot called [Duke](../se-book-adapted/projectDuke/index.html). Then, you will move to a team project in which you will build another small <tooltip content="Command Line Interface">CLI</tooltip> app while working as a team.

<include src="courseOverview.md#meaning-of-iterative-topics" />

</div>
<!-- =============================================================================== -->

</div>

{% endcall %}
