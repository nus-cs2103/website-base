<div id="flex-body">
{% if file %}
<nav id="site-nav" class="fixed-header-padding">
<div class="site-nav-top">
<div class="font-weight-bold mb-2" style="font-size: 1.25rem;">{{ sitenav_title }}</div>
</div>
<div class="nav-component slim-scroll">
<include src="sitenav-{{ file }}.md" />
</div>
</nav>
{% endif %}
<div id="content-wrapper" class="fixed-header-padding">
{{ content }}
</div>
<nav id="page-nav" class="fixed-header-padding">
<div class="nav-component slim-scroll">
<page-nav />
</div>
</nav>
</div>