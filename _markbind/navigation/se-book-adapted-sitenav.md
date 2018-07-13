<navigation>
{% import "se-book-adapted/config.njk" as config with context %}

* [Home {{ glyphicon_home }}, printable versions {{ glyphicon_print }}]({{baseUrl}}/se-book-adapted/index.html)
{% for section in config.topics %}
* **{{ section.heading }}**
{% for chapter in section.chapters %}
  * [{{ chapter.heading }}]({{baseUrl}}/se-book-adapted/chapters/{{ chapter.name }}.html)
{% endfor %}
{% endfor %}

</navigation>