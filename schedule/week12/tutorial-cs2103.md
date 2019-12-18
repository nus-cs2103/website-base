{% from "common/macros.njk" import embed_topic, thumb, show_as_tab, timing_badge with context %}
{% from "schedule/index.md" import show_week_pagetop with context%}
{{ show_week_pagetop(12, "tutorial") }}

{% from "common/macros.njk" import embed_topic with context %}

#### {{ thumb(1) }} Demo rehearsal

* Do a project demo dry run (as per project demo instructions given below) for your tutor.

<div class="indented-level2">
{{ embed_topic("../../admin/project-deliverables.md#project-deliverables-demo", "Admin " + icon_embedding + " tP → Deliverables → **Demo**", "t12_demo", "3") }}
</div>

#### {{ thumb(2) }} Exercise: process models

<div class="indented-level2">
<box type="info">

Do this if you did not do this in the previous week's tutorial.
</box>
</div>

* Divide XP and Scrum between the two sub-teams.

* Each person to use the Web to find about 2 distinguishing features of the process model i.e., if the sub-team has 2 members, find info about 4 features.
  * Some interesting [SCRUM concepts](https://www.scrum.org/resources/what-is-scrum): Product backlog, scrum board, story points, burndown charts, scrum master, product owner
  * XP rules are described at [http://www.extremeprogramming.org/rules.html](http://www.extremeprogramming.org/rules.html)

* Relate those features to your project. %%i.e. are they applicable? are you doing something similar?%%
