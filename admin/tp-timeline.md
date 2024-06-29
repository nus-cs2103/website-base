{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{% from "_course-" + course + "/weeklyTpTasks-fragment.md" import weekly_tp_themes with context %}

{% call show_admin_page("tp-timeline") %}
<div id="main">

{% set g = {
  w3: weekly_tp_themes.w3.name,
  w4: weekly_tp_themes.w4.name,
  w5: weekly_tp_themes.w5.name,
  w6: weekly_tp_themes.w6.name,
  w7: weekly_tp_themes.w7.name,
  iter1: "Iteration 1 (W7)",
  iter2: "Iteration 2 (W8)",
  iter3: "Iteration 3 (W9)",
  iter4: "Iteration 4 (W10)",
  iter5: "Iteration 5 (W11-W12)",
  iter6: "Iteration 6 (W13)"
} if cs2103 else {
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
<puml name="tpGanttChart-preIterations.png">
@startgantt
[{{ g.w3 }}] lasts 1 days
then [{{ g.w4 }}] lasts 1 days and starts 6 days after [{{ g.w3 }}]'s end
then [{{ g.w5 }}] lasts 2 days and starts 6 days after [{{ g.w4 }}]'s end
then [{{ g.w6 }}] lasts 3 days and starts 5 days after [{{ g.w5 }}]'s end
@endgantt
</puml>
{% endmacro %}

{% macro project_gantt_iterations(g) %}
<puml name="tpGanttChart-iterations.png">
@startgantt
{% if cs2103 %}
[{{ g.iter1 }}] lasts 7 days
[{{ version_practice }}] happens at [{{ g.iter1 }}]'s end
then [{{ g.iter2 }}] lasts 7 days
[{{ version_first }}] happens at [{{ g.iter2 }}]'s end
then [{{ g.iter3 }}] lasts 7 days
[{{ version_mvp }}] happens at [{{ g.iter3 }}]'s end
then [{{ g.iter4 }}] lasts 7 days
[{{ version_alpha }}] happens at [{{ g.iter4 }}]'s end
then [{{ g.iter5 }}] lasts 14 days
[{{ version_penultimate }}] happens at [{{ g.iter5 }}]'s end
then [{{ g.iter6 }}] lasts 3 days
[{{ version_final }}] happens at [{{ g.iter6 }}]'s end
{% else %}
[{{ g.iter1 }}] lasts 14 days
[{{ version_first }}] happens at [{{ g.iter1 }}]'s end
then [{{ g.iter2 }}] lasts 14 days
[{{ version_penultimate }}] happens at [{{ g.iter2 }}]'s end
then [{{ g.iter3 }}] lasts 7 days
[{{ version_final }}] happens at [{{ g.iter3 }}]'s end
{% endif %}
@endgantt
</puml>
{% endmacro %}

{% macro badge(text) %}<span class="badge bg-dark">{{ text }}</span>{% endmacro %}

The tP spans ten weeks, and is to be done in _breadth-first iterative_ fashion.

****The first portion of the tP**** **will be spent of laying out the foundation for the iterations**, as illustrated below. This portion of the tP is light because you will be doing the individual project (iP) in parallel during this time.

{{ project_gantt_pre(g) }}
--Note: that the diagrams above show the relative size of tasks i.e., smaller tasks are shown as shorter bars--

{% set tfw = (tp_first_week | int) %}

<div class="indented-level2">

#### {{ badge("Week " + tfw)}} {{ weekly_tp_themes.w3.name }}

* Form teams.{{ bullet_target_green }}
* Set weekly meeting times.

#### {{ badge("Week " + (tfw + 1))}} {{ weekly_tp_themes.w4.name }}

* Decide on a general direction for the project %%(i.e., target user profile, and problem addressed)%%.{{ bullet_target_green }}

#### {{ badge("Week " + (tfw + 2))}} {{ weekly_tp_themes.w5.name }}

* Gather requirements in the form of _user stories_.{{ bullet_target_green }}
* Decide which of them will go into the first version.

#### {{ badge("Week " + (tfw + 3))}} {{ weekly_tp_themes.w6.name }}

* Decide how the product will look like at {{ version_first }}.{{ bullet_target_green }}
* Record that product concept in the form of a user guide.

</div>


****The second portion of the tP**** **is divided into multiple iterations**, each of which is expected to produce a working version of the product by evolving the product delivered in the previous iteration.

{{ project_gantt_iterations(g) }}
<p/>

<div tags="m--cs2113" class="indented-level2">

#### {{ badge("Week " + (tfw + 4))}} {{ weekly_tp_themes.w7.name }}

* Ensure development environment is set up.{{ bullet_target_green }}
* Plan the next iteration i.e., decide who will do which parts by when.


#### {{ badge("&nbsp;W" + (tfw + 5)+ "&nbsp;")}} {{ badge("&nbsp;W" + (tfw + 6)+ "&nbsp;")}} Iteration 1 → {{ version_first }}

* This is the first proper iteration.{{ bullet_target_green }}
* Aim to deliver an <tooltip content="Minimum Viable Product">MVP</tooltip> version of the product.


#### {{ badge("W" + (tfw + 7))}} {{ badge("W" + (tfw + 8))}} Iteration 2 → {{ version_penultimate }}

* This version will be tested by peers and you will receive the bug reports without any penalty.{{ bullet_target_green }}
* Aim to **deliver all <tooltip content="i.e., all features you plan to deliver in this project at the end of the semester">target features</tooltip>** so that you can get them tested for free.


#### {{ badge("W" + (tfw + 9))}} Iteration 3 → {{ version_final }}

* This iteration is <span class="text-danger">shorter</span>.{{ bullet_target_green }}
* ==**Changes to features are strongly discouraged** in this iteration.== Use it for bug fixing, code quality improvements, improving the tests, and polishing up documentation only.

</div>

<div tags="m--cs2103" class="indented-level2">

#### {{ badge("W" + (tfw + 4))}} Iter.1 %%[ --{{ weekly_tp_themes.w7.name }}-- ]%%

<div id="v11-goals" class="indented">
<box header="****{{ version_practice }}****" light>

* **Learning outcome**: Able to follow the workflow as a team.{{ bullet_target_green }}
* **Product goal**: Update some documents to match the new product direction.
* **Strategy**: Practice the workflow while updating the documents.
</box>
</div>

<box type="info" seamless>

**Aim to do 'just enough':**{.text-info}
Note how the 'Learning outcome' appears _above_ 'Product goal', and how the product goal derives from the learning outcome. Unlike in a real SE project, the product in the tP exists only to help you achieve the learning outcome. Hence, aim to **do 'just enough' on the product front to achieve the intended learning outcome of the iteration** %%(e.g., don't make features bigger necessary)%% so that the tP doesn't add to your workload more than necessary.
</box>


#### {{ badge("&nbsp;W" + (tfw + 5)+ "&nbsp;")}} Iter.2 %%[ --{{ weekly_tp_themes.w8.name }}-- ]%%

<div id="v12-goals" class="indented">
<box header="****{{ version_first }}****" light>

* **Learning outcome**: Able to update functional code while working in parallel.{{ bullet_target_green }}
* **Product goal**: Take the first step towards an MVP by delivering at least _some_ functionality changes.
* **Strategy**: Define the smallest possible MVP. Each member tries to merge at least one PR that moves the product towards that MVP.

</box>
</div>

#### {{ badge("&nbsp;W" + (tfw + 6)+ "&nbsp;")}} Iter.3 %%[ --{{ weekly_tp_themes.w9.name }}-- ]%%

<div id="v13-goals" class="indented">
<box header="****{{ version_mvp }}****" light>

* **Learning outcome**: Able to deliver a fully working product, on time.{{ bullet_target_green }}
* **Product goal**: Reach a <tooltip content="Minimum Viable Product">MVP</tooltip>.
* **Strategy**: Reach MVP as soon as possible, by implementing the ==simplest versions of _must-have_ features only==. Use the remaining time to move the product further forward, while staying within own workload limitations.
</box>
</div>


#### {{ badge("W" + (tfw + 7))}} Iter.4 %%[ --{{ weekly_tp_themes.w10.name }}-- ]%%

<div id="v14-goals" class="indented">
<box header="****{{ version_alpha }}****" light>

* **Learning outcome**: Able to tweak the product/project plan to match the available time/resources.{{ bullet_target_green }}
* **Product goal**: Implement <popover content="i.e., _almost_ complete implementation of the feature, even if not fully polished">fully-fledged</popover>. versions of _all_ the features intended for final release.
* **Strategy**: Add features based on priority, while maintaining a working product. It is OK if the features are slightly rough around the edges, as the next iteration can still do minor tweaks to features.
</box>
</div>


#### {{ badge("W" + (tfw + 8))}} {{ badge("W" + (tfw + 9))}} Iter.5 %%[ --{{ weekly_tp_themes.w12.name }}-- ]%%

<div id="v15-goals" class="indented">
<box header="****{{ version_penultimate }}****" light>

* **Learning outcome**: Able to apply internal quality control.{{ bullet_target_green }}
* **Product goal**: Reach the _release candidate (RC)_ version, ready for a public beta testing (i.e., the product quality should be sufficiently high %%e.g., no obvious bugs%%).
* **Strategy**: Do an <popover content="A full-product testing conducted by internal testers (in this case, project members themselves) acting as target users">alpha test</popover> internally, and refine features as necessary. Improve tests, documentation, code quality.

</box>
</div>

<box type="info" seamless>

This version (i.e., {{ version_penultimate }}) will undergo a limited beta testing  (done by other teams) and you will receive the bug reports without any penalty.
</box>



#### {{ badge("W" + (tfw + 10))}} Iter.6 %%[ --{{ weekly_tp_themes.w13.name }}-- ]%%

<div id="v16-goals" class="indented">
<box header="****{{ version_final }}****" light>

* **Learning outcome**: Able to put in final touches while minimizing delivery risks %%i.e., risks of regressions or deadline overruns%%.{{ bullet_target_green }}
* **Product goal**: Reach the quality necessary for a public release.
* **Strategy**: Freeze features. Strictly limit changes to bug fixes only.
</box>
</div>

<box type="warning" seamless>

* This iteration is <span class="text-danger">very short</span> (just a few days).<br>
  ==**Even minute/cosmetic changes to features are not allowed** in this iteration== due to the _feature freeze_ enforced.
* This version will be subjected to an intensive peer testing (the so-called [_practical exam_](tp-pe.html#tp-practical-exam-pe)).
  You will get credit for finding bugs in others' tP deliverables and penalized for bugs found in your deliverables.
</box>

</div>

</div>

{% endcall %}
