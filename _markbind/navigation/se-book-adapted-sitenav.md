<navigation>
{% import "se-book-adapted/config.njk" as config with context %}

* [Home :glyphicon-home:, printable versions {{ icon_print }}]({{baseUrl}}/se-book-adapted/index.html)
{% for section in config.topics %}
* **{{ section.heading }}**
{% for chapter in section.chapters %}
  * [{{ chapter.heading }}]({{baseUrl}}/se-book-adapted/chapters/{{ chapter.name }}.html)
{% endfor %}
{% endfor %}
* Supplementary
{% if module == "CS2113" or module == "TIC2002" or module == "TIC4001" %}
  * [C++ to Java]({{ baseUrl }}/se-book-adapted/chapters/cppToJava.html)
  * [Project Duke]({{ baseUrl }}/se-book-adapted/projectDuke/index.html)
{% endif %}
  * [Combined Exercises]({{ baseUrl }}/se-book-adapted/common/exercises.html)
  * [List of Definitions]({{ baseUrl }}/se-book-adapted/common/definitions.html)
</navigation>
