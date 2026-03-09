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
  * [Project Portfolio Page (PPP)](#deliverable-project-portfolio-page-ppp)
* [Product Demo](#deliverable-demo)


<div id="tp-deliverables-executable">
<h3 class="d-block text-white bg-info p-1 ps-2 mt-4 mb-3">Deliverable: Executable</h3>


<include src="tp-deliverables-executable-fragment.md" />
</div>

<div id="tp-deliverables-sourcecode">

<h3 class="d-block text-white bg-info p-1 ps-2 mt-4 mb-3">Deliverable: Source code</h3>

<include src="tp-deliverables-sourcecode-fragment.md" />
</div>

<div id="tp-deliverables-ug">

<h3 class="d-block text-white bg-info p-1 ps-2 mt-4 mb-3">Deliverable: User Guide (UG)</h3>

<include src="tp-deliverables-ug-fragment.md" />
</div>

<div id="tp-deliverables-dg">

<h3 class="d-block text-white bg-info p-1 ps-2 mt-4 mb-3">Deliverable: Developer Guide (DG)</h3>

<include src="tp-deliverables-dg-fragment.md" />
</div>

<div id="tp-deliverables-website">

<h3 class="d-block text-white bg-info p-1 ps-2 mt-4 mb-3">Deliverable: Product Website</h3>

<include src="tp-deliverables-website-fragment.md" />
</div>

<div id="tp-deliverables-ppp">

<h3 class="d-block text-white bg-info p-1 ps-2 mt-4 mb-3">Deliverable: Project Portfolio Page (PPP)</h3>

<include src="tp-deliverables-ppp-fragment.md" />
</div>

<div id="tp-deliverables-demo">

<h3 class="d-block text-white bg-info p-1 ps-2 mt-4 mb-3">Deliverable: Demo</h3>

<include src="tp-deliverables-demo-fragment.md" />
</div>

</div>

{% endcall %}
