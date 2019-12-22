{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}

1. {{ icon_individual }} Deliver the feature
1. {{ icon_individual }} Update user docs
1. {{ icon_team }} Release as a jar file
1. {{ icon_team }} Wrap up the milestone
1. {{ icon_individual }} Attend the practical exam dry run {{ timing_badge("during Lecture") }}
{% endcall %}

<div id="body">

#### {{ thumb(1) }} {{ icon_individual }} Deliver the feature

* Ideally, this version of the feature should be a release-candidate for the v1.4 i.e., has the functionality expected of v1.4.


#### {{ thumb(2) }} {{ icon_individual }} Update user docs

* {{ icon_important_big_red }} v1.3 user guide should be updated to match the current version of the product. %%Reason: testers will need to refer to the UG during the practical exam dry run%%.
  * Clearly indicate which features are not implemented yet %%e.g. tag those features with a `Coming in v2.0`%%.
  * For those features already implemented, ensure their descriptions match the exact behavior of the product %%e.g. replace mockups with actual screenshots%%

* **README page**: Update to look like a real product (rather than a project for learning SE) if you haven't done so already. In particular, ==update the `Ui.png` to match the current product (<trigger trigger="click" for="modal:v13-tipsForProductScreenshot">{{ icon_tip }} tips</trigger>)==.

<modal large title="Admin → Project Deliverables → Website" id="modal:v13-tipsForProductScreenshot">
  <include src="project-deliverables-website.md#tips-for-product-screenshot"/>
</modal>


#### {{ thumb(3) }} {{ icon_team }} Release as a jar file

* {{ icon_important_big_red }} **Do a <tooltip content="resulting in a jar file on GitHub that can be downloaded by potential users">proper product release</tooltip>** [as described in the Developer Guide]({{ ab3_website }}/DevOps.html#making-a-release). Do some manual tests to ensure the jar file works.


#### {{ thumb(4) }} {{ icon_team }} Wrap up the milestone

* as before


#### {{ thumb(5) }} {{ icon_individual }} Attend the practical exam dry run {{ timing_badge("during Lecture", "secondary") }}

* =={{ icon_important_big_red }} See info in the panel below:==

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#project-deliverables-practicalexam-dry-run", "Admin " + icon_embedding + " tP Deliverables → **Practical Exam - Dry Run**", "1") }}
</div>


</div>
</div>
{% endmacro %}

{{ show_admin_page("project-w11-v13", show_main_text) }}
