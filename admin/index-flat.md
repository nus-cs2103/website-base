<frontmatter>
title: "Admin (All admin info in one page!)"
footer: footer.md
siteNav: adminSiteNav-flat.md
head: adminHead-flat.md
</frontmatter>


<div class="website-content">

<include src="../common/header-flat.md" />

{% from "common/admin.njk" import topics, show_title with context %}


{% macro show_hr()%} 
<hr style="border-width: 3px; background-color: #f3ccff">
{% endmacro %}


{% macro show_thin_hr()%} 
<hr style="border-width: 1px; border-color: #f3ccff; border-style: dotted">
{% endmacro %}


{% for topic in topics %} 
{% if topic.level in [1,2] %} 
{% if (not loop.first) and (topic.level == 1)%} 
{{ show_hr() }}
{% elif (not loop.first) and (topic.level == 2)%}
{{ show_thin_hr() }}
{% endif %}
<div id="admin-{{ topic.id }}-anchor"></div>
<div id="admin-{{ topic.id }}">
{{ show_title(topic.id, topics) | trim }}
<div class="indented-less">
  <include src="{{ topic.id }}.md#main" />
</div>
</div>
<br>
{% elif topic.level == 0 %}
{{ show_hr() }}

# {{ topic.title }}
{% endif %}
{% endfor %}

</div>
