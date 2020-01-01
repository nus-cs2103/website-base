{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}
{% from "admin/ip-tasks.mbdf" import duke_increments as d, learn_about_the_project, set_up_prerequisites, set_up_project, implement_increments with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Set up prerequisites
1. Set up the project in your computer
3. Implement increments while committing code frequently: `Level-1`, `Level-2`, `Level-3`, `Level-4`, `A-TextUiTesting`, `Level-5`, `Level-6`, `A-Enums` {{ timing_badge("by Thursday 2359") }}
{% endcall %}
<div id="body">

<box type="info">

The iP (and the tP) undergoes changes after each semester. As such, teething issues are a possibility. If you encounter any problem while doing the iP/tP, please post in the [forum]({{ forum_link }}) so that we can take necessary actions.
</box>

{{ learn_about_the_project(0) }}

{{ set_up_prerequisites(1) }}

{{ set_up_project(2) }}

{% call implement_increments(3, [d.Level_1, d.Level_2, d.Level_3, d.Level_4, d.A_TextUiTesting, d.Level_5, d.Level_6, d.A_Enums]) %}

<include src="ip-tasks.mbdf#commit-tag-push" />
<include src="ip-tasks.mbdf#no-jumping-ahead" />

{% endcall %}

</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w02", show_main_text) }}