{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("moduleOverview") %} 
<div id="main">

<!-- =============================================================================== -->
<span tags="m--cs2103">
<big><p class="lead text-secondary">A balanced, iterative, and brown-field introduction to Software Engineering...</p></big>

<img src="{{baseUrl}}/images/growingPlant.png" width="700">

<p class="lead"><md>{{ module_pair }} is an introductory Software Engineering module. It has **a 50-50 balance of basic SE theory knowledge and practical skills** that you need to gain before industry internships or <tooltip content="e.g., CS3203, CS3216/7, CS3281&2, etc.">higher-level project modules</tooltip>. The module follows an <tooltip content="going through SE topics several times while increasing depth, as opposed to going through topics sequentially">**iterative approach**</tooltip> to covering topics. It is also one of the rare SE modules that includes a <tooltip content="i.e., working in an existing project">**brown-field** project</tooltip>, in addition to a <tooltip content="i.e., a project that is started from scratch">**green-field** project</tooltip>.</md></p>


* **On the theory side,** this module is supported by a customized online textbook [_Software Engineering for Self-Directed Learners_](../se-book-adapted/index.html), integrated into this module website.

* **The practice side,** you will first ramp up your technical skills by doing a small individual project (green-field) in which you will develop a personal assistant chatbot called [Duke](../se-book-adapted/projectDuke/index.html). Then, you will move to a team project (brown-field) in which you will take over an existing project [AddressBook-Level3 (AB3)](https://se-edu.github.io/addressbook-level3/) -- a relatively small yet non-trivial (6 KLoC) generic product -- and enhance it into a better product or evolve it into a different product.

<div id="meaning-of-iterative-topics">

<box>

****What does mean to 'follow an iterative approach in covering topics'?****

**It means, we cover a little bit of <tooltip content="i.e., requirements, design, testing, project management, ...">all SE aspects</tooltip> at first and then iteratively go deeper into them later**, revisiting each aspect many time over the course of the semester. In contrast, a _sequential_ approach would have covered one SE aspect before moving to the next (e.g., teach the _requirements_ aspect completely before moving to the _design_ aspect).

**The choice of which topics are covered each week is driven by the project** i.e., we give priority to topics that you'll need to apply soon in the project that you will be doing in parallel.

**This way of 'jumping around' topics feels chaotic but consider the benefits**:
* It allows you to start doing SE projects early, and iteratively too. That is, you can start with a small project from the very start and make it bigger progressively, learning from earlier mistakes, and getting multiple chances improve on previous attempts.
* Important SE aspects such as testing can be practiced from the very beginning. If we followed a sequential approach, you an only learn it near the end of the semester.
* Lower risk of missing out some SE aspects altogether. For example, suppose your schedule got heavier in the second half of the semester and you could barely follow the module during that half. You still go away with the basic knowledge of _all_ SE aspects rather than knowing some aspects fully and missing some other aspects altogether.

**To help you cope with the non-sequential progression of topics,** this module website contains two versions of the topics. In the [Schedule page](../schedule/index.html), you'll find the topics organized into the order we cover them in each week. In the [Textbook page](../se-book-adapted/index.html), you'll find the topics in their natural sequential order. This format is suitable for exam reference.
</box>

</div>

Given below is a summary of what the module covers and does not cover.

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
<panel src="appendixC-faq.md#admin-faq-tVsNonT" header="Admin {{ icon_embedding }} **FAQ: What are the differences between {{ module }} and {{ module }}T?**" class="embedding" minimized />
</span>
<!-- =============================================================================== -->
<span tags="m--cs2113">

<big><p class="lead text-secondary">An iterative introduction to Software Engineering...</p></big>

<img src="{{baseUrl}}/images/growingPlant.png" width="700">

<p class="lead"><md>{{ module_pair }} is an introductory Software Engineering module covering **a balance of basic SE theory and practical skills** needed to work in a project that has a software component. The module follows an <tooltip content="going through SE topics several times while increasing depth, as opposed to going through topics sequentially">**iterative approach**</tooltip> to covering topics. The module also introduces you to the Java programming language, the OOP paradigm, and some basic UML models.</md></p>

* **The theory side** of this module is supported by a customized online textbook [_Software Engineering for Self-Directed Learners_](../se-book-adapted/index.html), integrated into this module website.

* **On the practice side**, you will first ramp up your technical skills by doing a small individual project in which you will develop a personal assistant chatbot called [Duke](../se-book-adapted/projectDuke/index.html). Then, you will move to a team project in which you will build another small <tooltip content="Command Line Interface">CLI</tooltip> app while working as a team.

<include src="moduleOverview.md#meaning-of-iterative-topics" />

<panel src="appendixC-faq.md#admin-faq-tVsNonT" header="Admin {{ icon_embedding }} **FAQ: What are the differences between {{ module }} and {{ module }}T?**" class="embedding" minimized />
</span>
<!-- =============================================================================== -->
<span tags="m--tic4001">

<big><p class="lead text-secondary">A Software Engineering practicum module focusing on <tooltip content="projects starting from scratch, as opposed to projects starting from an existing code base">greenfield</tooltip> team projects...</p></big>

<img src="{{baseUrl}}/images/growingPlant.png" width="650">


<p class="lead"><md>{{ module }} builds on <tooltip content="Introduction to Software Engineering">TIC2002</tooltip> (and <tooltip content="Software Requirements Analysis and Design">TIC3001</tooltip>) to strengthen your practical SE skills. The focus will be on getting some hands on practice in various tools, techniques, and processes used in a systematic SE project.</md></p>

* **On the theory side, this module relies mostly on the theory covered in TIC2002, but it will also cover some new topics** to help you with the project. As before, this module is supported by a customized online textbook [_Software Engineering for Self-Directed Learners_](../se-book-adapted/index.html), integrated into this module website.

* **The practice side, you will first ramp up your technical skills by doing a small individual project** (green-field) in which you will develop a personal assistant chatbot called [Duke](../se-book-adapted/projectDuke/index.html). This project is similar to the project you did in TIC2002 but will be done faster and at a higher level of rigor.<br>
  **Then, you will move to a team project** (also greenfield) in which you will build another small <tooltip content="Command Line Interface">CLI</tooltip> app while working as a team.

**At the end of this module** you are expected to be ready for <tooltip content="Software Engineering Practicum II">TIC4002</tooltip> in which you'll tackle a <tooltip content="starting with an existing code base">brownfield</tooltip> team project somewhat larger than the project you did in this module.

</span>



</div>

{% endcall %}
