<frontmatter>
title: "Software Engineering for Self-Directed Learners [Printable Version for CS2103/T]"
footer: footer.md
</frontmatter>

<link rel="stylesheet" href="{{baseUrl}}/book/css/textbook.css">

<div class="website-content">

{% import "se-book-adapted/config.md" as config %}
{% import "se-book-adapted/chapters/chapter-printable.md" as chapter_template %}

# Software Engineering for Self-Directed Learners

<span id="printable-version-description"><small>%%This is a **printer-friendly** version. It omits exercises, optional topics (i.e., four-star topics), and other extra content such as learning outcomes.%%</small></span>

{% macro show_section(section) %}
<hr>

# SECTION: {{ section.heading | upper }}
{% for chapter in section.chapters %}
  {{ chapter_template.embed_chapter("../book/", chapter) }}
{% endfor %}
{% endmacro %}


{% for section in config.topics %}
  {{ show_section(section) }}
{% endfor %}

</div>