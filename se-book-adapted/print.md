<frontmatter>
title: "Software Engineering for Self-Directed Learners [Printable Version for {{ module_pair }}]"
footer: footer.md
</frontmatter>

<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<div class="website-content">

{% import "se-book-adapted/config.njk" as config with context %}
{% import "se-book-adapted/chapters-printable/chapter-printable.njk" as chapter_template with context %}

# <big>**Software Engineering for Self-Directed Learners**</big>

<span id="printable-version-description"><small>%%{{ icon_print }} This is a **printer-friendly** version. It omits exercises, optional topics (i.e., four-star topics), and other extra content such as learning outcomes.%%</small></span>

{% macro show_section(section) %}

# **SECTION: {{ section.heading | upper }}**
{% set is_first_chapter = true %}
{% for chapter in section.chapters %}
  {% if is_first_chapter %}
    {% set is_first_chapter = false %}
  {% else %}
{{ pagebreak }}
  {% endif %}
  {{ chapter_template.embed_chapter("../book/", chapter) }}
{% endfor %}
{% endmacro %}

{% set is_first_section = true %}

{% for section in config.topics %}
  {% if is_first_section %}
    {% set is_first_section = false %}
  {% else %}
{{ pagebreak }}
  {% endif %}
  {{ show_section(section) }}
{% endfor %}

</div>