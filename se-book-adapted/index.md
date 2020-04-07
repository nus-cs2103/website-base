{% import "se-book-adapted/config.njk" as config with context %}


{% macro show_chapter(section, chapter) %}

* [{{ chapter.heading }}]({{baseUrl}}/se-book-adapted/chapters/{{ chapter.name }}.html)
  [{{icon_print}}]({{baseUrl}}/se-book-adapted/chapters-printable/{{ chapter.name }}-printable.html)
{% endmacro %}


{% macro show_section(section) %}
<big>

**{{ section.heading}}**
</big>
{% for chapter in section.chapters %}
  {{ show_chapter(section, chapter) }}
{% endfor %}
{% endmacro %}


{% macro show_toc() %}
<frontmatter>
title: "Textbook"
header: header.md
footer: footer.md
siteNav: se-book-adapted-sitenav.md
</frontmatter>

<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<div class="website-content" id="main">

## Software Engineering for Self-Directed Learners {{ edition_badge }}

<a href="{{baseUrl}}/book/about/acknowledgements.html" target="_blank">Acknowledgements</a> | <a href="{{baseUrl}}/se-book-adapted/print.html" target="_blank"><md>All chapters as one **printer-friendly page** (huge file!) {{ icon_print }}</md></a>

{% for section in config.topics %}
  {{ show_section(section) }}
{% endfor %}

<big>

**Supplementary**</big>

  {{ show_chapter("dummy", config.chapters.cppToJava) }}

* [Combined Exercises](common/exercises.html)
* [List of Definitions](common/definitions.html)

</div>
{% endmacro %}


{{ show_toc() }}
