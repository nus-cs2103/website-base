{% macro show_main_text() %}
<div id="main">

Here is a list of main deliverables of the project; their details are given in the subsequent sections.
* Product
  * [Executable](#deliverable-executable)
  * [Source code](#deliverable-source-code)
* Documentation
  * [User Guide](#deliverable-user-guide-ug)
  * [Developer Guide](#deliverable-developer-guide-dg)
  * [Product Website](#deliverable-product-website)
  * [Project Portfolio Page (PPP)](#deliverable-project-portfolio-page-ppp)
* [Product Demo](#deliverable-demo)
* [Practical Exam Dry Run (PE-D)](#deliverable-practical-exam-dry-run-pe-d)
* [Practical Exam (PE)](#deliverable-practical-exam-pe)


### <div class="text-white bg-info p-1">Deliverable: Executable</div>
<span id="project-deliverables-executable">
<include src="project-deliverables-executable.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: Source code</div>
<span id="project-deliverables-sourcecode">
<include src="project-deliverables-sourcecode.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: User Guide (UG)</div>
<span id="project-deliverables-ug">
<include src="project-deliverables-ug.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: Developer Guide (DG)</div>
<span id="project-deliverables-dg">
<include src="project-deliverables-dg.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: Product Website</div>
<span id="project-deliverables-website">
<include src="project-deliverables-website.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: Project Portfolio Page (PPP)</div>
<span id="project-deliverables-ppp">
<include src="project-deliverables-ppp.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: Demo</div>
<span id="project-deliverables-demo">
<include src="project-deliverables-demo.md" />
</span>

### <div class="text-white bg-primary p-1">Deliverable: Practical Exam Dry Run (PE-D)</div>
<span id="project-deliverables-practicalexam-dry-run">
<include src="project-deliverables-ped.md" />
</span>

### <div class="text-white bg-success p-1">Deliverable: Practical Exam (PE)</div>
<span id="project-deliverables-practicalexam">
<include src="project-deliverables-pe.md" />
</span>

</div>
{% endmacro %}

{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}
{{ show_admin_page("project-deliverables", show_main_text) }}
