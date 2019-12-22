{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Start weekly project meetings
1. Decide on a overall project direction %%(user profile, problem addressed)%% {{ timing_badge("before the tutorial") }}
1. Start a collaborative doc to take project notes {{ timing_badge("before the tutorial") }}
{% endcall %}

<div id="body">

Given below are some guidance on the recommended progress at this point of the project

#### {{ thumb(1) }} Start weekly project meetings

* We recommend you start weekly project meetings now. You can use the meeting to do tP tasks, but also help each other do iP tasks. On a related note, ==it is also acceptable to discuss weekly post-lecture quiz together with team members as you do the quiz== i.e., discuss and decide the answer collectively, but you should not give away your answers to someone who was not part of that discussion.

#### {{ thumb(2) }} Decide on a overall project direction %%(user profile, problem addressed)%%

* **Learn about the tP**
<div class="indented-level2">

{{ embed_topic("project-overview.md#main", "Admin " + icon_embedding + " **tP: Overview**", "3") }}
{{ embed_topic("project-product.md#main", "Admin " + icon_embedding + " **tP: Product**", "3") }}

</div>

* **Decide project direction, target user profile, and problem addressed** {{ timing_badge("before the tutorial", "secondary") }}

  Use your first project meeting to discuss with your team members and decide your project direction, target user profile, and the value proposition of the product, as described in the panels below:

<div class="indented-level2">

{{ embed_topic("project-scope.md#main", "Admin " + icon_embedding + " **tP: Scope**", "3") }}
{{ embed_topic("project-constraints.md#main", "Admin " + icon_embedding + " **tP: Constraints**", "3") }}
{{ embed_topic("project-grading.md#criteria-productDesign", "Admin " + icon_embedding + " **tP: Grading → Criteria Used for Grading the Product Design**", "3") }}

</div>

#### {{ thumb(3) }} Start a collaborative doc to take project notes {{ timing_badge("before the tutorial", "secondary") }}

* We recommend keeping project notes in easy-to-use collaborative docs such as GoogleDocs/sheets. Document the decisions taken above in one of those docs.

</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w04-inception", show_main_text) }}
