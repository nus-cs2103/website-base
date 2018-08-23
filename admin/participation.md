{% macro show_main_text() %}
<div id="main">

10 marks allocated for participation can be earned in the following ways (there are 30+ available marks to choose from):

* <tooltip content="No `Below Average`/`Poor` ratings">Good peer ratings</tooltip>
  * Criteria for professional conduct (1 mark for each criterion, max 7)
  * Competency criteria (2 marks for each, max 6)
* Quizzes
  * In-lecture quizzes (1 each, max 10 marks)
  * ~~Post-lecture quizzes (0.5 each, max 5 marks)~~
* Module admin tasks done _on time_ and _as instructed_
  * Peer evaluations (1 marks each, max 3)
  * Pre-module survey (1 marks)
* Enhanced AB1-AB3 (2 mark each, max 6 marks)

{{ embed_topic("peerEvaluations.md#peerEvaluation-criteria", "Admin " + icon_embedding + " Peer Evaluations → Criteria", "participation-peerEvals", "3") }}

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("participation", show_main_text) }}
