{% import "se-book-adapted/config.njk" as config with context %}
{% import "se-book-adapted/chapters/chapter.njk" as chapter_template with context %}
{% set chapter = config.chapters.teamwork %}
<frontmatter>
{{ chapter_template.add_front_matter(chapter) | trim}}
</frontmatter>

{{ chapter_template.show_chapter(chapter) }}