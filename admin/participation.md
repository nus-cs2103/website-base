{% macro show_main_text() %}
<div id="main">

**To receive full 10 marks allocated for participation, earn at least 15 participation _points_.**

There are 30+ available points to choose from:

* <tooltip content="No `Below Average`/`Poor` ratings">Good peer ratings</tooltip>
  * Criteria for professional conduct (1 point for each criterion, max 7)
  * Competency criteria (2 points for each, max 6)

<div class="indented">
  <box type="warning">

  Only those who submit peer evaluations can earn participation points from peer evaluations they receive.
  </box>
</div>

* In-lecture quizzes (1 each, max 10 points)
* Module admin tasks done _on time_ and _as instructed_
  * Peer evaluations (1 points each, max 3)
  * Pre-module survey (1 points)
* Enhanced AB1-AB3 (2 points each, max 6 points)


{{ embed_topic("peerEvaluations.md#peerEvaluation-criteria", "Admin " + icon_embedding + " Peer Evaluations → Criteria", "participation-peerEvals", "3") }}

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("participation", show_main_text) }}
