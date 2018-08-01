{% macro show_main_text() %}
<div id="main">

10 marks allocated for participation can be earned in the following ways (there are ~28 available marks to choose from):

* <tooltip content="No `Below Average`/`Poor` ratings">Good peer ratings</tooltip>
  * Criteria for professional conduct (1 mark for each criterion, max 7)
  * Competency criteria (2 marks for each, max 6)
* In-lecture quizzes
  * In-lecture quizzes (0.5 each, max 5 marks)
  * Post-lecture quizzes (0.5 each, max 5 marks)
* Module admin tasks done _on time_ and _as instructed_
  * Peer evaluations (1 marks each)
  * Pre-module survey (0.5 marks)
* Enhanced AB1-AB3: 1 mark each

<span class="flat">%%Related: [[Admin: Peer Evaluation](#admin-peerEvaluations-anchor)]%%</span>
<panel src="peerEvaluations.md#peerEvaluation-criteria" header="Admin {{ icon_embedding }} Peer Evaluations → Criteria" class="embedding" minimized />
  
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("participation", show_main_text) }}