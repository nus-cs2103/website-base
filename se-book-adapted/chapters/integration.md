<frontmatter>
{% import "se-book-adapted/config.md" as config %}
{% import "se-book-adapted/chapters/chapter.md" as chapter_template %}
{% set chapter = config.chapters.integration %}
{{ chapter_template.add_front_matter(chapter) }}
</frontmatter>

{{ chapter_template.show_chapter(chapter) }}