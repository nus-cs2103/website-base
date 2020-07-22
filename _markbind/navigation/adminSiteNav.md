{% from "common/admin.njk" import topics with context %}
{% from "common/macros.njk" import  show_stars_in_nav with context %}


<navigation>

{% for topic in topics %}
{% set decoration = "==" if topic.highlight else "" %} 
{% set title = decoration + (topic.alt if topic.alt else topic.title) + decoration %}
{% if topic.level == 1%} 
* [{{ title }}]({{ baseUrl }}/admin/{{ topic.link }}) {{ show_stars_in_nav(topic.priority) if topic.priority }}
{% elif topic.level == 2 %}
  * [<small>{{ title }}</small>]({{ baseUrl }}/admin/{{ topic.link }}) {{ show_stars_in_nav(topic.priority) }}
{% elif topic.level == 0 %}
* {{ title }} :expanded:
{% elif topic.level == -1 %}
* {{ title }}
{% endif %}
{% endfor %}

</navigation>