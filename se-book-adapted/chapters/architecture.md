<frontmatter>
{% import "se-book-adapted/config.md" as config with context %}
{% import "se-book-adapted/chapters/chapter.md" as chapter_template with context %}
{% set chapter = config.chapters.architecture %}
{{ chapter_template.add_front_matter(chapter) }}
</frontmatter>

{{ chapter_template.show_chapter(chapter) }}