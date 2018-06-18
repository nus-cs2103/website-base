<frontmatter>
{% import "se-book-adapted/config.md" as config with context %}
{% import "se-book-adapted/chapters/chapter-printable.md" as chapter_template with context %}
{% set chapter = config.chapters.design %}
{{ chapter_template.add_front_matter(chapter) }}
</frontmatter>

{{ chapter_template.show_chapter("../../book/", chapter) }}