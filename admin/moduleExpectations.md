{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("moduleExpectations") %} 
<div id="main">

<span tags="m--cs2103">

### Prior Knowledge: Java and OOP

This module requires you to write Java code almost every week, starting from the very first week. If your Java skills are rusty, do brush up your Java programming skills.

In particular, you may want to **have a look at the new Java 8 features** such as _streams_, _lambdas_, _Optionals_, that may not have been covered in previous Java modules.

CS2103 students: ==This module assumes a reasonable prior knowledge of Java and OOP== because most students taking this module have taken two Java modules before. If you are totally new to Java, you may be better off switching to CS2113 (Software Engineering & Object-Oriented Programming) instead.
</span>

### Workload

As {% if module == "TIC4001" %}100{% else %}70{% endif %}% of this module is based on CA, it can appear to be _heavy_. However, **it is not expected that you will spend more time on this module than its <tooltip content="e.g., if this module is core for you, it should not take more time than other level 2 core modules in your program">peer modules</tooltip>**.
* Note that the **module contains more things than a typical students can do**, in order to provide enough things for even the strongest students to learn as much as they wish to. 
* This means it is ==perfectly OK if you don't have time to learn everything the module offers==. Control your workload based on time you spend for the module in a week e.g., 1-1.5 days per week.
* We have provided a star rating system to guide you when prioritizing which things to do.

<div id="starRatingSystem">

#### Star Rating System

<div class="indented">

<p class="lead"><md>We use a _star rating system_ indicate the importance of module components. **Start with things that are rated one-star and progress to things with more stars.** Things rated four stars are optional.</md></p>

**Star ratings for topics** (and textbook sections):

* **One-star topics** {{ one_star }} are essential to keep up with the module. We recommend you to ==learn these topics if you want to pass the module== (i.e. up to a **C** grade).
* **Two-stars topics** {{ two_stars }} can get you up to a **B+**.
* **Three-stars topics** {{ three_stars }} can get you up to an **A**.
* **Four-stars topics** {{ four_stars }} can push you beyond the limits of the module, and help you get into a level above those who merely limit themselves to the topics of the module. They ==are not examinable==.

<span tags="m--cs2103 m--tic2002 m--tic4001">

* Topics marked with two {{ icon_prereq }} icons e.g., {{ prereq_one_star }},{{ prereq_two_stars }},{{ prereq_three_stars }} are relevant topics you are expected to have learned in prerequisite modules. They are given for reference, but ==are examinable==. The number of stars indicates the progression of topics, similar to the star rating system above i.e., one-star prerequisite topics are the most basic and the most important. four-star pre-requisite topics can be ignored without affecting CAP.
</span>

**Star ratings for other things** e.g., admin info sections:

* The module uses a similar star rating system to indicate the importance of other info in this website. i.e., information rated as one-star are the most essential. ==Info rated four stars are non-essential and can be ignored== without affecting your ability to follow the module.

</div>
</div>

</div>

{% endcall %}
