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
  iter1: "Iteration 1 " + ("(W7-W8)" if tic4002 else "(W8-W9)"),
  iter2: "Iteration 2 " + ("(W9-W10)" if tic4002 else "(W10-W11)"),
  iter3: "Iteration 3 " + ("(W12-W13)" if tic4001 else ( "(W11-W12)" if tic4002 else "(W12)"))
}%}



{% macro project_gantt_pre(g) %}
<puml name="tpGanttChart-preIterations.png">
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
<puml name="tpGanttChart-iterations.png">
@startgantt
[{{ g.iter1 }}] lasts 14 days
[{{ version_first }}] happens at [{{ g.iter1 }}]'s end
then [{{ g.iter2 }}] lasts 14 days
[{{ version_penultimate }}] happens at [{{ g.iter2 }}]'s end
then [{{ g.iter3 }}] lasts {{ "14" if tic4001 or tic4002 else "7" }} days
[{{ version_final }}] happens at [{{ g.iter3 }}]'s end
@endgantt
</puml>
{% endmacro %}

{% macro badge(text) %}<span class="badge badge-dark">{{ text }}</span>{% endmacro %}

The tP spans ten weeks, and is to be done in _breadth-first iterative_ fashion.

**The first half of the tP will be spent of laying out the foundation for the iterations**, as illustrated below (note that the diagrams above show the relative size of tasks i.e., smaller tasks are shown as shorter bar).

{{ project_gantt_pre(g) }}

{% set tfw = (tp_first_week | int) %}

<div class="indented-level2">

#### {{ badge("Week " + tfw)}} {{ weekly_tp_themes.w3.name }}

* Form teams
* Set weekly meeting times

#### {{ badge("Week " + (tfw + 1))}} {{ weekly_tp_themes.w4.name }}

* Decide on a general direction for the project (i.e., target user profile, and problem addressed)

#### {{ badge("Week " + (tfw + 2))}} {{ weekly_tp_themes.w5.name }}

* Gather requirements in the form of _user stories_.
* Decide which of them will go into the first version.

#### {{ badge("Week " + (tfw + 3))}} {{ weekly_tp_themes.w6.name }}

* Decide how the product will look like at {{ version_first }}.
* Record that product concept in the form of a user guide.

#### {{ badge("Week " + (tfw + 4))}} {{ weekly_tp_themes.w7.name }}

* Ensure development environment is set up.

* Plan the next iteration i.e., decide who will do which parts by when.

<div tags="m--cs2103">

* Do a _practice_ iteration ({{ version_practice }} to get used to the workflow. In this iteration, only some documents will be updated.
</div>
</div>

The first half of the tP is light because you will be doing the iP in parallel during that time.

**The second half of the tP is divided into three iterations**, each of which is expected to produce a working version of the product by evolving the product delivered in the previous iteration.

{{ project_gantt_iterations(g) }}

<div class="indented-level2">

#### {{ badge("&nbsp;W" + (tfw + 5)+ "&nbsp;")}} {{ badge("&nbsp;W" + (tfw + 6)+ "&nbsp;")}} Iteration 1 → {{ version_first }}

* This is the first proper iteration.
* Aim to deliver an <tooltip content="Minimum Viable Product">MVP</tooltip> version of the product.


#### {{ badge("W" + (tfw + 7))}} {{ badge("W" + (tfw + 8))}} Iteration 2 → {{ version_penultimate }}

<div tags="m--cs2113 m--cs2103 m--tic4002">

* This version will be tested by peers and you will receive the bug reports without any penalty.
* Aim to **deliver all <tooltip content="i.e., all features you plan to deliver in this project at the end of the semester">target features</tooltip>** so that you can get them tested for free.
</div>
<div tags="m--tic4001 m--tic4002">

* Aim to **deliver almost all <tooltip content="i.e., all features you plan to deliver in this project at the end of the semester">target features</tooltip>** because there will be additional documentation work to be done in the next iteration.
</div>


#### {{ badge("W" + (tfw + 9))}} {{ badge("W" + (tfw + 10)) if tic4001 or tic4002 }} Iteration 3 → {{ version_final }}

<div tags="m--cs2113 m--cs2103">

* This iteration is <span class="text-danger">shorter</span> (slightly more than one week).
* Plan to use this **for bug fixing and polishing up documentation**.
</div>
<div tags="m--tic4001 m--tic4002">

* Do final fine tuning to features.
* Add documentation.
</div>

</div>

**The final submission** will be at the {{ "end" if module == "TIC4001" else "start" }} of week 13. [Deliverables](tp-deliverables.html) include an executable jar file, a product website (containing both user and developer documentation), a demo video, among other things.

<div class="indented-level2" tags="m--cs2113 m--cs2103 m--tic4002">

#### {{ badge("W13")}} Evaluation

* The final submission is subjected to a intensive peer testing (in a so called [_practical exam_](tp-pe.html#tp-practical-exam-pe)).
* You will get credit for finding bugs in others' deliverables and penalized for bugs found in your deliverables.

</div>

</div>

{% endcall %}
