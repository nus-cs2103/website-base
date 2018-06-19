<frontmatter>
title: "Software Engineering for Self-Directed Learners [CS2103/T Version]"
footer: footer.md
</frontmatter>

<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<include src="../common/header.md" />

<div class="website-content" id="all">

## Software Engineering for Self-Directed Learners

### About this Book

* [Acknowledgements]({{baseUrl}}/book/about/acknowledgements.html)
* [How to use this book]({{baseUrl}}/book/about/usage.html)


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
### {{ section.heading}}
{% for chapter in section.chapters %}
  {{ show_chapter(section, chapter) }}
{% endfor %}
{% endmacro %}


{% for section in config.topics %}
  {{ show_section(section) }}
{% endfor %}


### Supplementary

<!-- TODO: add review -->
* [Combined Exercises](combined/)
* [List of Definitions](common/definitions.html)

</div>
