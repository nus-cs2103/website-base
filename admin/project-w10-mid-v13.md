{% macro show_main_text() %}
<div id="main">

<div id="title">

</div>
<div id="body">

<tip-box>

Overview: <include src="project-timeline.md#mid-v13-overview" inline />
</tip-box>


**<big>Project Management:</big>**

* :bulb: As you move the product towards v2.0 in small steps, ensure that **each PR that adds an enhancement also updates the relevant parts of documents and tests**. That way, your documentation/testing work will not pile up towards the end.


**<big>Product:</big>**

* {{ icon_important_big_red }} Try to **do a <tooltip content="resulting in a jar file on GitHub that can be downloaded by potential users">proper product release</tooltip>** as described in the Developer Guide. You can name it something like `v1.2.1`. Reason: You are _required_ to do a proper product release for v1.3. Doing a trial at this point will help you iron out any problems in advance.


**<big>Documentation:</big>**

* **User Guide**: Update where the document does not match the current product.
* **Developer Guide**: Similar to User Guide.

**<big>Demo:</big>**

* Optional. If you want feedback on your features, you can demo the feature and get feedback from the tutor.

</div>
</div>
{% endmacro %}

{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-w10-mid-v13", show_main_text) }}