{% import "se-book-adapted/config.md" as config %}
{% import "se-book-adapted/chapters/chapter.md" as chapter_template %}


{% macro show_level_three(location, topic) %}
{% set level_location =  location + "/" + topic.name %}
  <panel type="seamless" expanded>
    <span slot="header" class="panel-title"><include src="{{ level_location }}/text.md#title"/></span>
    <include src="{{ level_location }}/text.md#body" />
  </panel>
{% endmacro %}


{% macro show_level_two(location, topic) %}
{% set level_location =  location + "/" + topic.name %}
{% set level_is_empty =  (topic.name == "") %}
{% if not level_is_empty %}
  <panel type="seamless" expanded>
    <span slot="header" class="panel-title"><include src="{{ level_location }}/text.md#title"/></span>
{% endif %}
  {% for sub_topic in topic.level_three_topics %}
    {{show_level_three(level_location , sub_topic) }}
  {% endfor %}
{% if not level_is_empty %}
  </panel>
{% endif %}
{% endmacro %}


{% macro show_level_one(location, topic) %}
{% set level_location =  location + "/" + topic.name %}
<panel type="seamless" expanded>
  <span slot="header" class="panel-title"><include src="{{ level_location }}/text.md#title" /></span>
  {% for sub_topic in topic.level_two_topics %}
    {{show_level_two(level_location , sub_topic) }}
  {% endfor %}
</panel>
{% endmacro %}


{% macro show_chapter(chapter) %}
<frontmatter>
title: {{ chapter.heading }}
</frontmatter>

{% set level_location =  "../../book/" + chapter.name %}
<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<div class="website-content" id="all">

<include src="../../common/header.md" />

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

{{ show_chapter(config.chapters.architecture) }}