{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-pe") %}
<div id="main">

### <div class="text-white bg-primary p-1">tP: Practical Exam Dry Run (PE-D)</div>
<div id="tp-practicalexam-dry-run">
<include src="tp-ped-fragment.md" />
</div>

</div>

{% endcall %}
