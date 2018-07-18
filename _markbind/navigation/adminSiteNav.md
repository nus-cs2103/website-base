{% from "common/admin.njk" import topics with context %}

<navigation>

* [See all in one page (slow!)](index-flat.html)

{% for topic in topics %} 
{% set decoration = "==" if topic.highlight else "" %} 
{% set title = decoration + topic.title + decoration %} 
{% if topic.level == 1%} 
* [{{ title }}]({{ topic.link }})
{% elif topic.level == 2 %}
* [%%→%% {{ title }}]({{ topic.link }})
{% elif topic.level == 0 %}
* %%{{ title }}%%
{% endif %}
{% endfor %}

</navigation>