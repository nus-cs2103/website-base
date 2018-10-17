{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<p class="lead" style="color: purple"><md>{{ far_calendar_check }} <include src="project-timeline.md#mid-v13-overview" inline /></md></p>


**<big>Project Management:</big>**

* Continue to do deliberate project management using GitHub issue tracker, milestones, labels, etc. as you did in v1.2.
* :bulb: We recommend that **each PR also updates the relevant parts of documents and tests**. That way, your documentation/testing work will not pile up towards the end.
* :bulb: There is [a way to get GitHub to auto-close the relevant issue when a PR is merged](https://help.github.com/articles/closing-issues-using-keywords/) ([example](https://github.com/se-edu/addressbook-level4/pull/888)).


**<big>Product:</big>**

* {{ icon_important_big_red }} **Do a <tooltip content="resulting in a jar file on GitHub that can be downloaded by potential users">proper product release</tooltip>** as described in the Developer Guide. You can name it something like `v1.2.1`. Ensure that the jar file works as expected by doing some manual testing. %%Reason: You are _required_ to do a proper product release for v1.3. Doing a trial at this point will help you iron out any problems in advance. It may take additional effort to get the jar working especially if you use third party libraries or additional assets such as images.%%


**<big>Documentation:</big>**

* **User Guide**: Update where the document does not match the current product.
* **Developer Guide**: Similar to the User Guide.

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w10-mid-v13", show_main_text) }}