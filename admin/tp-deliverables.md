{% from "common/macros.njk" import embed_topic with context %}
{% from "common/admin.njk" import show_admin_page with context %}

{% call show_admin_page("tp-deliverables") %}
<div id="main">

Here is a list of main deliverables of the project; their details are given in the subsequent sections.
* Product
  * [Executable](#deliverable-executable)
  * [Source code](#deliverable-source-code)
* Documentation
  * [User Guide](#deliverable-user-guide-ug)
  * [Developer Guide](#deliverable-developer-guide-dg)
  * [Product Website](#deliverable-product-website)
  * [Project Portfolio Page (PPP)](#deliverable-tp-portfolio-page-ppp)
* [Product Demo](#deliverable-demo)
* [Practical Exam Dry Run (PE-D)](#deliverable-practical-exam-dry-run-pe-d)
* [Practical Exam (PE)](#deliverable-practical-exam-pe)


### <div class="text-white bg-info p-1">Deliverable: Executable</div>
<span id="tp-deliverables-executable">
<include src="tp-deliverables-executable.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: Source code</div>
<span id="tp-deliverables-sourcecode">
<include src="tp-deliverables-sourcecode.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: User Guide (UG)</div>
<span id="tp-deliverables-ug">
<include src="tp-deliverables-ug.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: Developer Guide (DG)</div>
<span id="tp-deliverables-dg">
<include src="tp-deliverables-dg.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: Product Website</div>
<span id="tp-deliverables-website">
<include src="tp-deliverables-website.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: Project Portfolio Page (PPP)</div>
<span id="tp-deliverables-ppp">
<include src="tp-deliverables-ppp.md" />
</span>

### <div class="text-white bg-info p-1">Deliverable: Demo</div>
<span id="tp-deliverables-demo">
<include src="tp-deliverables-demo.md" />
</span>

### <div class="text-white bg-primary p-1">Deliverable: Practical Exam Dry Run (PE-D)</div>
<span id="tp-deliverables-practicalexam-dry-run">
<include src="tp-deliverables-ped.md" />
</span>

### <div class="text-white bg-success p-1">Deliverable: Practical Exam (PE)</div>
<span id="tp-deliverables-practicalexam">
<include src="tp-deliverables-pe.md" />
</span>

</div>

{% endcall %}
