{% from "common/admin.njk" import show_admin_page with context %}
{% from "common/macros.njk" import show_troubleshooting with context %}

{% call show_admin_page("appendixG-Troubleshooting") %}
<div id="main">

<p class="lead"> This page contains some common technical problems encountered by students and possible solutions.</p>

## iP

{{ show_troubleshooting("uiPngRed", is_main_page=1, is_cs2103_only=1) }}
{{ show_troubleshooting("markdownTablesNotRendering", is_main_page=1, is_cs2103_only=1) }}
{{ show_troubleshooting("jarBreaksOnOtherOs", is_main_page=1, is_cs2103_only=1) }}
{{ show_troubleshooting("missingJavafxComponent", is_main_page=1, is_cs2103_only=1) }}
{{ show_troubleshooting("pipelineNotFound", is_main_page=1, is_cs2103_only=1) }}
{{ show_troubleshooting("moreRecentJavaVersion", is_main_page=1) }}
</div>

{% endcall %}
