{% from "common/admin.njk" import topics with context %}

<navigation>

{% for topic in topics %} 
{% set decoration = "==" if topic.highlight else "" %} 
{% set title = decoration + topic.title + decoration %} 
{% if topic.level == 1%} 
* [{{ title }}](#admin-{{ topic.id }}-anchor)
{% elif topic.level == 2 %}
  * [{{ title }}](#admin-{{ topic.id }}-anchor)
{% elif topic.level == 0 %}
* {{ title }}
{% endif %}
{% endfor %}

</navigation>