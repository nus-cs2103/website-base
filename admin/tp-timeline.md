{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{% from "_module-" + module + "/weeklyTpTasks.mbdf" import weekly_tp_themes with context %}

{% call show_admin_page("tp-timeline") %}
<div id="main">

{% set g = {
  w3: weekly_tp_themes.w3.name,
  w4: weekly_tp_themes.w4.name,
  w5: weekly_tp_themes.w5.name,
  w6: weekly_tp_themes.w6.name,
  w7: weekly_tp_themes.w7.name,
  iter1: "Iteration 1 (W8-W9)",
  iter2: "Iteration 2 (W10-W11)",
  iter3: "Iteration 3 (W12)"
}%}



{% macro project_gantt_pre(g) %}
<puml>
@startgantt
[{{ g.w3 }}] lasts 1 days
then [{{ g.w4 }}] lasts 1 days and starts 6 days after [{{ g.w3 }}]'s end
then [{{ g.w5 }}] lasts 2 days and starts 6 days after [{{ g.w4 }}]'s end
then [{{ g.w6 }}] lasts 3 days and starts 5 days after [{{ g.w5 }}]'s end
then [{{ g.w7 }}] lasts 4 days and starts 4 days after [{{ g.w6 }}]'s end
@endgantt
</puml>
{% endmacro %}

{% macro project_gantt_iterations(g) %}
<puml>
@startgantt
[{{ g.iter1 }}] lasts 14 days
[{{ version_first }}] happens at [{{ g.iter1 }}]'s end
then [{{ g.iter2 }}] lasts 14 days
[{{ version_penultimate }}] happens at [{{ g.iter2 }}]'s end
then [{{ g.iter3 }}] lasts 7 days
[{{ version_final }}] happens at [{{ g.iter3 }}]'s end
@endgantt
</puml>
{% endmacro %}

{% macro badge(text) %}<span class="badge badge-dark">{{ text }}</span>{% endmacro %}

The tP spans ten weeks, and is to be done in _breadth-first iterative_ fashion.

**The first half of the tP will be spent of laying out the foundation for the iterations**, as illustrated below (note that the diagrams above show the relative size of tasks i.e., smaller tasks are shown as shorter bar).

{{ project_gantt_pre(g) }}

<div class="indented-level2">

#### {{ badge("Week 3")}} {{ weekly_tp_themes.w3.name }}

* Form teams
* Set weekly meeting times

#### {{ badge("Week 4")}} {{ weekly_tp_themes.w4.name }}

* Decide on a general direction for the project (i.e., target user profile, and problem addressed)

#### {{ badge("Week 5")}} {{ weekly_tp_themes.w5.name }}

* Gather requirements in the form of _user stories_.
* Decide which of them will go into the first version.

#### {{ badge("Week 6")}} {{ weekly_tp_themes.w6.name }}

* Decide how the product will look like at {{ version_first }}.
* Record that product concept in the form of a user guide.

#### {{ badge("Week 7")}} {{ weekly_tp_themes.w7.name }}

* Ensure development environment is set up.

* Plan the next iteration i.e., decide who will do which parts by when.

<div tags="m--cs2103">

* Do a trial iteration ({{ version_trial }} to get used to the workflow. In this iteration, only some documents will be updated.
</div>
</div>

The first half of the tP is light because you will be doing the iP in parallel during that time.

**The second half of the tP is divided into three iterations**, each of which is expected to produce a working version of the product by evolving the product delivered in the previous iteration.

{{ project_gantt_iterations(g) }}

<div class="indented-level2">

#### {{ badge("&nbsp;W8&nbsp;")}} {{ badge("&nbsp;W9&nbsp;")}} Iteration 1 → {{ version_first }}

* This is the first proper iteration.
* Aim to deliver an <tooltip content="Minimum Viable Product">MVP</tooltip> version of the product.


#### {{ badge("W10")}} {{ badge("W11")}} Iteration 2 → {{ version_penultimate }}

* This version will be tested by peers and you will receive the bug reports without any penalty.
* Aim to **deliver all <tooltip content="i.e., all features you plan to deliver in this project at the end of the semester">target features</tooltip>** so that you can get them tested for free.


#### {{ badge("W12")}} Iteration 3 → {{ version_final }}

* This iteration is <span class="text-danger">shorter</span> (slightly more than one week).
* Plan to use this **for bug fixing and polishing up documentation**.

</div>

**The final submission** will be in week early week 13. [Deliverables](tp-deliverables.html) include an executable jar file, a product website (containing both user and developer documentation), a demo video, among other things.

<div class="indented-level2">

#### {{ badge("W13")}} Evaluation

* The final submission is subjected to a intensive peer testing (in a so called [_practical exam_](tp-pe.html#tp-practical-exam-pe)).
* You will get credit for finding bugs in others' deliverables and penalized for bugs found in your deliverables.

</div>

</div>

{% endcall %}
