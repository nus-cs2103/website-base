<frontmatter>
title: "Admin: Preliminaries"
footer: footer.md
siteNav: adminSiteNav.md
</frontmatter>

<link rel="stylesheet" href="../css/main.css">
<link rel="stylesheet" href="../css/admin.css">

<include src="../common/header.md" />

<div class="website-content" id="main">

# {{ module }}/T at a Glance

{{ module }}/T is an introductory Software Engineering module. It covers basic SE theory and practices that a student needs to know before she goes out to SE internships in the industry or take <tooltip content="e.g., CS3203, CS3216/7, CS3281&2, etc.">level 3 project modules</tooltip>.

This module has a significant team project, to be done in teams of 5. In the project students are expected to take over an existing project [AddressBook-Level4](https://se-edu.github.io/addressbook-level4/) which is relatively small yet non-trivial (10 KLoC) generic product that the students are expected to take over and enhance into a better product or evolve into a different product. To help students ramp up their skills to a level that can tackle an existing product of 10 KLoC size, the module take them through a series of projects of increasingly bigger slze, from AddressBook-Level1 (1 KLoC) to AddressBook-Level3(4 KLoC).

The module is supported by a customized online text book [_Software Engineering for Self-Directed Learners_](http://127.0.0.1:8080/website-base/se-book-adapted/index.html), integrated into this module website.

Some of the important things student learn in this module are:
* Typical SE tools (e.g., revision control, continuous integration), practices (test automation, code reviews, OSS practices), and workflows (e.g., forking workflow) used in a mature, high-rigor SE project
* Some lightweight techniques to gather and document project requirements
* Some UML notations, sufficient to be able to describe SE artifacts using models
* Using OOP (and functional programming, to a lesser extent) in a non-trivial project
* Documentation targeting end users as well as those targeting developers
* Iterative delivery of a product
* Working collaboratively with team members
* To contribute to an existing product

Some of the things NOT covered by the module are
* Expected to have been covered by upstream modules: Java programming basics, OOP basics
* Expected to be covered by downstream modules in future: Web programming, Mobile programming, Database programming, Setting up project infrastructure from scratch, building a product from scratch
 
<panel header="%%Admin {{ icon_embedding }}%% **FAQ: Where is everything?**" type="seamless" minimized>
  <include src="appendixC-faq.md#admin-faq-whereIsEverything" />
</panel>
<p/>

<panel header="%%Admin {{ icon_embedding }}%% **FAQ: What are the differences between {{ module }} and {{ module }}T?**" type="seamless" minimized>
  <include src="appendixC-faq.md#admin-faq-{{ module | lower }}Vs{{ module | lower }}t" />
</panel>

</div>