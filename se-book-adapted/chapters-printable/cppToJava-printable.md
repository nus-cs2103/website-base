<frontmatter>
{% import "se-book-adapted/config.njk" as config with context %}
{% import "se-book-adapted/chapters-printable/chapter-printable.njk" as chapter_template with context %}
{% set chapter = config.chapters.cppToJava %}
{{ chapter_template.add_front_matter(chapter) }}
</frontmatter>

{{ chapter_template.show_chapter("../../book/", chapter) }}