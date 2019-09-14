{% from "common/admin.njk" import show_admin_page, show_project_summary_lead with context %}
{% from "common/macros.njk" import embed_topic, thumb, timing_badge with context %}

{% macro show_main_text() %}
<div id="main">

{% call show_project_summary_lead()%}
1. Finalize the features
1. Set up the product website
1. Release the product
{% endcall %}
<div id="body">

<box type="important">

**Aim to finish the iP by this week!**<br> Although the official iP submission deadline is Week 7 Monday, aim to finish the iP **by this week's <tooltip content="i.e., 2359 before the tutorial">weekly deadline</tooltip>** so that you can devote more time to the tP after this week. %%The extra time for the iP (i.e., from week 6 to 7) is meant as a buffer for those lagging behind in the iP.%%
</box>

#### {{ thumb(1) }} Finalize the features

* You may give the product any name, but do not rename the repo.
* Reminder: you can give the chatbot any personality (there is no need to follow the exact command/response formats given)

#### {{ thumb(2) }} Set up a product website

* **Add a representative screenshot** of the product to the `docs` folder.
  * ==The file name should be `docs/Ui.png` exactly== (even if the file format is not `png`, name it `png`)
  * Ideally, the product name is visible in the screenshot e.g., in the title bar of the Window

<div class="indented-level2">

{{ embed_topic("project-deliverables.md#tips-for-product-screenshot", "Admin " + icon_embedding + " Team Project (tP) → Tips for Product Screenshots", "ipW6-tipsForScreenshots", "3") }}
</div>

* **Add a brief User Guide (UG)**

<div class="indented">

<include src="dukeFragment.md" boilerplate var-header="**`A-UserGuide`: User Guide**" var-fragment="extensions.mbdf#A-UserGuide" />
</div>
<p/>

#### {{ thumb(3) }} Release the product

* Create a new jar file.
* Ensure the jar file works %%(reason: it will be used to grade your iP)%%.<br>
  ==Get a team member to test the Jar file on their computer== %%(reason: it's possible for the jar file to work on your computer but not on others')%%.
* Create a new release on GitHub (e.g., `v0.2`) and upload the jar file.

<div class="indented">

<include src="dukeFragment.md" boilerplate var-header="**`A-Release`: Release**" var-fragment="extensions.mbdf#A-Release" />
</div>
<p/>

</div>
</div>
{% endmacro %}

{{ show_admin_page("ip-w06", show_main_text) }}