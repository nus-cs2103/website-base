<navigation>
{% import "se-book-adapted/config.njk" as config with context %}

* [Home {{ glyphicon_home }}, printable versions {{ icon_print }}]({{baseUrl}}/se-book-adapted/index.html)
{% for section in config.topics %}
* **{{ section.heading }}**
{% for chapter in section.chapters %}
  * [{{ chapter.heading }}]({{baseUrl}}/se-book-adapted/chapters/{{ chapter.name }}.html)
{% endfor %}
{% endfor %}
* Supplementary
  * [C++ to Java]({{ baseUrl }}/se-book-adapted/chapters/cppToJava.html)
  * [Combined Exercises]({{ baseUrl }}/se-book-adapted/common/exercises.html)
  * [List of Definitions]({{ baseUrl }}/se-book-adapted/common/definitions.html)

</navigation>