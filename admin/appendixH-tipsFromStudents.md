{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import show_troubleshooting with context %}
{% from "admin/tips-from-students-fragment.md" import show_tips_list with context %}

{% call show_admin_page("appendixH-tipsFromStudents") %}
<div id="main">

<p class="lead"><md>This is a curated collection of tips from past students, **collected via ==an anonymous post-course survey==**.</md>
</p>

{{ show_tips_list() }}

</div>

{% endcall %}
