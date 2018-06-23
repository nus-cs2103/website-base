{% import "se-book-adapted/config.njk" as config with context %}

{% macro find_level_three(topics, path) %}
{% for topic in topics %}
  {% if topic.name === path[2] %}
  {{ topic.priority }}
  {% endif %}
{% endfor %}
{% endmacro %}

{% macro find_level_two(topics, path) %}
{% for topic in topics %}
  {% if topic.name === path[1] %}
    {{ find_level_three(topic.level_three_topics, path) }}
  {% endif %}
{% endfor %}
{% endmacro %}

{% macro find_level_one(topics, path) %}
{% for topic in topics %}
  {% if topic.name === path[0] %}
    {{find_level_two(topic.level_two_topics, path)}}
  {% endif %}
{% endfor %}
{% endmacro %}

{% macro find_priority(chapter, path) %}
{% if (path | length) == 3 %}
  {{find_level_one(config.chapters[chapter].level_one_topics, path)}}
{% elseif (path | length) == 2 %}
  {{find_level_one(config.chapters[chapter].level_one_topics, [path[0], "", path[1]])}}
{% elseif (path | length) == 1 %}
  {{find_level_one(config.chapters[chapter].level_one_topics, ["", "", path[0]])}}
{% endif %}
{% endmacro %}


{{ find_priority("uml", ["classDiagrams", "introduction", "what"]) }}
{{ find_priority("softwareEngineering", ["introduction", "prosAndCons"]) }}
{{ find_priority("javaTools", ["varargs"]) }}