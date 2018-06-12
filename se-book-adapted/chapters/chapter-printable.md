{% macro add_front_matter(topic) %}
title: "Text Book Chapter [Printable] : {{ topic.heading }}"
footer: footer.md
{% endmacro %}

{% from "se-book-adapted/chapters/chapter.md" import show_priority %}

{% macro show_level_three(location, topic) %}
{% set level_location =  location + "/" + topic.name %}
{% set title =  "#### " + topic.heading + " <small><small>" + show_priority(topic.priority) + "</small></small>" %}
{{ title }}
<include src="{{ level_location }}/text.md#body" />
{% endmacro %}


{% macro show_level_two(location, topic) %}
{% set level_location =  location + "/" + topic.name %}
{% set level_is_empty =  (topic.name == "") %}
{% if not level_is_empty %}
  <include src="{{ level_location }}/text.md#title"/>
{% endif %}
  {% for sub_topic in topic.level_three_topics %}
    {{show_level_three(level_location , sub_topic) }}
  {% endfor %}
{% endmacro %}


{% macro show_level_one(location, topic) %}
{% set level_location =  location + "/" + topic.name %}
<include src="{{ level_location }}/text.md#title" />
  {% for sub_topic in topic.level_two_topics %}
    {{show_level_two(level_location , sub_topic) }}
  {% endfor %}
{% endmacro %}


{% macro show_chapter(chapter) %}
<frontmatter>
title: {{ chapter.heading }}
</frontmatter>

{% set level_location =  "../../book/" + chapter.name %}
<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<div class="website-content" id="all">

%%**<include src="{{ level_location }}/../path.md" inline />**%%

<div id="title">
  <include src="{{ level_location }}/text.md#title" />
</div>

<div id="main">

{% for topic in chapter.level_one_topics %}
  {{show_level_one(level_location, topic) }}
{% endfor %}

</div>

</div>
{% endmacro %}