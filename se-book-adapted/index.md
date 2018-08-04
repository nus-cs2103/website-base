{% import "se-book-adapted/config.njk" as config with context %}


{% macro show_chapter(section, chapter, is_flat=false) %}

* [{{ chapter.heading }}]({{baseUrl}}/se-book-adapted/chapters/{{ chapter.name }}.html)
  <trigger for="pop:{{ chapter.name }}-preview">{{icon_preview}}</trigger> [{{icon_print}}]({{baseUrl}}/se-book-adapted/chapters-printable/{{ chapter.name }}-printable.html)

<popover id="pop:{{ chapter.name }}-preview" title="{{ chapter.heading}} {{icon_preview}}" placement="right">
  <div slot="content">
    <include src="../book/{{chapter.name}}/preview.md" />
  </div>
</popover>
{% endmacro %}


{% macro show_section(section, is_flat=false) %}
<big>

**{{ section.heading}}**
</big>
{% for chapter in section.chapters %}
  {{ show_chapter(section, chapter, is_flat) }}
{% endfor %}
{% endmacro %}


{% macro show_toc(is_flat=false) %}
<frontmatter>
title: "Software Engineering for Self-Directed Learners [{{ module_pair }} {{ "Flat " if is_flat }}Version]"
footer: footer.md
siteNav: se-book-adapted-sitenav.md
</frontmatter>

<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<include src="../common/header{{ "-flat" if is_flat }}.md" />

<div class="website-content" id="main">

## Software Engineering for Self-Directed Learners <small><small><small><span class='badge badge-pill badge-success'>{{ module_pair }} edition - 2018</span></small></small></small>

<a href="{{baseUrl}}/book/about/acknowledgements.html" target="_blank">Acknowledgements</a> | <a href="{{baseUrl}}/se-book-adapted/print.html" target="_blank"><md>All chapters as one **printer-friendly page** (huge file!) {{ icon_print }}</md></a>

{% for section in config.topics %}
  {{ show_section(section, is_flat) }}
{% endfor %}

<big>

**Supplementary**</big>

  {{ show_chapter("dummy", config.chapters.cppToJava) }}

* [Combined Exercises](common/exercises.html)
* [List of Definitions](common/definitions.html)

</div>
{% endmacro %}


{{ show_toc() }}
