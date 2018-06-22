<frontmatter>
title: "Software Engineering for Self-Directed Learners [CS2103/T Version]"
footer: footer.md
siteNav: se-book-adapted-sitenav.md
</frontmatter>

<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<include src="../common/header.md" />

<div class="website-content" id="all">

## Software Engineering for Self-Directed Learners

<br/><big>

**About this Book**
</big>

* [Acknowledgements]({{baseUrl}}/book/about/acknowledgements.html)
* [How to use this book]({{baseUrl}}/book/about/usage.html)
* [All chapters as one printer-friendly page (huge file!) {{ glyphicon_print }}]


{% import "se-book-adapted/config.md" as config with context %}


{% macro show_chapter(section, chapter) %}

* [{{ chapter.heading }}]({{baseUrl}}/se-book-adapted/chapters/{{ chapter.name }}.html)
  <trigger for="pop:{{ chapter.name }}-preview">{{glyphicon_eye_open}}</trigger> [{{glyphicon_print}}]({{baseUrl}}/se-book-adapted/chapters/{{ chapter.name }}-printable.html)

<popover id="pop:{{ chapter.name }}-preview" title="{{ chapter.heading}} {{glyphicon_eye_open}}" placement="right">
  <div slot="content">
    <include src="../book/{{chapter.name}}/preview.md" />
  </div>
</popover>

{% endmacro %}


{% macro show_section(section) %}
<br/><big>

**{{ section.heading}}**
</big>
{% for chapter in section.chapters %}
  {{ show_chapter(section, chapter) }}
{% endfor %}
{% endmacro %}


{% for section in config.topics %}
  {{ show_section(section) }}
{% endfor %}

<br/><big>

**Supplementary**</big>

* [Combined Exercises](common/exercises.html)
* [List of Definitions](common/definitions.html)

</div>
