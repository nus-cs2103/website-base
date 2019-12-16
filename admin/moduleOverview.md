{% macro show_main_text() %} 
<div id="main">

<big><p class="lead text-secondary">A balanced, iterative, and brown-field introduction to Software Engineering...</p></big>

<img src="{{baseUrl}}/images/growingPlant.png" width="700">

<p class="lead"><md>{{ module_pair }} is an introductory Software Engineering module. It has **a 50-50 balance of basic SE theory knowledge and practical skills** that you need to gain before industry internships or <tooltip content="e.g., CS3203, CS3216/7, CS3281&2, etc.">higher-level project modules</tooltip>. The module follows an <tooltip content="going through SE topics several times while increasing depth, as opposed to going through topics sequentially">**iterative approach**</tooltip> to covering topics. It is also one of the rare SE modules that includes a <tooltip content="i.e., working in an existing project">**brown-field** project</tooltip>, in addition to a <tooltip content="i.e., a project that is started from scratch">**green-field** project</tooltip>.</md></p>

* **On the theory side,** this module is supported by a customized online textbook [_Software Engineering for Self-Directed Learners_](../se-book-adapted/index.html), integrated into this module website.

* **The practice side,** you will first ramp up your technical skills by doing a small individual project (green-field) in which you will develop a personal assistant chatbot called [Duke](../se-book-adapted/projectDuke/index.html). Then, you will move to a team project (brown-field) in which you will take over an existing project [AddressBook-Level3 (AB3)](https://se-edu.github.io/addressbook-level3/) -- a relatively small yet non-trivial (6 KLoC) generic product -- and enhance it into a better product or evolve it into a different product.

Given below is a summary of what the module covers and does not cover.

Topic | {{ icon_tick_green }} Covered | {{ icon_x_red }} Not covered
------|---------|------------
Java | Used heavily, but not taught | syntax %%(reason: expected prerequisite knowledge)%%
OOP | Used in a non-trivial project, <tooltip content="e.g., Single Responsibility Principle, Open-Closed Principle">intermediate OOP principles</tooltip> | basics %%(reason: expected prerequisite knowledge)%%
SE tools/practices | <tooltip content="e.g., revision control, continuous integration, practices, test automation, code reviews, pull requests">those typically used in a mature, high-rigor SE project</tooltip> | those specific to start-ups</md></td>
Modeling | <tooltip content="e.g., class diagrams, sequence diagrams, activity diagrams">Some UML notations</tooltip> (sufficient to be able to describe SE artifacts using models, such as seen in [this Developer Guide of AB3](https://se-edu.github.io/addressbook-level3/DeveloperGuide.html#design)) | intensive <tooltip content="creating detailed UML models before strating to code">upfront design modeling</tooltip>
Requirements | <tooltip content="e.g., user stories, use cases">Some lightweight techniques</tooltip> to gather and document project requirements | rapid prototyping, heavy UI design, designing a product from scratch
Documentation | Documentation targeting end users ([example](https://se-edu.github.io/addressbook-level3/UserGuide.html)) as well as those targeting developers ([example](https://se-edu.github.io/addressbook-level3/DeveloperGuide.html)) | Marketing materials
Project Management | Iterative delivery of a product, working collaboratively with team members, on-site as well as remotely | Setting up project infrastructure from scratch
Testing | <tooltip content="e.g., automated unit/integration/system testing">basic developer testing</tooltip> and <tooltip content="e.g., acceptance testing">user testing</tooltip> | <tooltip content="e.g., security testing, performance testing, usability testing">testing for non-functional aspects</tooltip>
Applications domains | Cross-platform desktop applications | Web programming, Mobile programming, Database programming

<br>

<panel src="appendixC-faq.md#admin-faq-tVsNonT" header="Admin {{ icon_embedding }} **FAQ: What are the differences between {{ module }} and {{ module }}T?**" class="embedding" minimized />

</div>
{% endmacro %} 


{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("moduleOverview", show_main_text) }}